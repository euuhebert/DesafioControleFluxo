# Contador
Este é um programa em Java que recebe dois parâmetros inteiros do usuário e imprime os números entre eles. O programa também valida se o primeiro parâmetro é maior que o segundo e lança uma exceção personalizada chamada ParametrosInvalidosException.

## Como usar
Para executar o programa, você precisa ter o Java instalado no seu computador. Você pode baixar o Java [aqui]. Depois de instalar o Java, você pode compilar e executar o programa usando os seguintes comandos no terminal:

```
javac Contador.java
java Contador
```

O programa irá solicitar que você digite o primeiro e o segundo parâmetro. Por exemplo:

```
Digite o primeiro parâmetro
5
Digite o segundo parâmetro
10
```

O programa irá imprimir os números entre os parâmetros, incluindo o primeiro e excluindo o segundo. Por exemplo:

```
Imprimindo numero 5
Imprimindo numero 6
Imprimindo numero 7
Imprimindo numero 8
Imprimindo numero 9
```

Se você digitar um primeiro parâmetro maior que o segundo, o programa irá lançar uma exceção e imprimir a seguinte mensagem:

```
O segundo parâmetro deve ser maior que o primeiro
```

## Código fonte
Aqui está o código fonte do programa:

```java
import java.util.Scanner;

public class Contador  {
    public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite o primeiro parâmetro");
		int parametroUm = sc.nextInt();
		System.out.println("Digite o segundo parâmetro");
		int parametroDois = sc.nextInt();;
		
		try {
			//chamando o método contendo a lógica de contagem
			
			contar(parametroUm, parametroDois);
		
		}catch (ParametrosInvalidosException e) {
			//imprimir a mensagem: O segundo parâmetro deve ser maior que o primeiro
			System.out.println(e.getMessage());
		}
		
	}
	static void contar(int parametroUm, int parametroDois ) throws ParametrosInvalidosException {
		//validar se parametroUm é MAIOR que parametroDois e lançar a exceção
		if (parametroUm > parametroDois) {
			throw new ParametrosInvalidosException("O segundo parâmetro deve ser maior que o primeiro");

		}
		
		int contagem = parametroDois - parametroUm;
		for ( int i = 1; i <=contagem; i++) {
            System.out.println("Imprimindo numero " + i);
        }
	}
}
```

Espero que isso tenha sido útil para você. 😊
