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





