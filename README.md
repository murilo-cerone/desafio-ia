# Desafio Python MPRJ

1 - Enquanto N é um inteiro positivo, considere a função f(n), que satisfaz as seguintes sentenças:

```
f(0) = 0
f(0) = 1
f(n) = f(n-1) + f(n-2)
```

Crie um programa que determine f(n)

2 - Utilize o programa anterior para calcular f(10000). Estime a complexidade do algoritmo.

3 - Implemente um programa que liste todos os nós de um nível de uma árvore binária.

4 - Você possui um site com um bilhão de usuários, cujos IDs são inteiros, positivos e sequenciais (de 1 até um bilhão).<br>
O log de acesso do seu servidor no último mês tem 500GB, onde constam esses IDs.<br>
Você quer saber quantos usuários únicos acessaram o site nesse período, mas sua máquina só tem 512 MB de memória.<br>
Como você desenvolveria uma aplicação para esse fim sem usar ferramentas externas?

5 - Recebemos recentemente um arquivo de texto com nomes de diversos procurados pela justiça no seguinte formato:

```nome: Fulano da Silvanome: Beltrano José Pereira nome: Ciclano Feliciano Marcianonome: Ildo Vieira Pereiranome: João Ninguém nome: Fulaninha```

Não é um dos melhores formatos de arquivo para se trabalhar, precisamos de uma solução!<br>
Produza uma **Regex Python** que obtenha apenas os nomes completos 

<hr>

## Classificação de Documentos

No MPRJ tratamos de grandes massas de documentos textuais.<br>
Hoje, boa parte deste trabalho é realizado pelos servidores da casa de forma manual, old fashion: abre o documento, lê o documento, entende o documento, toma uma decisão acerca do documento.<br>

Com a ajuda da Estatística e da Inteligência Artificial queremos mudar esta realidade!

Anualmente, o setor de Apoio Operacional a Demandas do Consumidor analisa mais de 580.000 processos do Tribunal de Justiça do Rio de Janeiro. 

Este trabalho é realizado pelos nossos caprichosos e empenhados estagiários!

Recentemente, nosso intrépido estagiário recebeu uma gloriosa demanda: identificar possíveis tutelas coletivas em processos relativos a Forncecimento de Energia Elétrica no estado do Rio de Janeiro. 

Para não maltratar muito nosso servidor público, separamos Decisões Interlocutórias e Sentenças para que ele possa trabalhar e ele identificou, classificou e separou alguns tópicos, são eles:

    - Cobrança de Servico Não Fornecido
    - Problemas de Cobrança ou Tarifa
    - Dificuldade de Contratação ou Recusa Injustificada
    - Interrupção ou Instabilidade no Fornecimento
    - Cobrança Sob Ameaça
    - Danos a Eletro-domésticos
    - Dificuldade de Renegociacao
    - Negativação Indevida


Utilizando esta massa de dados produzimos um modelo de Machine Learning que produziu os seguintes resultados:




1 - Você consegue pensar em um Método Estatístico ou de Machine Learning para criar um modelo de aprendizado de máquina que possa utilizar esta massa para treino?
Implemente e demonstre seus testes e precisão.