# Atividade 3 — Qualidade de Software

Esqueleto do repositório da Atividade 3 da disciplina de Qualidade de Software (UFS); preencher os campos indicados sem incluir dados pessoais ou credenciais.

## Resumo

Esta atividade documenta uma comparação exploratória entre respostas do fluxo de Base de Conhecimento do Cherry Studio. Foram transcritas seis respostas A e seis B em 11/11/2026. O estudante informou posteriormente prompts de sistema diferentes para A e B, sem capturas arquivadas para confirmação independente. R1 reportado atribuiu 2,2,2,0 a cada saída (aprovação provisória 6/6 por versão); justificativas individuais ainda não foram fornecidas e a rubrica foi formalizada após a coleta. As referências atuais foram rascunhadas com IA e `tau=0,5` foi escolhido após as execuções. Os resultados não sustentam uma conclusão confirmatória de superioridade entre versões.

## Projeto avaliado

- Projeto: Cherry Studio, fluxo de Base de Conhecimento (RAG).
- Versão avaliada: 2.0.13.
- Modelo: Gemini Flash-Lite Latest (alias `latest`; revisão não congelável).
- Comparação: versão A (baseline com prompt simples) e versão B (mudança apenas no prompt de sistema).
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

## Índice

- [`atividade3/gqm/`](atividade3/gqm/): plano GQM registrado antes dos testes.
- [`atividade3/casos/`](atividade3/casos/): casos de teste e referências.
- [`atividade3/fontes/`](atividade3/fontes/): inventário das fontes sintéticas.
- [`atividade3/versoes/`](atividade3/versoes/): prompts e manifestos das versões A e B.
- [`atividade3/execucao/`](atividade3/execucao/): saídas brutas e capturas.
- [`atividade3/metricas/`](atividade3/metricas/): cálculo automático de F1 lexical.
- [`atividade3/avaliacao/`](atividade3/avaliacao/): rubrica e avaliações humanas.
- [`atividade3/resultados/`](atividade3/resultados/): consolidação e divergências.
- [`atividade3/ciclo-de-vida/`](atividade3/ciclo-de-vida/): ciclo de vida e rastreabilidade.
- [`atividade3/decisao/`](atividade3/decisao/): decisão experimental.
- [`atividade3/equipe/`](atividade3/equipe/): contribuições e declaração de uso de IA.
- [`atividade3/entrega/`](atividade3/entrega/): checklist e informações do vídeo.

## Como recuperar as versões A e B

As versões experimentais são descritas pelos prompts e manifestos em `atividade3/versoes/A/` e `atividade3/versoes/B/`. Ambas usam o código Cherry Studio v2.0.13 no commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669`; a versão B altera somente o prompt de sistema. Para consultar esse código, clone o repositório oficial do Cherry Studio e faça checkout do commit registrado:

```text
git clone https://github.com/CherryHQ/cherry-studio.git
cd cherry-studio
git checkout 6e3af1beac02cdc53dd2aba382cb6af7475dc669
```

Reconstitua cada configuração aplicando o prompt correspondente, os parâmetros e as fontes documentados no manifesto. Os campos não registrados ainda estão marcados como `[PREENCHER]`; não presuma que uma nova execução reproduzirá saídas anteriores, pois o alias `latest` pode mudar e houve uma execução por caso/versão.
