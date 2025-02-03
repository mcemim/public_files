---
title: markmap
markmap:
  colorFreezeLevel: 2
  initialExpandLevel: 2
  embedAssets: true
  maxWidth: 350
---


# **==Metodologia CRISP-DM==**<br>*A metodologia CRISP-DM (Cross-Industry Standard Process for Data Mining) é um modelo amplamente utilizado para guiar projetos de mineração de dados. Este documento apresenta uma visão geral das etapas do CRISP-DM, os entregáveis esperados em cada fase e as questões que devem ser respondidas para garantir a eficácia do processo. Através dessa abordagem estruturada, é possível maximizar o valor dos dados e obter insights significativos.*

## 1. Entendimento do Negócio
### *A primeira etapa tem como objetivo garantir que todos os envolvidos compreendam claramente o contexto e as necessidades do negócio antes de iniciar qualquer trabalho de mineração de dados. Cada subetapa dentro desse processo ajuda a responder perguntas específicas, permitindo alinhar os objetivos de negócio com os objetivos de mineração de dados.*

### **Questões a serem respondidas**
- 1.1.1. Qual é o contexto do negócio, e quais são os fatores que motivam esse projeto? O que o cliente pretende alcançar com esse projeto? Qual é o problema que estamos tentando resolver? Como saberemos que atingimos os objetivos de negócio? Quais métricas indicam sucesso?
- 1.1.2. Quais recursos estão disponíveis (dados, equipe, ferramentas, tempo)? Quais são as expectativas e limitações do projeto? Quais restrições de tempo, orçamento ou regulatórias existem?
- 1.1.3. Quais são os termos técnicos ou de negócio que precisam ser definidos para evitar mal-entendidos?
- 1.1.4. Qual conhecimento ou informação o modelo deve gerar? É um modelo de classificação, regressão, geração de conteúdo, classificação de imagem, …?
- 1.1.5. Qual o impacto de um erro na resposta do modelo? 
- 1.1.6. Como mediremos o sucesso técnico do projeto? Quais métricas de desempenho ou acurácia serão usadas?
- 1.1.7. Qual é o plano para realizar o projeto? Quais são as fases, cronograma e entregáveis?
- 1.1.8. Quais ferramentas e técnicas são adequadas para esse projeto? Temos acesso a todas as ferramentas necessárias?

### **Entregas & Formatos**
- 1.2.1. Documento de texto (.md)
    - Descrição os objetivos de negócio, critérios de sucesso, restrições e benefícios, além de inventário de recursos, restrições, riscos, terminologia, critérios de sucesso, ferramentas, bibliotecas e técnicas possíveis. 
- 1.2.2. Repositório no azure-devops
    - Contendo o `readme.md` para registrar essas informações.
- 1.2.3. Repositório no sharepoints 
    - Contendo estrutura para armazenamento dos dados crus e limpos.

## 2. Entendimento dos Dados
### *Na segunda etapa, o foco é obter uma compreensão clara dos dados disponíveis, suas características, qualidade e relevância para o projeto. As subetapas dessa fase ajudam a responder perguntas práticas que garantem que os dados sejam adequados para alcançar os objetivos do projeto.*

### **Questões a serem respondidas**
- 2.2.1. Quais dados estão disponíveis para o projeto? Onde esses dados estão armazenados?
- 2.2.2. Quais são as principais características dos dados? Quais variáveis estão disponíveis, e como estão estruturadas?
- 2.2.3. Quais padrões iniciais podem ser observados nos dados? Existem relações, distribuições ou anomalias notáveis?
- 2.2.4. Os dados estão completos, corretos e consistentes? Existem valores ausentes ou duplicados? Quais são os possíveis problemas de qualidade que precisam ser tratados?

### **Entregas & Formatos**
- 2.2.1. Notebook Python (.ipynb)
    - Scripts para extrair e carregar os dados, contendo informações com detalhes sobre as fontes, formatos e volumes dos dados.
    - A estrutura dos dados, contendo análise de colunas e tipos de dados
    - Gráficos de dispersão, histogramas, boxplots, e correlações para explorar relações entre variáveis.
    - Diagnóstico de qualidade de dados, para identificar valores ausentes, duplicados, outliers, e inconsistências.

## 3. Preparação dos Dados
### *Na terceira fase o objetivo é transformar os dados brutos em um formato adequado para a modelagem. Esta etapa envolve diversas tarefas de limpeza, transformação e formatação dos dados, essenciais para garantir que o modelo de mineração de dados possa ser criado corretamente.*

### **Questões a serem respondidas**
- 3.1.1. Quais dados ou atributos são mais relevantes para o modelo? Os atributos podem ser selecionados com base na experiência / teoria ou utilizando técnicas como análise de correlação ou algoritmos de seleção de características.
- 3.1.2. Como lidar com dados ausentes, inconsistências ou valores incorretos?
- 3.1.3. Precisamos criar ou transformar variáveis adicionais para o modelo? Se sim, quais, como e qual a razão para tal?
- 3.1.4. Como combinar dados de diferentes fontes em um único dataset? Quais são as chaves de ligação entre as diferentes bases? 
- 3.1.5. Como formatar os dados para que estejam prontos para a modelagem, em termos de padronização, formatação, encoding, agrupamento de classes… ? 

### **Entregas & Formatos**
- 3.2.1. Notebook Python (.ipynb)
    - Seleção de variáveis e justificativa em comentários.  
    - Estratégias para tratar dados ausentes e inconsistentes, com relatório comparativo pré e pós-limpeza. 
    - Geração novas features, com documentação das novas variáveis criadas. 
    - Integração de diferentes fontes de dados, com documentação explicativa.   
    - Notebook ou script com o dataset final pronto para modelagem, exportado em formato .csv ou similar.    ==DEFINIR==



## 4. Modelagem
### *A etapa de modelagem é onde são escolhidas as técnicas apropriadas e os dados preparados são utilizados para construir o(s) modelo(s). É importante selecionar as técnicas corretas e ajustar seus parâmetros de acordo com os dados disponíveis. Também é essencial comparar diferentes modelos e métodos para garantir que o modelo escolhido atenda aos objetivos do projeto.*

### **Questões a serem respondidas**
- 4.1.1. Quais técnicas de modelagem são mais adequadas para o problema? O problema requer técnicas de classificação, regressão, clusterização, ou outra abordagem?
- 4.1.2. Como os dados precisam ser preparados para essas técnicas? Existem exigências específicas como normalização, balanceamento de classes, ou criação de conjuntos de validação e teste?
- 4.1.3. Quais parâmetros dos modelos devem ser ajustados (hiperparâmetros)? Para cada modelo, quais hiperparâmetros precisam ser ajustados? Exemplo: número de árvores para um Random Forest, taxa de aprendizado para uma rede neural, etc.
- 4.1.4. Como dividimos os dados para treinamento e validação? Qual será a divisão entre treino, validação e teste (ex: 70/15/15)? Utilizamos cross-validation ou holdout?
- 4.1.5. Como avaliar o desempenho dos modelos? Quais métricas de avaliação são relevantes para o projeto? Exemplos: acurácia, precisão, recall, F1-score, AUC-ROC, RMSE, etc.
- 4.1.6. Os modelos atendem aos objetivos do projeto? O modelo é adequado para os requisitos de negócio estabelecidos? Há necessidade de refinamento ou ajustes?

### **Entregas & Formatos**
- 4.2.1. Notebooks Python (.ipynb)
    - Implementação dos modelos selecionados. 
    - Scripts para treinamento e avaliação dos modelos
    - Ajuste de hiperparâmetros, utilizando técnicas de busca em grade (GridSearchCV), busca aleatória (RandomizedSearchCV), ou Bayesian Optimization.
    - Métricas de avaliação 
        - Acurácia, precisão, recall, F1-score, curva ROC/AUC (para classificação).
        - MAPE, R², RMSE, MAE (para regressão).
        - Silhouette score, inertia (para clusterização).
    - Gráficos de avaliação
        - Matriz de confusão.
        - Curva ROC.
        - Plotagem de resíduos (regressão).
        - Gráficos de clusters (clusterização).
- 4.2.2. Salvamento do(s) modelo(s) final(is) em formato adequado para implementação futura:
    - Usar formato joblib ou pickle ==DEFINIR== para salvar os modelos treinados.
    - Salvar o modelo e seus parâmetros de ajuste para facilitar a reusabilidade.

## 5. Avaliação
### *Após a modelagem, a fase de avaliação tem como objetivo revisar e interpretar os resultados dos modelos criados para garantir que eles atendem às expectativas do projeto e os objetivos de negócio. Nesta fase, os resultados dos modelos são analisados mais profundamente, e decisões são tomadas sobre a viabilidade do modelo para a implementação.*

### **Questões a serem respondidas**
- 5.1.1. O modelo atende aos objetivos de negócio definidos? O desempenho do modelo está alinhado com os critérios estabelecidos na fase de entendimento do negócio? Como os resultados do modelo impactam o problema de negócio que estamos tentando resolver?
- 5.1.2. Quais são as limitações do modelo? Quais problemas, incertezas ou falhas foram observados no desempenho do modelo? Há viés ou variância elevada em algum modelo? Existe algum erro significativo nos dados que afeta o desempenho?
- 5.1.3. Como os resultados do modelo são interpretados pelo negócio? Os resultados do modelo são compreensíveis e acionáveis para os stakeholders? É possível explicar as previsões ou classificações do modelo de forma clara para as partes interessadas?
- 5.1.4. Qual é o nível de confiança nos resultados? Quais são os limites de confiança ou margem de erro nos resultados do modelo? Como os resultados variam conforme os diferentes cenários de validação e teste?
- 5.1.5. Qual é o plano de ação com base na avaliação? O modelo está pronto para ser implementado ou precisa de refinamento adicional? Existe necessidade de coleta de mais dados ou ajustes no pré-processamento?

### **Entregas & Formatos**
- 5.2.1. Relatório de Avaliação do Modelo (.md ou .pdf)
    - Interpretação dos resultados
        - Gráficos de importância das variáveis (ex.: Feature Importance no Random Forest)
        - Gráficos de erro e de performance para inspeção visual das previsões.*
        - Interpretação de modelos "caixa-preta" (ex.: uso de técnicas como SHAP ou LIME para interpretar redes neurais ou outros modelos complexos).
    - Resumo do desempenho de cada modelo, com foco nos melhores resultados.
        - Qual modelo performou melhor e por quê.
        - Comparação clara entre os modelos com tabelas e gráficos que mostrem as diferenças de performance.
        - Destaque das fraquezas e limitações dos modelos testados.
        - Justificativas para a escolha do modelo final.
    - Análise de viabilidade do modelo
        - O quão bem o modelo atende aos objetivos de negócio.
        - Justificativas para continuar com o modelo ou realizar ajustes adicionais.
        - Potenciais riscos associados à implementação do modelo.
- 5.2.2. Recomendações para a próxima fase - Detalhamento de ações futuras com base nos resultados
    - Refazer alguma parte do pré-processamento ou modelagem?
    - Testar outros algoritmos ou ajustar hiperparâmetros?
    - Implementar o modelo ou realizar testes adicionais?
- 5.2.3. Plano de ação pós-avaliação
    - Se o modelo for considerado adequado, fornecer um plano claro para a implementação e monitoramento do modelo.
    - Caso o modelo precise de ajustes, detalhar quais partes do pipeline precisam de revisão (ex.: coleta de novos dados, seleção de outras features).

## 6. Implementação
### *Na etapa de implementação, o modelo que foi avaliado e validado é colocado em uso no ambiente de produção (VIRIDIS). Além disso, é crucial planejar o monitoramento contínuo e a manutenção do modelo para garantir que ele continue a gerar valor ao longo do tempo.*

### **Questões a serem respondidas**
- 6.1.1. O modelo será integrado a um sistema existente ou será utilizado de forma independente?
- 6.1.2. Como os dados reais serão processados e ingeridos pelo modelo em produção?
- 6.1.3. Como garantir a escalabilidade e a robustez do modelo em produção? O modelo precisa lidar com grandes volumes de dados em tempo real ou em batch? Como ele será escalado?
- 6.1.4. Como será feito o monitoramento do desempenho do modelo em produção? Quais métricas serão monitoradas para garantir que o modelo mantenha seu desempenho ao longo do tempo (ex.: monitoramento de acurácia, latência, uso de recursos)?
- 6.1.5. Quais são os procedimentos para lidar com falhas ou degradação do modelo? Como o sistema reagirá se o modelo começar a apresentar problemas (ex.: alertas, fallback para um modelo mais simples ou regras manuais)?
- 6.1.6. Que documentação deve ser fornecida para garantir que os usuários e administradores saibam como utilizar, monitorar e manter o modelo?

### **Entregas & Formatos**
- 6.2.1. Código e scripts de implementação:
- 6.2.2. Monitoramento e manutenção:
    - Logs e alertas automáticos para identificar anomalias no desempenho ou falhas do modelo.
    - Instruções sobre quais métricas monitorar, como acurácia, desempenho em tempo real, latência, e consumo de recursos.
    - Procedimentos para reagir a alertas ou problemas detectados.
- 6.2.3. Plano de contingência
    - Plano para retornar a uma versão anterior do modelo ou desativar o modelo em caso de falhas graves.
    - Implementação de regras manuais ou modelos mais simples caso o modelo principal falhe.

## 7. Manutenção
### *A etapa de manutenção visa garantir que o modelo continue a fornecer resultados precisos e úteis ao longo do tempo. Isso envolve o monitoramento contínuo do desempenho do modelo, ajustes para melhorar a acurácia ou eficiência, e a atualização do modelo para refletir mudanças nos dados ou no ambiente do negócio.*

### **Questões a serem respondidas**
- 7.1.1. Como garantir que o modelo continue a ser eficaz ao longo do tempo? Como será feito o monitoramento contínuo do desempenho do modelo? O modelo está se degradando devido a mudanças nos dados ou no ambiente de produção?
- 7.1.2. Quais são os procedimentos para atualização ou re-treinamento do modelo? Com que frequência o modelo precisará ser re-treinado? Existem sinais claros que indicam a necessidade de re-treinamento (ex.: queda de acurácia, introdução de novas features nos dados)?
- 7.1.3. Como será garantida a integridade dos dados e a eficiência do modelo? Quais medidas serão adotadas para manter a integridade e a qualidade dos dados que alimentam o modelo? O modelo será ajustado de acordo com novas variáveis ou novas versões dos dados?
- 7.1.4. Como monitorar o impacto das mudanças no negócio? Como o modelo será adaptado se o contexto ou os requisitos de negócios mudarem significativamente (ex.: novas regulamentações, mudanças nos processos)?
- 7.1.5. Quais métricas serão utilizadas para monitorar o desempenho do modelo? Como métricas de acurácia, precisão, recall, F1-score, entre outras, serão monitoradas regularmente? Como será feito o acompanhamento de métricas de desempenho operacional, como tempo de resposta, uso de recursos, ou taxas de erro?
- 7.1.6. Quais são os planos para ajuste e manutenção contínua? Existem processos automáticos ou manuais para realizar ajustes menores no modelo, como recalibração de hiperparâmetros? Como será documentado o histórico de ajustes e melhorias realizadas no modelo?

### **Entregas & Formatos**
- 7.2.1. Manual de manutenção do modelo (.md ou .pdf)
    - Procedimentos para o monitoramento contínuo do desempenho e alertas.
    - Plano de ação para correção de problemas e re-treinamento.
    - Instruções para ajustes de hiperparâmetros e reconfiguração do modelo conforme necessário.
- 7.2.2. Log de ajustes e atualizações
    - Relatório de alterações realizadas no modelo ao longo do tempo, incluindo motivos e impacto esperado de cada mudança.
- 7.2.3. Implementação de métricas de monitoramento
    - Configuração de dashboards de monitoramento que acompanham o desempenho preditivo do modelo e a qualidade dos dados em tempo real.
    - Ferramentas para capturar e exibir métricas como precisão, recall, tempo de inferência, uso de memória e CPU.
- 7.2.4. Relatórios periódicos de desempenho (.md ou .pdf)
    - Relatórios automatizados ou manuais gerados periodicamente (ex.: semanalmente, mensalmente) com uma análise das principais métricas de desempenho e alertas para possíveis degradações.
- 7.2.5. Plano de re-treinamento do modelo
    - Scripts para re-treinamento automático ou manual:
        - Scripts Python (.py ou .ipynb) que permitem o re-treinamento automático do modelo em períodos definidos ou após a detecção de mudanças significativas nos dados.
        - Instruções claras sobre como executar o re-treinamento e validar o novo modelo antes de colocá-lo em produção.
    - Documentação sobre o ciclo de vida do modelo:
        - Plano que documenta a frequência de re-treinamento e os triggers que indicam a necessidade de reavaliar o modelo.
    - Comparação de versões do modelo:
        - Arquivo detalhando as versões anteriores e atuais do modelo, com comparações de desempenho, precisão e outras métricas relevantes.
- 7.2.6. Gerenciamento de mudanças
    - Logs de alterações no código e no modelo, garantindo que todas as modificações e ajustes sejam rastreados, possibilitando reversões, se necessário.
- 7.2.7. Plano de rollback
    - Procedimentos para desfazer mudanças no modelo ou retornar a uma versão anterior se novos problemas forem detectados após atualizações.
