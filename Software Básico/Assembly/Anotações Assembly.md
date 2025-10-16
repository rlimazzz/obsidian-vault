Exemplo de código em C:

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

