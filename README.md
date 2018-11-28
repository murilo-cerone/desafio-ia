# Desafio Python MPRJ

1 - Enquanto `N` é um inteiro positivo, considere a função `f(n)`, que satisfaz as seguintes sentenças:

```
f(0) = 0
f(0) = 1
f(n) = f(n-1) + f(n-2)
```

Crie um programa que determine `f(n)`.

2 - Utilize o programa anterior para calcular `f(10000)`. Estime a complexidade do algoritmo.

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


### O Caso Energia
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
    - Danos a Eletrodomésticos
    - Dificuldade de Renegociação
    - Negativação Indevida

Claro, temos que levar em consideração a qualidade dessa classificação, seus vieses e possíveis erros que, apesar de todo o capricho, nosso estagiário possa ter cometido.

Utilizando esta massa de dados produzimos um modelo de Machine Learning que produziu os seguintes resultados:

```
                                           precision    recall  f1-score   support

                      DemandaNaoResolvida       0.93      0.84      0.88      8954
                  DificuldadeRenegociacao       0.92      0.84      0.87      9120
DificuldadeContratacaoRecusaInjustificada       0.73      0.93      0.82      6526
     InterrupcaoInstabilidadeFornecimento       0.82      0.81      0.81      8444
                        CobrancaSobAmeaca       0.98      0.86      0.92      9476
                      NegativacaoIndevida       0.98      0.94      0.96      8484
              CobrancaServicoNaoFornecido       0.89      0.95      0.92      7713
                           CobrancaTarifa       0.83      0.95      0.89      7123

                              avg / total       0.89      0.89      0.89     65840
```


1 - Você consegue pensar em um Método Estatístico ou de Machine Learning para criar um modelo de aprendizado de máquina que possa utilizar esta massa para treino?
Implemente e demonstre seus testes e precisão.

2 - Explique porque você acha seus resultados piores ou melhores que os resultados que produzimos.

<hr>

### O Caso Telecom

Foi realizado um trabalho muito semelhante ao anterior, nos processos relacionados a Telecomunicações. 

Porém, como nosso estagiário é muito organizado, ele nos deu de bandeja uma tabela com termos que ele mesmo identificou como muito importantes nas Decisões e Sentenças que foram separadas - classificando em ordem por cada uma dessas classes. Segue a tabela:

```
    Termos                          Classe
1   Com: combo, pacote              Pacote de Serviços ( Combo )

2   Com: fixa, banda larga,         Telefonia Fixa
    velox, modem
    Sem: internet e combo
3   Com: fixa                       Internet Fixa

4   Com: pré-pago                   Telefonia Móvel Pré-paga
    Sem: TV por assinatura

5   Com: TV, assinatura, canais     TV por Assinatura
    Sem: Combo

6   Com: pacote de dados, 3G e      Internet Móvel
    4G

7   Com: celular, telefone          Telefonia Móvel Pós-paga
    móvel
```

Utilizando esta tabela e tentando classificar cada um desses documentos seguindo a ordem informada, ele está conseguindo classificar dezenas de documentos.

Mas queremos atingir os milhares!

1 - Você consegue pensar em um processo para separar documentos em pastas como no exercício anterior?

Apesar de muito esforçado, não é possível identificar com facilidade muitas outras classes, nosso estagiário é apenas um ser humano! Entendemos suas limitações.

Após esse processo de filtragem, foi produzido junto uma enorme massa de documentos que não foram classificados em nenhuma dessas categorias.

2 - Implemente um método de Machine Learning que consiga identificar possíveis novos tópicos e os termos que os identificam.
Demonstre seus testes, erros, acertos e precisão.

<hr>

## Entrega

    - O desafio deve ser entregue em até sete dias corridos após a confirmação do recebimiento do e-mail
    - O código e todos os insumos devem estar disponíveis em um repositório público versionado com Git
    - Você pode fazer em em Python ou no Jupyter, em Python :P
    - Nós gostamos muito de testes, faça um código testado e testável
    - Nossos clientes são humanos, gostam de visualizações ricas, a comunicação dos resultados é importantíssima, capriche!
    - Existem diversas receitas para este bolo. Você tem liberdade para escolher as suas ferramentas, desde que seja feito em Python. Solucione o problema mostrando pra gente no que você é bom/boa, mas não se esqueça de ser efetivo
    - Os insumos para a classificação dos textos estão neste repositório, clone/forque e divirta-se
