# Exericios Kotlin



## First


Crie uma função que receba 2 valores `Double` como parâmetro que correspondem a notas de P1 e P2 de uma aluno. A função deve calcular a média desse aluno e imprimir na tela sua nota de acordo com o seguinte conceito:


| Média de Aproveitamento        | Conceito           | 
| ------------- |:-------------:| 
|  Entre 9.0 e 10.0  | A |
|  Entre 7.5 e 9.0   | B |
|  Entre 6.0 e 7.5   | C |
|  Entre 4.0 e 6.0   | D |
|  Entre 4.0 e zero  | E |


## Soma de Array

A seguinte função em Kotlin deve efetuar a soma de um `Array` recebido como parâmetro:


```
fun arraySum(ar: Array<Int>): Int{


}
```

Implemente o código da função.


## Tabuada

Implemente a função `tabuada`, esta função deve receber um inteiro como parâmetro e imprimir sua tabuada do 1 ao 10. Ex:

Entrada: `5`

Saída:

```
5 X 1 = 5
5 X 2 = 10
5 X 3 = 15
...
```



## Diferença diagonal


Dado uma matriz quadrada, calcule a diferença absoluta entre a soma de suas diagonais.

Por exemplo, para a matriz mostrada abaixo:

```
1 2 3
4 5 6
9 8 9  
```

A soma da diagonal da esquerda para a direita é: `1+5+9 = 15`. 
A soma da diagonal da direita pra esquerda é: `3+5+9 = 17`

E a diferença absoluta: `|15 - 17| = 2`

Complete a função `diferencaDiagonal`. Essa função receberá uma matriz quadrada de inteiros e deve retornar um único inteiro como resultado.

```
fun diferencaDiagonal(a: Array<Array<Int>>): Int {

}
```

Para inicializar a matrix de teste utilize o seguinte código:

```

val matriz = arrayOf(
                arrayOf(1, 2, 3),
                arrayOf(4, 5, 6),
                arrayOf(9, 8, 9)
        )

```

## Negativos e positivos

Dado um array de inteiros, calcule quantos elementos são positivos, negativos e quantos tem valor zero. A função deve imprimir o resultado em três linhas.

```
fun positivosNegativos(arr: Array<Int>): Unit {


}
```


## Professor zangado

Um professor de matemática está zangado com seus alunos. Frustrado com a quantidade de faltas em suas aulas, ele decidiu cancelar a aula caso um número meinimo de alunos não estejam em sala quando a aula começar. 

O número mínimo de alunos será determinado por `k`

O tempo de chegada de cada aluno será dado por um `Array` de inteiros em que números negativos significam que o aluno chegou antes do ínicio da aula, números positivos indicam que o aluno chegou atrasado.

Veja o seguinte exemplo:

```
val k = 3
val a = arrayOf(-1, -3, 4, 2)
```

A entrada acima deve produzir a seguinte saída: `AULA CANCELADA` pois o número mínimo de alunos eram `3` e no incio da aula só tinham 2 alunos(`-1, -3`).


Veja mais um exemplo:

```
val k = 2
val a = arrayOf(0 ,-1, 2, 1)
```

A entrada acima deve produzir a seguinte saída: `AULA NORMAL` pois o professor esperava pelo menos `2` alunos e tinham dois alunos quando a aula começou (`0, -1`)


Implemente a função abaixo:

```
fun professorZangado(k: Int, a: Array<Int>): String {


}

```


## Quadrado Mágico


Faça uma função que receba uma `List` de inteiros como parâmetro, e retorne outra `List` com todos os números pares elevados ao quadrado, por exemplo:

```
val arrayEntrada = listOf( 1 , 4, 2, 5, 9, 6 )
```

Para essa entrada, o a função deve retornar o seguinte array:

```
[1 , 16, 4, 5, 81, 36 ]
```

No `arraySaida` todos os números pares foram elevados ao quadrado, os números impares contiam da mesma forma.

```
fun quadradoMagico(a :List<Int> ) : List<Int>{

    
}
```


## Multiplicação de Array

Faça uma função que receba um `Array` de inteiros e retorne a multiplicação de todos os elementos do Array, ex:


```
val a = arrayOf( 1 ,2, 3, 4, 5 )
```

Este array deve retornar `120` pois `1x2x3x4x5 = 120`.












