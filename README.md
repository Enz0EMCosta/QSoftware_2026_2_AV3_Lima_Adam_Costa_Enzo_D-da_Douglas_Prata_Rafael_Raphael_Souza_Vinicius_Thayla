# Atividade 3 — Qualidade de Software

Esqueleto do repositório da Atividade 3 da disciplina de Qualidade de Software (UFS); preencher os campos indicados sem incluir dados pessoais ou credenciais.

## Resumo

Esta atividade documenta uma comparação exploratória entre respostas do fluxo de Base de Conhecimento do Cherry Studio. Foram transcritas seis respostas A e seis B em 11/11/2026; quatro capturas parciais estão arquivadas. O estudante informou posteriormente prompts de sistema diferentes para A e B, sem evidência visual da configuração. R1 reportou 6/6 aprovações por versão; R2 reportou concordância em 4/4 revisões selecionadas, com justificativa geral “Respostas Esperadas e Condizentes”. A rubrica foi formalizada após a coleta, as fontes são sintéticas preparadas com IA, e a captura de B-CT04 mostra aviso de revisão pendente em DOC-04. `tau=0,5` foi escolhido após as execuções. O gráfico e métricas são exploratórios; os resultados não sustentam conclusão confirmatória de superioridade entre versões.

## Projeto avaliado

- Projeto: Cherry Studio, fluxo de Base de Conhecimento (RAG).
- Versão avaliada: 2.0.13.
- Modelo: Gemini Flash-Lite Latest (alias `latest`; revisão não congelável).
- Comparação planejada: versão A (baseline) e versão B (prompt de sistema diferente, conforme relato posterior à execução; não há evidência suficiente para confirmar que foi a única mudança).
- Contexto: documentos sintéticos da empresa fictícia Cereja Eletro.

## Integrantes

Equipe 04 — 7 pessoas:

- Adam Lima
- Enzo Emanuel Maia Costa
- Douglas D-da
- Rafael Prata
- Raphael Portella
- Vinicius Souza
- Thayla Figueiredo

## Vídeo da atividade

[PREENCHER URL]

## Relatório

O texto-base do relatório está em [`atividade3/entrega/relatorio-base.md`](atividade3/entrega/relatorio-base.md). A versão final em PDF ainda deve ser revisada pela equipe e adicionada ao repositório.

## Índice

- [`atividade3/gqm/`](atividade3/gqm/): plano GQM e critérios, com limitações de pré-registro documentadas.
- [`atividade3/casos/`](atividade3/casos/): casos de teste e referências.
- [`atividade3/fontes/`](atividade3/fontes/): inventário das fontes sintéticas.
- [`atividade3/versoes/`](atividade3/versoes/): prompts e manifestos das versões A e B.
- [`atividade3/execucao/`](atividade3/execucao/): saídas brutas e capturas.
- [`atividade3/metricas/`](atividade3/metricas/): cálculo automático de F1 lexical.
- [`atividade3/avaliacao/`](atividade3/avaliacao/): rubrica e avaliações humanas.
- [`atividade3/resultados/`](atividade3/resultados/): consolidação, gráfico e divergências.
- [`atividade3/ciclo-de-vida/`](atividade3/ciclo-de-vida/): ciclo de vida e rastreabilidade.
- [`atividade3/decisao/`](atividade3/decisao/): decisão experimental.
- [`atividade3/equipe/`](atividade3/equipe/): contribuições e declaração de uso de IA.
- [`atividade3/entrega/`](atividade3/entrega/): checklist e informações do vídeo.

## Como recuperar as versões A e B

Os prompts e manifestos informados para A e B estão em `atividade3/versoes/A/` e `atividade3/versoes/B/`. Ambas são relatadas como executadas no Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669`; como os prompts foram informados após a execução e faltam capturas/configurações completas, não é possível verificar que o prompt foi a única diferença. Para consultar esse código, clone o repositório oficial do Cherry Studio e faça checkout do commit registrado:

```text
git clone https://github.com/CherryHQ/cherry-studio.git
cd cherry-studio
git checkout 6e3af1beac02cdc53dd2aba382cb6af7475dc669
```

Uma nova execução com os manifestos não deve ser apresentada como reprodução exata das respostas antigas: parâmetros e contextos efetivamente recuperados não foram preservados, o alias `latest` pode mudar e houve apenas uma execução por caso/versão.
