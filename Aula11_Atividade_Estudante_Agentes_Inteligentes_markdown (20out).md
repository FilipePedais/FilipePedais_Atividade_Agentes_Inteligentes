# Atividade sobre agentes inteligentes

Aula 20/10/2026 | Professora Kadidja Valéria | Inteligência artificial

**Disciplina:** Linguagens Formais e Autômatos | ciência da Computação

**Estudante:** Filipe Pedais | **Turma:** Ciência da Computação - N1

Realize os exercícios 2.3, 2.4 e 2.5 do Capítulo 2 sobre agentes inteligentes. Analise a racionalidade, descreva ambientes de tarefa por meio do modelo PEAS e explique os conceitos com suas próprias palavras. Utilize o capítulo disponibilizado e justifique suas respostas.

**Modalidade sugerida:** individual com consulta. **Tempo estimado:** 2h30. **Prazo:** conforme orientação da professora.

## Preparação
Leia os tópicos sobre racionalidade, ambientes e estrutura dos agentes, especialmente a Seção 2.3.2.

## Exercício 2.3
Para cada afirmação, indique V ou F, justifique e forneça exemplo ou contraexemplo. Explicite as hipóteses utilizadas.

### a. Um agente que detecta apenas informações parciais sobre o estado não pode ser perfeitamente racional.

- Julgamento: F
- Justificativa: Um agente não precisa saber tudo para tomar a melhor decisão possível. Ele deve escolher a ação com maior resultado esperado usando o que conseguiu perceber e o que já sabe.
- Exemplo ou contraexemplo: Um aplicativo de rotas pode escolher o melhor caminho mesmo sem saber se haverá um acidente mais à frente.

### b. Existem ambientes de tarefa nos quais nenhum agente reativo puro pode comportar-se racionalmente.

- Julgamento: V
- Justificativa: As vezes é necessário lembrar o que aconteceu antes. Um agente que só reage ao instante atual pode repetir um erro.
- Exemplo ou contraexemplo: um robô que precisa visitar duas salas, mas só identifica se o chão atual está limpo, não consegue decidir sempre qual sala falta verificar usando apenas essa leitura.

### c. Existe um ambiente de tarefa em que todo agente é racional.

- Julgamento: V
- Justificativa: Se nenhuma escolha fizer diferença para o resultado, todas terão o mesmo desempenho esperado.
- Exemplo ou contraexemplo: um jogo de teste que dá exatamente cinco pontos independentemente do botão apertado.

### d. A entrada para o programa de agente é a mesma que a entrada para a função de agente.

- Julgamento: F
- Justificativa: A função de agente relaciona o histórico completo de percepções com uma ação. Já o programa recebe a percepção atual e pode guardar informações anteriores na memória.
- Exemplo ou contraexemplo: um robô recebe agora o aviso de obstáculo, mas seu programa pode lembrar que já tentou passar pela esquerda.

### e. Toda função de agente é implementável por uma combinação de programa/máquina.

- Julgamento: F
- Justificativa: Uma função pode ser definida de maneira abstrata mesmo que não exista um programa capaz de calculá-la em todos os casos. Também há limites físicos de memória e processamento.
- Exemplo ou contraexemplo: uma função que exigisse resolver corretamente qualquer instância de um problema não computável não poderia ser implementada por um computador comum.

### f. Suponha que um agente selecione sua ação uniformemente ao acaso do conjunto de ações possíveis. Existe um ambiente de tarefa determinista em que esse agente é racional.

- Julgamento: V
- Justificativa: Isso acontece quando todas as ações disponíveis são igualmente boas.
- Exemplo ou contraexemplo: em uma simulação, apertar A ou B sempre acende a mesma luz e rende a mesma pontuação. Sortear entre A e B não prejudica o desempenho.

### g. É possível para um dado agente ser perfeitamente racional em dois ambientes de tarefa distintos.

- Julgamento: V
- Justificativa: Se a estratégia continuar sendo a melhor nas duas situações, não é necessário mudar o agente.
- Exemplo ou contraexemplo: um controlador que desliga uma lâmpada quando não há ninguém pode funcionar de modo racional em duas salas com sensores e objetivos equivalentes.

### h. Todo agente é racional em um ambiente não observável.

- Julgamento: F
- Justificativa: Mesmo sem sensores, o agente ainda pode fazer escolhas boas ou ruins usando informações anteriores.
- Exemplo ou contraexemplo: um temporizador programado para irrigar uma planta por dez minutos pode cumprir a tarefa; outro que nunca liga a água não cumpre o mesmo objetivo.

### i. Um agente jogador de pôquer perfeitamente racional nunca perde.

- Julgamento: F
- Justificativa: Decidir bem não significa ganhar todas as vezes. O pôquer envolve cartas desconhecidas e sorte.
- Exemplo ou contraexemplo: mesmo apostando com boas chances, o jogador pode perder quando o adversário recebe a carta de que precisava.

## Exercício 2.4
Para cada caso, delimite o agente, preencha o PEAS e justifique todas as classificações. Considere Titã como cenário hipotético do exercício.

### Caso 1 — Jogar futebol.

- Agente analisado: um jogador robótico de uma equipe.
- Objetivo e hipóteses: partida oficial, com companheiros e adversários.
- P — Medida de desempenho: Contribuir para a vitória, acertar passes, evitar faltas e ajudar na defesa.
- E — Ambiente: Gramado, bola, traves, árbitro e demais jogadores.
- A — Atuadores: Motores de locomoção, pernas para chutar e comunicação com a equipe.
- S — Sensores: Câmeras, sensores de posição, equilíbrio e distância.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcial | não enxerga todos os jogadores nem sabe suas intenções. |
| Número de agentes | Multiagente | coopera com seu time e compete com o outro. |
| Previsibilidade | Estocástico | desvios da bola e movimentos de jogadores geram incerteza prática. |
| Dependência entre decisões | Sequencial | um passe muda as opções da próxima jogada. |
| Mudança durante a decisão | Dinâmico | a partida continua enquanto o robô decide. |
| Natureza dos elementos | Contínuos | posição, velocidade e tempo variam continuamente. |
| Conhecimento do funcionamento | Conhecido | conhece regras e movimentos básicos, mesmo sem prever tudo. |

### Caso 2 — Explorar os oceanos subterrâneos de Titã.

- Agente analisado: Sonda/Submarino robótico explorador autônomo.
- Objetivo e hipóteses: Mapear o oceano subterrâneo e coletar amostras químicas/biológicas mantendo a integridade do veículo em ambiente extremo.
- P — Medida de desempenho: Área oceânica mapeada, volume e relevância das amostras coletadas, preservação da sonda e autonomia energética.
- E — Ambiente: Oceano de fluido líquido sob a crosta de gelo de Titã, escuridão, correntes aquáticas, relevo rochoso e alta pressão.
- A — Atuadores: Propulsores marítimos, braço mecânico de coleta, broca de perfuração, sistema de flutuabilidade e transmissor sonar/rádio.
- S — Sensores: Sonar de varredura, câmeras infravermelhas, sensores de pressão e temperatura, espectrômetro e giroscópio.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcial | A escuridão e a turbidez do fluido limitam o alcance dos sensores no oceano. |
| Número de agentes | Agente único | Não há outros agentes inteligentes conhecidos operando no ambiente submarino de Titã. |
| Previsibilidade | Estocástico | Correntes marítimas imprevistas e obstáculos ocultos introduzem incertezas nos resultados. |
| Dependência entre decisões | Sequencial | O consumo de energia e rotas escolhidas afetam diretamente a capacidade de sobrevivência futura. |
| Mudança durante a decisão | Dinâmico | As correntes aquáticas e a posição da sonda mudam enquanto o agente delibera. |
| Natureza dos elementos | Contínuo | Pressão, temperatura, velocidade, localização espacial e tempo variam continuamente. |
| Conhecimento do funcionamento | Desconhecido | O ambiente aquático de Titã não é totalmente conhecido \\(a\ priori\\), exigindo exploração e aprendizado. |

### Caso 3 — Comprar livros usados de IA na Internet.

- Agente analisado: programa que compara anúncios e faz compras dentro de um orçamento definido.
- Objetivo e hipóteses: Realizar a tarefa com segurança e bom desempenho.
- P — Medida de desempenho: Comprar a edição certa, em bom estado, com menor custo total e entrega confiável.
- E — Ambiente: Sites de sebos, anúncios, vendedores, compradores e serviços de entrega.
- A — Atuadores: Pesquisar páginas, enviar requisições, adicionar ao carrinho e finalizar pedidos.
- S — Sensores: Dados dos anúncios, avaliações, preços, frete e respostas das plataformas.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcial | fotos e descrições não garantem o estado real do livro. |
| Número de agentes | Multiagente | vendedores e outros compradores influenciam a disponibilidade. |
| Previsibilidade | Estocástico | anúncios podem mudar e entregas podem atrasar. |
| Dependência entre decisões | Sequencial | comprar um título reduz o dinheiro para os próximos. |
| Mudança durante a decisão | Dinâmico | preço e estoque podem mudar durante a pesquisa. |
| Natureza dos elementos | Mistos | cliques e exemplares são discretos; tempo e custo podem ser modelados em escalas contínuas. |
| Conhecimento do funcionamento | Parcialmente desconhecido; classificado como desconhecido | sabe usar a loja, mas precisa aprender a confiabilidade de vendedores e anúncios. |

### Caso 4 — Jogar uma partida de tênis.

- Agente analisado: robô que disputa uma partida contra outro jogador.
- Objetivo e hipóteses: Realizar a tarefa com segurança e bom desempenho.
- P — Medida de desempenho: Ganhar pontos e sets, acertando golpes e evitando erros.
- E — Ambiente: Quadra, rede, bola, linhas e adversário.
- A — Atuadores: Locomoção, braço mecânico e raquete.
- S — Sensores: Câmeras, sensores de movimento e de contato com a bola.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcial | não conhece antecipadamente a jogada do rival. |
| Número de agentes | Multiagente competitivo | cada jogador tenta vencer o outro. |
| Previsibilidade | Estocástico | vento e pequenas variações do contato dificultam prever o resultado. |
| Dependência entre decisões | Sequencial | um golpe altera o posicionamento para o próximo. |
| Mudança durante a decisão | Dinâmico | a bola continua em movimento. |
| Natureza dos elementos | Contínuos | trajetória, força, ângulo e velocidade. |
| Conhecimento do funcionamento | Conhecido | conhece as regras e os efeitos básicos das batidas. |

### Caso 5 — Praticar tênis contra uma parede.

- Agente analisado: robô que rebate a bola repetidamente.
- Objetivo e hipóteses: Realizar a tarefa com segurança e bom desempenho.
- P — Medida de desempenho: Conseguir muitas rebatidas seguidas com boa precisão.
- E — Ambiente: Parede, piso, bola e espaço de treino.
- A — Atuadores: Rodas ou pernas e braço com raquete.
- S — Sensores: Câmeras e sensores de posição e impacto.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcial | sensores podem não captar perfeitamente rotação e velocidade da bola. |
| Número de agentes | Único | a parede não escolhe jogadas nem tem objetivos. |
| Previsibilidade | Determinístico no modelo idealizado | mesmas condições e mesmo golpe produzem o mesmo retorno. |
| Dependência entre decisões | Sequencial | cada batida determina o retorno seguinte. |
| Mudança durante a decisão | Dinâmico | a bola se move enquanto o robô calcula. |
| Natureza dos elementos | Contínuos | posição, tempo e força da batida. |
| Conhecimento do funcionamento | Conhecido | o agente possui um modelo do movimento e das colisões. |

### Caso 6 — Realizar um salto de altura.

- Agente analisado: robô atleta.
- Objetivo e hipóteses: uma tentativa de salto, com pista e altura da barra previamente informadas.
- P — Medida de desempenho: Passar sobre a barra sem derrubá-la e atingir a maior altura possível.
- E — Ambiente: Pista, barra, suportes e colchão de queda.
- A — Atuadores: Articulações e motores para correr, impulsionar e ajustar o corpo.
- S — Sensores: Câmeras, medidores de distância, acelerômetros e sensores articulares.

| Propriedade | Classificação | Justificativa |
|---|---|---|
| Observabilidade | Parcial | mede a barra, mas não percebe com precisão absoluta todas as condições do contato com o solo. |
| Número de agentes | Único | a tentativa não exige interação estratégica com outros atletas. |
| Previsibilidade | Estocástico na prática | pequenas diferenças na impulsão podem mudar o resultado. |
| Dependência entre decisões | Sequencial | corrida, impulso e postura precisam ser coordenados. |
| Mudança durante a decisão | Dinâmico durante o salto | a posição do robô muda enquanto ele controla o movimento. |
| Natureza dos elementos | Contínuos | velocidade, altura, ângulos e tempo. |
| Conhecimento do funcionamento | Conhecido | conhece regras, dimensões e princípios de movimento. |

### Caso 7 — Participar de um leilão de um item, realizando lances.

- Agente analisado: Agente de software comprador em leilão.
- Objetivo e hipóteses: Arrematar o item leiloado pelo menor preço possível, sem ultrapassar o valor máximo de avaliação privada.
- P — Medida de desempenho: Sucesso no arremate do item, maximização da margem de economia em relação ao limite e minimização de taxas.
- E — Ambiente: Plataforma de leilão, leiloeiro, licitantes concorrentes e histórico de lances do item.
- A — Atuadores: Envio digital de novo lance, confirmação de cobertura de oferta ou desistência do leilão.
- S — Sensores: Monitoramento de mensagens do leiloeiro, lances concorrentes atuais e cronômetro.

| Propriedade | Classificação | Justificativa |
| ------ | ------ | ------ |
| Observabilidade | Parcial | Os valores máximos e as estratégias privadas dos outros licitantes são informações ocultas. |
| Número de agentes | Multiagente (competitivo) | Outros licitantes competem diretamente para vencer o leilão, elevando os preços. |
| Previsibilidade | Estocástico | Os lances e comportamentos dos outros concorrentes não podem ser previstos com certeza. |
| Dependência entre decisões | Sequencial | Cada lance submetido altera o preço atual e condiciona as opções de lances futuros. |
| Mudança durante a decisão | Dinâmico | O cronômetro avança e outros licitantes podem enviar lances enquanto o agente analisa sua decisão. |
| Natureza dos elementos | Discreto | Os lances ocorrem em incrementos monetários discretos e em instantes de tempo discretos. |
| Conhecimento do funcionamento | Conhecido | As regras formais do leilão (incrementos mínimos e prazo de encerramento) são conhecidas \\(a\ priori\\). |

### Opções para classificação

- **Observabilidade:**  Completamente observável, parcialmente observável ou não observável.
- **Número de agentes:**  Agente único ou multiagente; indique cooperação ou competição quando pertinente.
- **Previsibilidade:**  Determinístico ou estocástico; considere a influência estratégica de outros agentes.
- **Dependência entre decisões:**  Episódico ou sequencial.
- **Mudança durante a decisão:**  Estático, dinâmico ou semidinâmico.
- **Natureza dos elementos:**  Discretos, contínuos ou combinação; considere estados, tempo, percepções e ações.
- **Conhecimento do funcionamento:**  Conhecido ou desconhecido para o agente.


### Comparação final

1. O que muda entre jogar tênis contra outra pessoa e praticar contra uma parede?
2. Por que comprar livros usados pode exigir decisões com informações incompletas?
3. Como outros agentes influenciam futebol e leilões?

Respostas:

1. No jogo contra outra pessoa, o ambiente é multiagente e competitivo, exigindo que o agente preveja e reaja às intenções e estratégias ativas do oponente. Contra a parede, o ambiente é de agente único, pois a parede é um objeto passivo regido unicamente pelas leis mecânicas da física, sem objetivos concorrentes.
2. Porque aspectos essenciais do ambiente — como o estado real de conservação física do livro (páginas grifadas, rasgos) e a idoneidade do vendedor — são parcialmente observáveis e não podem ser verificados com certeza antes do recebimento do produto.
3. No futebol, outros agentes geram necessidade de cooperação em tempo real com companheiros de equipe e antecipação competitiva para evitar desarmos dos adversários. No leilão, a presença de outros agentes concorrentes altera a medida de utilidade, pois cada lance efetuado por um rival força o agente a decidir entre elevar a oferta ou desistir para não ultrapassar seu orçamento limite.

## Exercício 2.5
Defina cada termo com suas palavras em duas a quatro linhas e apresente um exemplo.

### Agente

- Definição: algo que recebe informações do ambiente e consegue agir nele. Não precisa ser um robô físico; também pode ser um programa.
- Exemplo: um filtro de e-mail que identifica spam e move mensagens.

### Função de agente

- Definição: regra abstrata que indica qual ação corresponde a cada histórico possível de percepções.
- Exemplo: decidir entre continuar ou parar com base nas leituras acumuladas de temperatura.

### Programa de agente

- Definição: código que coloca essa tomada de decisão em funcionamento em um equipamento. Recebe dados atuais e pode consultar a memória.
- Exemplo: software de um termostato que liga o ar-condicionado.

### Racionalidade

- Definição: escolher a ação com melhor resultado esperado a partir das informações disponíveis. Não é acertar sempre.
- Exemplo: diminuir a velocidade quando a pista parece escorregadia.

### Autonomia

- Definição: capacidade de ajustar o comportamento usando experiências próprias em vez de depender apenas de regras fixas.
- Exemplo: aplicativo que aprende os horários em que o usuário costuma sair.

### Agente reativo

- Definição: responde ao que percebe agora, sem precisar lembrar de situações anteriores.
- Exemplo: porta automática que abre ao detectar alguém perto.

### Agente baseado em modelo

- Definição: guarda uma representação do ambiente para lidar com coisas que não consegue enxergar naquele momento.
- Exemplo: robô que lembra onde encontrou um obstáculo.

### Agente baseado em objetivos

- Definição: escolhe ações pensando em chegar a uma situação desejada.
- Exemplo: navegador que procura um caminho até o destino.

### Agente baseado em utilidade

- Definição: compara alternativas considerando qual oferece o melhor equilíbrio de benefícios e custos.
- Exemplo: sistema que escolhe uma rota levando em conta duração, pedágios e segurança.

### Agente com aprendizagem

- Definição: melhora suas decisões depois de observar resultados e receber avaliações.
- Exemplo: recomendador de músicas que adapta sugestões conforme as escolhas do ouvinte.

## Síntese com autômatos
Escolha um caso do item 2.4. Apresente três estados internos, três percepções, três ações e duas regras no formato estado atual + percepção → próximo estado e ação. Explique como estados internos representam informação passada e cite uma limitação da simplificação.

Resposta: 

**Caso escolhido:** compra de livros usados pela internet. Vamos simplificar o comprador automático como uma máquina com três estados.

**Estados internos:**
- `q0 — Pesquisando`: ainda procura ofertas.
- `q1 — Avaliando`: encontrou uma opção e está verificando preço e condições.
- `q2 — Finalizado`: compra realizada ou busca encerrada.

**Percepções:** `p1 — anúncio encontrado`; `p2 — oferta atende aos critérios`; `p3 — orçamento insuficiente`.

**Ações:** `a1 — abrir detalhes do anúncio`; `a2 — efetuar compra`; `a3 — descartar oferta`.

**Três regras de transição:**

```text
q0 + p1 → q1 e a1
q1 + p2 → q2 e a2
q1 + p3 → q0 e a3
```

**O que a memória representa?** O estado `q1` mostra que o sistema já encontrou um anúncio e passou da etapa de pesquisa para a avaliação. Assim, ele não precisa tratar cada informação como se fosse a primeira.

**Limitação:** três estados não representam bem situações reais, como comparação de vários vendedores, frete variável, fraude ou falha no pagamento. Seria necessário um modelo mais detalhado.

## Entrega e avaliação
Confira: identificação; nove análises no item 2.3; sete casos completos no item 2.4; dez conceitos no item 2.5; síntese; referências.
Nome sugerido: `NomeSobrenome_Atividade_AgentesInteligentes`. Prazo e envio conforme orientação da professora.

| Critério | Atividade avaliativa (1,0 ponto) A2 |
|---|---:|
| Item 2.3 — correção e argumentação | 30% |
| Item 2.4 — PEAS e classificação justificada | 40% |
| Item 2.5 — precisão conceitual e exemplos | 20% |
| Síntese, organização e referências | 10% |

## Referências
Material-base: Capítulo 2 — Agentes inteligentes, disponibilizado para a aula de 19/10/2026.

Referências adicionais: RUSSELL, Stuart; NORVIG, Peter. *Inteligência Artificial*. 3. ed. Rio de Janeiro: Elsevier, 2013. Capítulo 2.
