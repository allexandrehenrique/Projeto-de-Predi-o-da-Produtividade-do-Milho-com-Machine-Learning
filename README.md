### Projeto de Predição da Produtividade do Milho com Machine Learning

## 1. Introdução

A capacidade de prever a produtividade agrícola é um fator crítico para a sustentabilidade e eficiência do setor. No contexto da cultura do milho, a antecipação da produtividade permite um planejamento mais eficaz de recursos, otimização de insumos e mitigação de riscos associados a fatores ambientais e de manejo. Este relatório técnico detalha um projeto que emprega técnicas de Machine Learning para desenvolver um modelo preditivo da produtividade do milho, com base em variáveis agronômicas e climáticas.

## 2. Descrição do Projeto

## 2.1. Problema de Negócio

O problema de negócio central abordado é a predição da produtividade do milho. A acurácia na previsão da produtividade é fundamental para o planejamento estratégico de agricultores, cooperativas e demais stakeholders da cadeia produtiva, influenciando decisões sobre plantio, colheita, comercialização e gestão de riscos.

## 2.2. Contexto

O projeto foi desenvolvido utilizando um conjunto de dados sintéticos, gerados para simular as interações entre diversas variáveis agronômicas e climáticas e a produtividade do milho. As variáveis incluídas são pH do solo, matéria orgânica do solo (MO_solo), nitrogênio foliar (N_foliar), fósforo no solo (P_solo), potássio no solo (K_solo), chuva acumulada, temperatura média e dose de fertilizante organomineral. A produtividade foi calculada por uma função que combina esses fatores, com a adição de ruído para mimetizar a variabilidade inerente aos sistemas biológicos. Este ambiente controlado permite o desenvolvimento e a validação de um modelo preditivo em um cenário simulado, antes de sua aplicação em dados reais de campo.

## 2.3. Premissas da Análise

As premissas que fundamentam este estudo são:

• Representatividade dos Dados: Assume-se que o conjunto de dados sintéticos, apesar de sua natureza artificial, captura as relações essenciais e a complexidade entre as variáveis de entrada e a produtividade do milho. Em aplicações reais, a validação com dados de campo seria indispensável.

• Qualidade dos Dados: Presume-se que os dados utilizados estão livres de valores ausentes significativos ou anomalias que possam distorcer os resultados da análise e a performance do modelo.

• Adequação do Modelo de Regressão: A escolha do algoritmo RandomForestRegressor baseia-se na sua robustez e capacidade de modelar relações não lineares e interações complexas entre variáveis, sendo considerado apropriado para o problema de predição de produtividade.

• Divisão dos Dados: A proporção de 80% para treinamento e 20% para teste (test_size=0.2) é adotada como uma prática padrão para garantir uma avaliação imparcial do desempenho do modelo.

## 2.4. Estratégia da Solução

A estratégia para solucionar o problema de predição da produtividade do milho envolve a aplicação de técnicas de machine learning para regressão, seguindo os passos:

1. Geração de Dados: Criação de um dataset sintético com 500 amostras, compreendendo 8 variáveis preditoras e a variável alvo (produtividade).

2. Análise Exploratória de Dados (EDA): Realização de análises visuais para compreender a distribuição da produtividade e as correlações entre as variáveis.

3. Pré-processamento: Divisão do dataset em conjuntos de treinamento e teste para o desenvolvimento e avaliação do modelo.

4. Modelagem: Construção de um modelo preditivo utilizando o algoritmo RandomForestRegressor.

5. Avaliação do Modelo: Quantificação do desempenho do modelo por meio de métricas como R² (coeficiente de determinação), RMSE (raiz do erro quadrático médio) e MAE (erro médio absoluto).

6. Análise de Importância de Variáveis: Identificação das variáveis que exercem maior influência na predição da produtividade, fornecendo insights agronômicos valiosos.

## 2.5. Metodologia de Análise (Passos 1-7)

Para guiar a análise e o desenvolvimento do projeto, foi adotada uma metodologia estruturada em sete passos:

## 2.5.1. Passo 1: Resumir o contexto em uma pergunta aberta

Qual a relação entre as variáveis agronômicas (pH do solo, matéria orgânica, nitrogênio foliar, fósforo, potássio, chuva, temperatura média, dose de fertilizante organomineral) e a produtividade do milho, e como essas relações podem ser utilizadas para prever a produtividade?

## 2.5.2. Passo 2: Transformar pergunta aberta em fechada

É possível prever a produtividade do milho com base em variáveis agronômicas utilizando um modelo de machine learning, e quais são as variáveis mais influentes nessa predição?

## 2.5.3. Passo 3: Definição da Coluna Fato

A Coluna Fato para este projeto é a produtividade (sacas/ha), representando a variável alvo que o modelo busca prever.

## 2.5.4. Passo 4: Identificação das Dimensões

As Dimensões ou variáveis preditoras que influenciam a produtividade são:

• pH_solo: Medida da acidez ou alcalinidade do solo.

• MO_solo: Percentual de matéria orgânica presente no solo.

• N_foliar: Teor de nitrogênio nas folhas da planta.

• P_solo: Concentração de fósforo disponível no solo.

• K_solo: Concentração de potássio disponível no solo.

• chuva: Volume de chuva acumulada (em mm).

• temp_media: Temperatura média do ambiente (em °C).

• dose_fert_organomineral: Quantidade de fertilizante organomineral aplicado (em kg/ha).

## 2.5.5. Passo 5: Hipóteses Analíticas

Foram formuladas as seguintes hipóteses para guiar a análise:

1. Hipótese 1: Variáveis relacionadas à fertilidade do solo (pH, MO, N, P, K) apresentarão uma correlação significativa com a produtividade do milho.

2. Hipótese 2: Condições climáticas, como chuva e temperatura média, serão fatores determinantes na produtividade.

3. Hipótese 3: A aplicação de fertilizante organomineral demonstrará um impacto positivo na produtividade.

4. Hipótese 4: Um modelo baseado em Random Forest será capaz de capturar as relações complexas entre as variáveis e atingir uma acurácia preditiva razoável (R² > 0.5).

## 2.5.6. Passo 6: Critérios de Priorização

Os critérios utilizados para priorizar as hipóteses analíticas incluem:

• Relevância Agronômica: O impacto direto e prático na gestão agrícola.

• Disponibilidade de Dados: A facilidade de obtenção das variáveis em cenários de aplicação real.

• Potencial de Impacto: A capacidade da hipótese de gerar insights que otimizem a produtividade e influenciem decisões.

• Complexidade da Análise: A viabilidade técnica de testar a hipótese com os recursos e dados disponíveis.

## 2.5.7. Passo 7: Priorização das Hipóteses Analíticas

Todas as hipóteses foram consideradas relevantes para a fase inicial do projeto. Contudo, a Hipótese 4, referente ao desempenho do modelo de machine learning, é a mais crítica para validar a abordagem metodológica. As demais hipóteses (1, 2 e 3) são exploradas e validadas através da análise de correlação e da importância das variáveis no modelo, fornecendo insights sobre os fatores agronômicos mais influentes.

## 3. Análise e Interpretação dos Gráficos

Esta seção apresenta a interpretação detalhada dos gráficos gerados durante a fase de Análise Exploratória de Dados (EDA) e avaliação do modelo, fornecendo insights cruciais sobre as relações entre as variáveis e a performance do modelo preditivo.

## 3.1. Correlação entre variáveis











O mapa de calor de correlação ilustra a intensidade e direção das relações lineares entre todas as variáveis do dataset. Os valores variam de -1 (correlação negativa perfeita) a 1 (correlação positiva perfeita), com 0 indicando ausência de correlação linear. Cores mais escuras (azul marinho) denotam correlações mais fortes, enquanto cores mais claras (amarelo) indicam correlações mais fracas.

Justificativa:

• Produtividade e Chuva (0.45): Observa-se uma correlação positiva moderada entre a chuva acumulada e a produtividade. Este achado é agronomicamente consistente, pois a disponibilidade hídrica é um dos principais fatores limitantes para o desenvolvimento do milho, e volumes adequados de chuva são essenciais para altas produtividades.

• Produtividade e MO_solo (0.37): A matéria orgânica do solo exibe uma correlação positiva moderada com a produtividade. Solos ricos em matéria orgânica tendem a apresentar melhor estrutura, maior capacidade de retenção de água e nutrientes, e maior atividade microbiana, fatores que promovem o crescimento vigoroso das plantas.

• Produtividade e P_solo (0.29): O fósforo disponível no solo demonstra uma correlação positiva fraca a moderada. O fósforo é vital para o estabelecimento inicial da cultura, desenvolvimento radicular e processos energéticos, impactando diretamente a produtividade.

• Produtividade e dose_fert_organomineral (0.25): A dose de fertilizante organomineral apresenta uma correlação positiva fraca a moderada. Isso sugere que a aplicação deste insumo contribui para o aumento da produtividade, validando a importância de um manejo nutricional adequado.

• Produtividade e N_foliar (0.16): O nitrogênio foliar mostra uma correlação positiva fraca. Embora o nitrogênio seja o nutriente mais demandado pelo milho, sua correlação linear direta pode ser atenuada por outros fatores ou pela faixa de variação nos dados sintéticos.

• Produtividade e K_solo (0.13): O potássio no solo também exibe uma correlação positiva fraca. O potássio é crucial para a regulação hídrica, resistência a doenças e enchimento de grãos.

• Produtividade e pH_solo (0.01): O pH do solo apresenta uma correlação muito baixa com a produtividade. Isso pode indicar que, dentro da faixa de pH simulada, este fator não foi o principal limitante ou que sua influência é mais complexa e não linear, não sendo bem capturada por uma análise de correlação simples.

• Produtividade e temp_media (0.02): A temperatura média também exibe uma correlação muito baixa. Similar ao pH, a temperatura pode ter um efeito mais complexo e não linear na produtividade, onde tanto temperaturas muito baixas quanto muito altas podem ser prejudiciais, e uma faixa ótima é necessária. A correlação linear simples pode não refletir essa complexidade.

Em síntese, a análise de correlação destaca a chuva e a matéria orgânica do solo como os fatores mais fortemente e linearmente associados à produtividade do milho neste conjunto de dados, seguidos por fósforo e fertilizante organomineral.

## 3.2. Distribuição da Produtividade (sacas/ha)











O histograma, sobreposto por uma curva de Estimativa de Densidade de Kernel (KDE), ilustra a distribuição de frequência da produtividade do milho em sacas por hectare. O eixo horizontal representa os valores de produtividade, e o eixo vertical indica a contagem de ocorrências para cada intervalo de produtividade.

Justificativa:

• Formato da Distribuição: A distribuição da produtividade se aproxima de uma distribuição normal (gaussiana), caracterizada por sua forma de sino e simetria em torno da média. A curva KDE suaviza o histograma, confirmando essa tendência.

• Média e Moda: O pico da distribuição, que corresponde à moda e se alinha com a média, está concentrado em torno de 65 sacas/ha. Isso indica que a maioria das observações de produtividade no dataset se agrupa em torno desse valor central.

• Amplitude e Variabilidade: A produtividade varia aproximadamente de 35 a 95 sacas/ha, demonstrando a amplitude dos resultados simulados. A concentração dos dados em torno da média sugere que valores extremos de produtividade são menos frequentes, o que é comum em dados biológicos e agronômicos.

• Implicações para Modelagem: Uma distribuição aproximadamente normal é um atributo desejável para muitos algoritmos de machine learning, pois pode facilitar a convergência e melhorar a performance preditiva. Esta visualização é fundamental para compreender o comportamento geral da variável alvo e a variabilidade intrínseca da produtividade do milho.

## 3.3. Importância das Variáveis no Modelo











Este gráfico de barras horizontais quantifica a importância relativa de cada variável preditora na determinação da produtividade do milho, conforme avaliado pelo modelo RandomForestRegressor. O eixo horizontal representa o score de importância (normalizado, somando 1 para todas as variáveis), e o eixo vertical lista as variáveis em ordem decrescente de importância.

Justificativa:

• Variáveis Climáticas Dominantes: A chuva e a temperatura média emergem como as variáveis mais importantes para o modelo, com a chuva apresentando a maior contribuição. Este resultado sublinha a preponderância dos fatores climáticos na definição da produtividade do milho, um fato bem estabelecido na agronomia. A temperatura média, embora com baixa correlação linear, revela-se crucial no modelo de Random Forest, indicando interações complexas com outras variáveis.

• Fatores de Solo e Nutrição: A matéria orgânica do solo (MO_solo) e o fósforo no solo (P_solo) seguem em importância, reforçando a relevância da qualidade do solo e da disponibilidade de nutrientes. A dose de fertilizante organomineral também se mostra um contribuinte significativo, validando a importância do manejo nutricional.

• Variáveis de Menor Impacto: O potássio no solo (K_solo), o nitrogênio foliar (N_foliar) e o pH do solo (pH_solo) são as variáveis com menor importância relativa no modelo. Embora sejam fatores agronômicos relevantes, o modelo atribuiu-lhes um peso preditivo menor neste dataset simulado, o que pode ser atribuído à sua menor variabilidade ou a interações mais sutis que o modelo não priorizou.

• Consistência e Complementaridade: Há uma consistência entre a análise de correlação e a importância das variáveis, especialmente para chuva e MO_solo. A importância elevada da temperatura média no modelo, apesar de sua baixa correlação linear, destaca a capacidade do Random Forest de capturar relações não lineares e interações entre as variáveis, fornecendo uma visão mais completa dos fatores preditivos.

Este gráfico é uma ferramenta valiosa para direcionar pesquisas futuras e estratégias de manejo, indicando quais variáveis devem ser monitoradas com maior atenção para otimizar a produtividade do milho.

## 4. Resultados e Conclusões

## 4.1. Insights da Análise

A análise exploratória e a modelagem preditiva revelaram insights importantes sobre os fatores que influenciam a produtividade do milho:

• Fatores Climáticos são Predominantes: A chuva e a temperatura média são as variáveis mais críticas para a predição da produtividade, conforme evidenciado pela análise de importância das variáveis no modelo. Isso reforça a necessidade de monitoramento climático rigoroso e estratégias de manejo adaptadas às condições meteorológicas.

• Qualidade do Solo é Fundamental: A matéria orgânica do solo e o fósforo no solo demonstraram ser fatores importantes, tanto na análise de correlação quanto na importância do modelo. Isso sublinha a relevância de práticas de manejo que visem à melhoria da fertilidade e estrutura do solo.

• Manejo Nutricional Otimizado: A dose de fertilizante organomineral também se mostrou um preditor relevante, indicando que a adubação é um componente chave para maximizar a produtividade.

• Distribuição da Produtividade: A produtividade do milho no dataset simulado segue uma distribuição aproximadamente normal, com a maioria dos valores concentrados em torno de 65 sacas/ha, o que é um comportamento esperado para fenômenos agronômicos.

## 4.2. Resultados do Modelo Preditivo

O modelo RandomForestRegressor foi avaliado utilizando as seguintes métricas:

• R² (Coeficiente de Determinação): 0.5963

• RMSE (Raiz do Erro Quadrático Médio): 6.0278

• MAE (Erro Médio Absoluto): 4.7989

O valor de R² de aproximadamente 0.60 indica que o modelo consegue explicar cerca de 60% da variância na produtividade do milho. Embora não seja um R² extremamente alto, é um resultado razoável para um modelo preditivo em um contexto agrícola, onde a variabilidade é inerente e muitos fatores não controláveis podem influenciar a produtividade. O RMSE de 6.03 sacas/ha e o MAE de 4.80 sacas/ha indicam que, em média, as previsões do modelo desviam-se da produtividade real em aproximadamente 5 a 6 sacas por hectare. Estes valores são aceitáveis para um modelo inicial e sugerem que o modelo tem um bom potencial para auxiliar na tomada de decisões.

## 4.3. Conclusões

Este projeto demonstrou a viabilidade da aplicação de machine learning para a predição da produtividade do milho com base em variáveis agronômicas e climáticas. O modelo RandomForestRegressor desenvolvido apresentou um desempenho satisfatório, identificando a chuva e a temperatura média como os fatores mais influentes, seguidos pela matéria orgânica e fósforo do solo, e pela dose de fertilizante organomineral. Os insights gerados podem ser utilizados para otimizar o manejo agrícola, direcionar a pesquisa e desenvolver estratégias mais eficientes para o aumento da produtividade do milho.

Para futuras etapas, recomenda-se a validação do modelo com dados reais de campo, a exploração de outras variáveis (como genótipo do milho, tipo de solo, histórico de manejo) e a investigação de modelos mais complexos ou ensembles para aprimorar a acurácia preditiva. A integração deste tipo de ferramenta em sistemas de apoio à decisão pode trazer benefícios significativos para a agricultura de precisão.

