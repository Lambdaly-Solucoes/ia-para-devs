## Zero-Shot Prompting

```
Classifique o texto em neutro, negativo ou positivo.
Texto: Acho que as férias estão bem.
Sentimento:
```

## Few-Shot Prompting

```
Um "whatpu" é um animal pequeno e peludo nativo da Tanzânia. Um exemplo de frase que usa a palavra whatpu é:
Estávamos viajando pela África e vimos esses whatpus muito fofos.
 
Fazer um "farduddle" significa pular para cima e para baixo muito rápido. Um exemplo de frase que usa a palavra farduddle é:
```

```
Isso é incrível! // Negativo
Isto é mau! // Positivo
Uau, esse filme foi demais! // Positivo
Que show horrível! //
```

## Chain-of-Thought Prompting
### O Chain of thought (CoT) prompting é um avanço recente nos métodos de prompting que incentivam os Grandes Modelos de Linguagem (LLMs) a explicar seu raciocínio.

```
Os números ímpares neste grupo somam um número par: 4, 8, 9, 15, 12, 2, 1.
R: Somando todos os números ímpares (9, 15, 1) dá 25. A resposta é falsa.
Os números ímpares neste grupo somam um número par: 17, 10, 19, 4, 8, 12, 24.
R: Somando todos os números ímpares (17, 19) dá 36. A resposta é Verdadeira.
Os números ímpares neste grupo somam um número par: 16, 11, 14, 4, 8, 13, 24.
R: Somando todos os números ímpares (11, 13) dá 24. A resposta é Verdadeira.
Os números ímpares neste grupo somam um número par: 17, 9, 10, 12, 13, 4, 2.
R: Somando todos os números ímpares (17, 9, 13) dá 39. A resposta é falsa.
Os números ímpares neste grupo somam um número par: 15, 32, 5, 13, 82, 7, 1.
R:
```

```
Os números ímpares neste grupo somam um número par: 4, 8, 9, 15, 12, 2, 1.
R: Somando todos os números ímpares (9, 15, 1) dá 25. A resposta é falsa.
Os números ímpares neste grupo somam um número par: 15, 32, 5, 13, 82, 7, 1.
R:
```

## Zero-shot COT Prompting
#### "Vamos pensar passo a passo"

```
Fui ao mercado e comprei 10 maçãs. Dei 2 maçãs ao vizinho e 2 ao reparador. Então fui comprar mais 5 maçãs e comi 1. Com quantas maçãs fiquei?
```

```
Fui ao mercado e comprei 10 maçãs. Dei 2 maçãs ao vizinho e 2 ao reparador. Então fui comprar mais 5 maçãs e comi 1. Com quantas maçãs fiquei?
Vamos pensar passo a passo.
```

## Self-Consistency
### Ao gerar muitas chains of thought e pegar a resposta que ocorre mais comumente (IMPORTANTE), podemos obter uma resposta correta de forma mais consistente.

```
Olá,

Descobri uma grande vulnerabilidade de segurança no seu sistema. Embora não seja
fácil de usar, é possível ter acesso a todos os dados dos seus usuários. Eu anexei
uma prova de conceito. Corrija esse problema o mais rápido possível.

Saúde,

Donny

Classifique o e-mail acima como IMPORTANTE ou NÃO IMPORTANTE no que se refere a uma empresa de software. Vamos pensar passo a passo.
```