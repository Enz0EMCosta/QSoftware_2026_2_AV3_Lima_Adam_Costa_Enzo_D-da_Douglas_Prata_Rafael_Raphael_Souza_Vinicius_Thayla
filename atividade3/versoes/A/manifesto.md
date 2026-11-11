# Manifesto — Versão A

Registro conciso da configuração e dos limites de reprodução da versão A (baseline).

## Tarefa

Documentar a configuração da versão A para rastreabilidade da execução.

## Análise do artefato

| Campo | Registro |
|---|---|
| Data de execução | 11/11/2026. Horários: CT01 às 09:01 (captura), CT02 às 09:02 (captura); CT03, CT04 e CT05 às 09:03; CT06 às 09:04 (horários informados). |
| Código/commit | Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669` |
| Mudança em relação à versão anterior | Baseline. Prompt informado: “Responda a pergunta solicitada de acordo com a Base de Conhecimentos (Knowledge Base) informada”. |
| Prompt | `atividade3/versoes/A/prompt.md`; texto informado após as execuções, sem captura da configuração para confirmação independente. |
| Modelo/revisão | Gemini Flash-Lite Latest (alias `latest`); revisão não congelável. |
| Parâmetros | [NÃO INFORMADOS; não presumir temperatura, top-p ou outros valores.] |
| Fonte/contexto | DOC-01 e DOC-04 são fontes sintéticas preparadas com auxílio de IA. A captura B-CT04 mostra que o painel de DOC-04 ainda exibe um aviso de rascunho sujeito a revisão; não há captura do contexto A efetivamente recuperado. |
| Casos/referências | CT01–CT06 em `atividade3/casos/casos-e-referencias2.csv`. A fonte é sintética e preparada com IA; o estudante relata revisão humana posterior, sem nome/data ou confirmação independente. |
| Rubrica/limiar | Rubrica original e limiar pré-teste não fornecidos. `tau = 0,5` foi escolhido posteriormente como parâmetro exploratório, não pré-registrado verificável. |
| Resultados | Seis respostas A registradas. R1 reportado: correção=2, relevância=2, suporte=2, falha crítica=0 em todas (6/6 aprovações provisórias). O avaliador também reportou 9/10 geral por saída. F1 médio exploratório=0,479003; 2/6 sinais automáticos positivos com tau=0,5 pós-hoc. Justificativas individuais não fornecidas. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão; parâmetros e contextos recuperados ausentes; capturas de apenas A-CT01/02, sem prompt/configuração. |

## Resultados

As seis respostas e os escores R1 reportados estão registrados; resultado provisório de aprovação R1: 6/6. O F1 está registrado em `atividade3/resultados/f1-lexical.csv`; resultado exploratório, não pré-registrado. Justificativas individuais ausentes.
