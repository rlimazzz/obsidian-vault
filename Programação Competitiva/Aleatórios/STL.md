Todos contêineres da STL do C++ são passados por valor em funções, então se quisermos fazer uma mudança no contêiner original temos que passar com & atrás do contêiner, por exemplo:

```c++
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
```

Seria a maneira certa de mudar o valor original em um vetor, isso vale para qualquer contêiner do STL, se não passarmos o endereço de memória do contêiner o C++ criará uma cópia dentro da função e modificará aquela cópia ao invés do original. Segue o exemplo: 

```c++	
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
```

Deque é um contêiner da STL C++ onde você pode inserir e remover tanto na frente do vetor quanto atrás, exemplo de uso:

```c++
#include <bits/stdc++.h>

using namespace std;

void printe(deque<int> &valores) {
	for(auto x : valores) {
		cout << x << " ";
	}	
	cout << "\n";
}

void solve() {
	deque<int> valores;

	valores.push_back(1);
	valores.push_back(2);
	valores.push_front(3);

	printe(valores);

	valores.pop_front();

	printe(valores);

	valores.push_back(5);

	printe(valores);

}
```

