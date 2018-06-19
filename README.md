
# Glossario de OOP

Glossário para o estudo dos conceitos aplicados à matéria de Programação Orientada à Objetos.

Índice
========

   * [Construtor](#construtor)
   * [Instanciação](#instanciação)
   * [Encapsulamento](#encapsulamento)
   * [Getters e Setters](#getters-e-setters)
   * [Assinatura de Método](#assinatura-de-método)
   * [Sobrecarga de Método](#sobrecarga-de-método)
   * [Escopo de classe](#escopo-de-classe)
   * [Escopo de objeto](#escopo-de-objeto)
   * [Palavras reservadas](#palavras-reservadas)
      * [Palavra reservada new](#palavra-reservada-new)
      * [Palavra reservada instanceof](#palavra-reservada-instanceof)
      * [Palavra reservada this](#palavra-reservada-this)
      * [Palavra reservada public e private](#palavra-reservada-public-e-private)
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

 O objetivo do encapsulamento é ocultar os atributos de uma classe, protegendo o estado de cada objeto. É considerado um dos princípios da programação orientada à objetos.

## Getters e Setters

São métodos de uma classe utilizados para aplicar os princípios do encapsulamento. Os *getters* servem para recuperar os atributos da classe e os *setters* servem para alterar/atribuir valores ao atributos.

**Exemplo:**

```java
public class Conta{
	private double saldo;
	
	public double getSaldo(){
		return this.saldo;
	}

	public void setSaldo(double novoSaldo){
		saldo = novoSaldo;
	}

}
```

## Assinatura de Método

A assinatura de método é uma forma de definir a "identidade" e exclusividade daquele método. Ela é composta, geralmente, pelo nome, tipo de retorno, tipo de parâmetros, quantidade de parâmetros e suas visibilidades.

## Sobrecarga de Método

A sobrecarga de método é quando se tem diversos métodos com o mesmo nome porem eles diferem nos tipos e quantidades de parâmetros e seus retornos.

**Exemplo:**

```java
public class FazAlgumaCoisa{
	public int fazAlgo(int num1, int num2){
		//Faz alguma operação
	}
	public double fazAlgo(double num3){
		//Faz alguma operação
	}
}
```
## Escopo de Classe

No escopo de classe o atributo/método pertence apenas à classe em que ele foi definido. No java se utiliza a palavra *static* para representar o escopo de classe.

**Exemplo:**
```java
public class EscopoClasse{
	public static int valor = 42;

	public static void bar(){
		//Realiza alguma operação
	}
	
}

```
## Escopo de Objeto

Quando um atributo/método em uma classe não é definido com o *static* ele é considerado pertencendo ao escopo de objeto. Por padrão os componentes da classe são considerados escopos de objeto.

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

### Palavra reservada *Public e Private*

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

É quando um uma classe necessita da instância de outra classe para que ela possa realizar suas operações.

**Exemplo UML:**

![Alt text](http://blogedsonbelem.com.br/blog/java/img/uml03.jpg "Exemplo agregação")

### Relacionamento de Agregação

Num relacionamento de Agregação, uma classe pode ser composta por outras classes, porém essas classes adjacentes não deixam de existir se a classe principal seja "apagada".

**Exemplo UML:**

![Alt text](https://i.imgur.com/GkJTUr0.gif "Exemplo agregação")

### Relacionamento de Composição

O relacionamento de composição é parecido com o de agregação, porem neste tipo de relacionamento, se a classe principal deixar de existir a outras adjacentes também são apagadas. 

**Exemplo UML:**
![Alt text](https://i.stack.imgur.com/iBdxi.png "Exemplo agregação")
