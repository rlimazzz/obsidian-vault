Todos conteiners da STL do C++ são passados por valor em funções, então se quisermos fazer uma mudança no conteiner original temos que passar com & atrás do conteiner, por exemplo:

	#include <bits/stdc++.h>

	using namespace std;
	
	void mudanca(vector<int> &vetor, int idx, int valor) {
		vetor[idx] = valor;
	}
	
	
	int main() {
		vector<int> vetor = {1, 2, 3, 4, 5};
	
		for(auto x : vetor) {
			cout << x << " ";
		}
		cout << endl;
	
		mudanca(vetor, 2, 10);
	
		for(auto x : vetor) {
			cout << x << " ";
		}
		cout << endl;
	}

Seria a maneira certa de mudar o valor original em um vetor, isso vale para qualquer conteiner do STL, se não passarmos o endereço de memória do conteiner o C++ criará uma cópia dentro da função e modificará aquela cópia ao invés do original. Segue o exemplo: 

	#include <bits/stdc++.h>

	using namespace std;
	
	void mudanca(vector<int> vetor, int idx, int valor) {
		vetor[idx] = valor;
	
		for(auto x : vetor) {
			cout << x << " ";
		}
		cout << endl;
	}
	
	
	int main() {
		vector<int> vetor = {1, 2, 3, 4, 5};
	
		for(auto x : vetor) {
			cout << x << " ";
		}
		cout << endl;
	
		mudanca(vetor, 2, 10);
	
		for(auto x : vetor) {
			cout << x << " ";
		}
		cout << endl;
	}