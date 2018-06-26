# Calculadora de IMC


Faça um aplicativo que calcule o IMC de uma pessoa. Para calcular o IMC é necessário dividir o peso da pessoa pela altura ao quadrado:

```kotlin

val imc = peso / (altura * altura)

```

O aplicativo deve ter o seguinte layout:


![Calculadora de IMC](img/calculadora_imc.png)


## Adicional 

Após o calculo de IMC mostre ao usuário qual a classificação que ele se encotra de acordo com a tabela abaixo:


| IMC        | Classificação           |
| ------------- |:-------------:|
| < 16     | Magreza grave |
| 16 a < 17     | Magreza moderada      |
| 17 a < 18,5| Magreza leve      |
| 18,5 < 25| Saudável      |
| 25 a < 30| Sobrepeso      |
| 30 a < 35| Obesidade Grau I      |
| 35 a < 40| Obesidade Grau II (Severa)     |
| > 40| Obesidade Grau III (Mórbida)    |


