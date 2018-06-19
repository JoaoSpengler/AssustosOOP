
# Glossario de OOP

Glossário para o estudo dos conceitos aplicados à matéria de Programação Orientada à Objetos.

Índice
========

   * [Construtor](#construtor)
   * [Instanciação](#instanciação)
   * [Encapsulamento](#encapsulamento)
   * [Getters / Setters](#getters-/-setters)
   * [Assinatura de Método](#assinatura-de-método)
   * [Sobrecarga de Método](#sobrecarga-de-método)
   * [Escopo de classe](#escopo-de-classe)
   * [Escopo de objeto](#escopo-de-objeto)
   * [Palavras reservadas](#palavras-reservadas)
      * [Palavra reservada new](#palavra-reservada-new)
      * [Palavra reservada instanceof](#palavra-reservada-instanceof)
      * [Palavra reservada this](#palavra-reservada-this)
      * [Palavra reservada public/private](#palavra-reservada-public-private)
      * [Palavra reservada final](#palavra-reservada-final)
   * [Relacionamentos](#relacionamentos)
      * [Relacionamento de Dependência](#relacionamento-de-dependência)
      * [Relacionamento de Agregação](#relacionamento-de-agregação)
      * [Relacionamento de Composição](#relacionamento-de-composição)

## Construtor

Construtor é um método de uma classe, é utilizado para a criação de um objeto. Sempre que se instanciar um objeto o método construtor será usado. Caso o construtor não seja definido na classe, será utilizado um **padrão**.

Pode-se ter construtores com parâmetros de entradas ou sem tais parâmetros, porem uma classe pode apenas ter um construtor sem parâmetros. Não existe um limite de quantos construtores (com parâmetros) uma classe pode ter.

**Exemplos:**
```java
public class exemploConstrutorComParametros {

    public exemploConstrutorComParametros(int valorA, int valorB) {
        //Restante do código
    }

}
```
```java
public class ExemploConstrutorSemParametros {

    public ExemploConstrutorSemParametros() {
        //Restante do código
    }

}
```

## Instanciação

A instanciação de uma classe é um processo para gerar um objeto dela. No processo de instanciação se usa a [palavra reservada new](#palavra-reservada-new).

**Exemplo:**
```java
public class ExemploInstanciacao {

    public void foo() {
        ExemploInstanciacao exemplo = new ExemploInstanciacao();
        //Restante do código
    }
    
}
```
## Encapsulamento

## Getters / Setters

## Assinatura de Método

## Sobrecarga de Método

## Escopo de Classe

## Escopo de Objeto

## Palavras Reservadas

### Palavra reservada *New*

A palavra *new*  tem como função instanciar um objeto de uma classe. O objeto instanciado pode ser referenciado por uma variável ou não.

**Exemplo:**
```java
public class ExemploNew {

	public void new(){
		new ExemploNew(); //Sem refencia

		ExemploNew teste = new ExemploNew(); //Com referencia
	}
}
```

### Palavra reservada *Instanceof*

A palavra *instanceof* compara se um objeto pertence ao mesmo tipo de uma determinada classe. O resultado irá retornar um valor booleano.

**Exemplo:**
```java
public class Animal{
	
	Animal humano = new Animal();
	boolean resposta;
	resposta = (humano instanceof animal)

}
```

### Palavra reservada *This*

A palavra *this* é utilizada para um objeto se referir a ele mesmo. Em muitos casos esta palavra é utilizada nos métodos de uma classe para se referenciar aos seus atributos.

**Exemplo:**

```java
public class Conta{

	//Atributos
	double saldo;

	public void deposita(double valor) {
		this.saldo += valor;
	}

}
```

### Palavra reservada *Public / Private*

Palavras utilizadas para definir a visibilidade de atributos/métodos/classes. O *public* define que a visibilidade é aberta para todo o sistema e para as outras classes, sendo possível sofrer alterações de suas características por meios externos.  O *private* define que apenas aquele classe tem visibilidade dessas características e somente ela pode realizar alterações.

**Exemplo:**
```java
public class Conta{
	//Atributos
	public int codigo; //Atributo publico
	private double saldo; //Atributo privado
}

```

### Palavra reservada *Final*

A palavra *final* é utilizada para valores constantes e que serão apenas de leitura, valores imutáveis.

**Exemplo:**
```java
//Classe final
final class Final{

    //Variavel final
    final int HorasdoDia = 24;
    
}
```
## Relacionamentos

### Relacionamento de Dependência

### Relacionamento de Agregação

### Relacionamento de Composição


