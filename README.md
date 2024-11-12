# Operador Condicional Ternário

A última estrutura de condição que estudaremos será o operador ternário. Este traz algumas melhorias em relação ao If Else e o Switch Case, mas também possui algumas desvantagens.

Eis o link da documentação oficial: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Conditional_operator


## Estrutura

Dentro todas as estruturas de condição, o operador ternário é o que possui a estrutura mais simples, mas igualmente é essencial observar os caracteres e suas posições: 

``` condição ? saida_1 : saida_2 ```

- A ```condição```, como de costume será o que queremos validar.
- O símbolo de interrogação ```?``` é parte essencial da estrutura e pode ser interpretada como uma pergunta, se a condição for verdadeira, então...
- A ```saida_1``` representa a primeira resposta da pergunta, do que tentamos validar.
- Enquanto que a ```saida_2``` reprenta a segunda resposta da pergunta.

## São Sempre Duas Respostas

Uma das desvantagens da operação ternária é a impossibilidade de obter apenas um resultado, ou seja, não adicionar os ```:``` para a segunda resposta.

A forma mais simples de evitar é tentar transformar a pergunra em "sim e não", normalmente o não, não importa, por isso não tem necessidade obtê-lo. Se a pergunta não puder ser transformada, então ela terá duas respostas e será possível utilizar o ternário.


## Pergunta Dentro de Pergunta

Como o objetivo é ser uma estrutura simples, ela possui apenas uma peculiaridade, assim como as demais; a possibilidade de colocar mais estruturas dela mesma uma aninhada a outra, ou seja, pergunta dentro de pergunta.

``` condição_1 ? saida_1 : condição_2 ? saida_2 : saida_3 ```

A ```condição_1``` não necessariamente precisa ser igual a ````condição_2```, como por exemplo:

```
<script>
// Entrada de dados
    let numero = parseInt(prompt("Digite um número"));


    // Processamento
    let ePar = numero == 0 ? "Neutro" : numero % 2 == 0 ? "Par" : "Ímpar"
    

    // Saída de dados
    document.write(ePar);

</script>
```
- Na primeira condição, estamos verificando se o ```numero``` é igual a zero, caso seja, será apresentado em tela a mensagem ```Neutro```.
- Caso contrário, será verificado se a divisão por 2 sobra resto zero, caso sobre, imprime a mensagem ```Par```.
- Case não seja zero e nem par, resta apenas que seja ```Ímpar```.

Essa estrutura pode ser ajustada visualmente para auxiliar o entendimento:

```
<script>
// Entrada de dados
    let numero = parseInt(prompt("Digite um número"));


    // Processamento
    let ePar = numero == 0 ? "Neutro" 
    : numero % 2 == 0 ? "Par" 
    : "Ímpar"
    

    // Saída de dados
    document.write(ePar);

</script>
```

## Momentos de utilidade

O operador ternário será essencial em situações que necessitarem uma ou muito poucas instruções a serem realizadas, como um: cálculo, texto, concordância verbal, bloco de código, elemento.

- Exemplo de cálculo apresentado acima.
- Texto: ```let texto = fruta == "tomate" ? "Verdadeiro" : "Falso"```.
- Concordância verbal: ``` document.write(`...X pessoa${pessoa > 1 ? "s" : ""} aprendem programação...`) ```.
- Bloco de código: ``` isUser == "Admin" ? {...} : {...} ```.
- Elemento: ``` isUser == "Admin" ? menuAdmin() : menuUser() ```.

Ele é muito mais simples que as outras duas estruturas de condição, mas também específico em utilização.
