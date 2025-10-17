Matéria interessante pois vemos o que está por trás das linguagens de programação pelo Assembly, ajudando também a melhorar a complexidade de algoritmos e estrutura de dados [[STL]], entendendo o funcionamento dos compiladores Exemplo de código em C:

```C
int nums[] = {10, -21, -30, 45};

int main() {
	int i, *p;
	for(int i = 0, p = nums;i != 4;i++;p++) {
		printf("%d\n", *p);
	}
	return 0;
}
```

```asm
.data 
	nums : .int 10, -21, -30, 45
	
.text 

.globl main 
	main: 
		movl $0, %edx # move o número 0 para o registrador edx
		movq $nums, %r11 # move os valores de nums para o registrador r11
		
	.L1 : 
		cmpl $4, %edx # if (i == 4), faz apenas uma comparação entre o número 4 e o número armazenado no registrador edx
		je .L2 # se for igual a 4, que foi o que a gente comparou, a gente pula para o final do for
		movl (%r11), %eax # eax = *p, aqui a gente está atribuindo o ponteiro de p ao registrador eax
		addl $1, %edx # i++
		addq $4, %r11, # p++
		jmp .L1
		
	.L2 :
		ret
```

Labels são usadas para **nomear** variáveis globais, funções e posições para jumps. Labels iniciados por ".L" não são visíveis fora do arquivo.

Exemplos de variáveis globais:

```asm
.data
	num : .int 1024
	i: .short 0x33AF
	str01: .ascii "Hello\0"
	str02: .asciz "Hello"
	str03: .string "Hello"
	
	vet: .int 1, 2, 3, 4, 5, 6
```

Tipos de dados assembly:
	.byte  : 1 byte
	.short : 2 bytes
	.int : 4 bytes
	.quad : 8 bytes
