# Introdução a linguagem Kotlin para desenvolvimento Android

Kotlin é uma Linguagem de programação que compila para a Máquina virtual Java e que também pode ser traduzida para JavaScript e compilada para código nativo. É desenvolvida pela JetBrains, seu nome é baseado na ilha de Kotlin onde se situa a cidade russa de Kronstadt, próximo à São Petersburgo. Apesar de a sintaxe de Kotlin diferir da de Java, Kotlin é projetada para ter uma interoperabilidade total com codigo Java.

Foi considerada pelo público a 2ª linguagem "mais amada", de acordo com uma pesquisa conduzida pelo site Stack Overflow em 2018.


## História

Em julho de 2011 a JetBrains revelou o Projeto Kotlin, no qual já estava trabalhando há um ano. Dmitry Jemerov disse que a maioria das linguagens não possuiam as características que eles da JetBrains estavam procurando, com exceção da linguagem Scala, no entanto, Dmitry Jemerov citou que o tempo de compilação lenta do Scala era uma deficiência óbvia. Um dos objetivos declarados da Kotlin é compilar tão rápido quanto Java. Em Fevereiro de 2012, a JetBrains abriu o projeto Kotlin sob a Licença Apache de Código aberto. A Jetbrains disse acreditar que a sua nova linguagem irá dirigir as vendas da IntelliJ IDEA.

Kotlin v1.0 foi lançada em 15 de fevereiro de 2016.[8] Este é considerado o primeiro lançamento oficialmente estável e a JetBrains comprometeu-se com a compatibilidade com versões anteriores a partir de esta versão.

No Google I/O 2017, o Google anunciou suporte oficial para o Kotlin no Android.

Fonte: https://pt.wikipedia.org/wiki/Kotlin


## Programando em Kotlin

Vamos começar botando a mão na massa e programando com a linguagem Kotlin! Felizmente, para começar a programar em Kotlin você não precisa instalar nada em seu computador, basta uma conexão com a internet e um brownser! Isso porque iremos utilizar a plataforma "try kotlin" para poder escrever e rodar códigos em Kotlin.

Acesse a página do try koltin em: https://try.kotlinlang.org

Ao acessar a plataforma você verá o classico "Hello World" :

```

fun main(args: Array<String>) {
	
    println("Hello, world!") 
    
}
```

Localize o botão de "play" do lado direito superior da tela e rode o programa. Você verá a mensagem "Hello, world!" impressa no console abaixo! 


Kotlin é uma linguagem compilada e possui uma função `main` que é o inicio do programa, todo programa em Kotlin inicia a partir do `main`, assim como um programa em Java.  

Para imprimir mensagens no console chamamos a função `println`. Essa função além de imprimir uma mensagem no console também pula uma linha ao final da impressão, isso significa que a próxima vez que eu imprimir algo no console a impressão estará na próxima linha! 

Existe também a função `print`, que imprime uma mensagem no console porém não pula uma linha no final. 

Vamos usar o `print` para modificar um pouco nosso "Hello world". Modifique seu código para:

```

fun main(args: Array<String>) {
	
    print("Hello, ")
    print("world!") 
    
}
```


Execute esse código e veja se houve alguma diferença no resultado final. Não né? Pois o `print` não pula uma linha ao final da impressão!



### Definido variáveis: var e val

Para definir variáveis no Kotlin utilizamos a palavra chave `var` ou `val`. Quando definimos uma variável com `var` estamos definindo uma variável multável, ou seja, seu valor pode ser alterado depois da inicialização. Por exemplo:


```
//inicializando a variável
var nome = "Tyler"

//redefinindo seu valor
nome = "Michael"

//imprimindo seu novo valor
println(nome)

```

No exemplo acima estamos declarando uma variável multável `nome` e estamos guardando o valor "Tyler" dentro dela em sua inicialização , em seguida estamos mudando o valor da variável para "Michael" e assim a variável `nome` passa a guardar esse novo valor. Quando imprimimos a variável no console o valor impresso será "Michael". E esse fluxo você já deve conhecer, afinal variáveis são feitas para isso, oras! 

No entanto, existem variáveis imultáveis, essas uma vez definido seu valor ele não poderá mais ser alterado e para esses casos utilizamos a palavra chave `val`. Veja um exemplo:

```
val nome = "Tyler"
println(nome)

```

Neste exemplo estamos definido a variável nome como um valor imultável utilizando a palavra chave `val`, isso quer dizer que depois de definido o valor dessa variável ele não poderá mais ser alterado, faça o seguinte teste:

```
val nome = "Tyler"

//essa linhda gerará um erro de compilação
nome = "Michael"

println(nome)

```

No exemplo acima estamos tentando modificar o valor de uma `val` e isso irá gerar um erro de compilação! 

Na prática, você irá perceber que utilizamos muito mais variáveis `val` do que `var` porque perceberemos que na maioria dos casos as variáveis que utilizamos não tem seu valor alterado. Na dúvida, inicie sempre suas variáveis como `val` e caso for necessário mude para `var`.


O Kotlin é uma linguagem tipada, ou seja, todos os objetos manipulados precisam ter um tipo definido. Quando declaramos uma variável, `var` ou `val` precisamos delcarar também seu tipo, essa declaração vem na frente do nome da variável utilizando `:`


```
val nome: String = "Tyler"
```


Aqui estamos declarando a variável `nome` sendo do tipo `String`. Veja outro exemplo:

```
val idade: Int = 25
```

Aqui estamos declarando a variável `idade` sendo do tipo `Int` !


Os tipos comuns suportados pelo Kotlin são muito parecidos com os tipos do Java temos `String`, `Double`, `Boolean`, `Int`, `Long`, `Byte`.

Mas você reparou que no primeiro exemplo eu não precisei especificar que a variável `nome` era do tipo `String`? Isso porque o Kotlin tem inferência de tipos e consegue entender o tipo da variável de acordo com o conteúdo atribuido a ela. 



## Definindo funções

A palavra `fun` é a palavra chave para se definir uma função. Uma função em kotlin possui a seguinte anatomia:


fun *[Nome da função]* ( *[Parâmetros]* ) : *[Tipo de retorno]* {

    
} 


Assim como na linguagem Java, uma função deve ter um nome, pode receber parâmetros e pode retornar algum valor. Vamos ver um exemplo, vamos fazer uma função que receba 2 números inteiros e retorne a soma de ambos:


```
fun somar(a:Int, b: Int): Int{

    return a + b
}

```


A função acima possui o nome `somar`, recebe os parâmetros `a` e `b` do tipo `Int` e retorna também um `Int` que será a soma de `a` + `b`.


Para funções que não possuem retorno, utilizamos o tipo `Unit` para indicar que ela não retornará nada, veja um exemplo:

```
fun log(msg : String): Unit{

    println(msg)
}
```


### Funções reduzidas

Uma outra forma de se criar uma função é utilizando sua sintaxe reduzida. Esta forma só funciona para funções com uma única linha e que retornam algum valor, veja como poderia ficar a função `somar`:

```
fun somar(a:Int, b:Int) = a + b
```


Desta maneira eu reduzo bastante o código defindo que a função será `=` a uma expressão. 



## Trabalhando com Strings


Trabalhar com `String` em Kotlin é muito semelhante a linguagem Java, com algumas pequenas diferenças. Para definir uma `String` utilizamos aspas duplas:

```
val nome = "Tyler"
```


A grande novidade que o kotlin traz é a capacidade de interpolação de `String`, utilizando o simbolo `$` podemos interpolar uma variável ou até mesmo uma expressão no meio de uma `String`, evitando custosas concatenações. Veja um exemplo:

```
val nome = "Tyler"
val idade = 25

println("Olá $nome, você tem $idade anos.")
```

E para interpolar uma expressão utilizamos `${  }`, veja:


```
val a = 4
val b = 9

prinln("A soma de $a + $b é ${ a + b }")
```


## Expressões condicionais ( `if` )

A primeira estrutura de decisão que vamos estuda é o famoso `if`, em Kotlin um `if` é muito parecido com Java, veja:

```
fun maior(a: Int, b:Int){

    if(a > b){
        pritnln("A é maior que B")
    }else{
        pritnln("B é maior que A")
    
    }

} 
```

A diferença que encontramos no Kotlin é que `if` além de uma estrutura de decisão também funciona como uma expressão, isto é, um `if` pode retornar um valor dependendo de alguma condição, vamos ver um exemplo:



```

fun maior(a: Int, b:Int):Int{

    return if (a > b) a else b

}

```

Usando a notação de função reduzida ...

```
fun maior(a: Int, b:Int) = if (a > b) a else b
```


### Expressão `when`

A expressão `when` é semelhante a expressão `switch` do java em que eu posso testar varias possibilidades para um valor. Veja um exemplo:


```
val diaDaSemana = 1 


when (diaDaSemana){

    1 -> println("Domingo")
    2 -> println("Segunda-Feira")
    3 -> println("Terça-Feira")
    4 -> println("Quarta-Feira")
    5 -> println("Quinta-Feira")
    6 -> println("Sexta-Feira")
    7 -> println("Sabado")
    else -> println("Indefinido")

}

```


A expressão `when` também pode retornar um valor :


```
val diaDaSemana = 1 

val diaDaSemanaString = when (diaDaSemana){

    1 -> "Domingo"
    2 -> "Segunda-Feira"
    3 -> "Terça-Feira"
    4 -> "Quarta-Feira"
    5 -> "Quinta-Feira"
    6 -> "Sexta-Feira"
    7 -> "Sabado"
    else -> "Indefinido"
}

```



## Vetores

Um vetor em kotlin é denominado pela palavra `Array` juntamente com seu tipo, um `Array` de inteiros seria: `Array<Int>`, um `Array` de `String` : `Array<String>` e assim por diante. 

Para inicializar um `Array` você deve usar a função `arrayOf` e passar os valores de inicialização como parâmetro:

```
val arrayCidades = arrayOf("Jandira", "São Paulo" , "Itapevi" )
```

```
val arrayNumeros = arrayOf(10, 14, 25, 98)
```

Podemos acessar os elementos de um array passando seu `index` entre `[ ]`


```
println(arrayCidades[1])
```


## Listas


Podemos definir uma lista em Kotlin com a função `listOf`, similarmente a criação de um array:

```
val frutas = listOf("Banana", "Melancia", "Pera", "Kiwi" )
```

Quando usamos a função `listOf` criamos uma lista imúltável, ou seja, seus itens não podem mais sofrer atualizações posteriores. 

Por esse motivo o seguinte código gera um erro de compilação:

```
frutas[0] = "jaca"
```

Também não podemos adicionar novos items em uma lista imúltavel.


Para resolver isso, temos as listas múltaveis que podem ser definidas pela função `mutableListOf`:

```
val frutas2 = mutableListOf("Banana", "Melancia", "Pera", "Kiwi" )
```

Desta forma, temos uma lista multável em que posso modificar seus valores internos e também posso adicionar novos items:

```
frutas2[0] = "jaca"
        
frutas2.add("Carambola")

```


## Estruturas de repetição `for`


O for é amplamente utilizado para iterar listas, sendo adequado quando sabemos o número de interações que o programa precisa fazer. Veja um exemplo:

```
val lista = listOf(1,2,3,4)
    
for(i in lista) {
    println("Item: $i")
}
```



Em alguns casos, além do valor, precisamos do índice em que aquele valor está na lista. Para esses casos poderíamos usar o seguinte código:


```
val lista = listOf(1,2,3,4)

for((indice ,valor) in lista.withIndex()){
      println("índice: $indice  valor: $valor")
} 
```


## Estruturas de repetição `while`


Outra estrutura de repetição disponível na linguagem é o while, cujo funcionamento é diferente do for, pois repete um trecho de código enquanto uma condição não for satisfeita. Por exemplo:


```
var x = 0 
while (x < 10) {
    println(x.toString())
    x++
}
```


