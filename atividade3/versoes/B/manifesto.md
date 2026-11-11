# Manifesto — Versão B

Registro conciso da configuração e dos limites de reprodução da versão B.

## Tarefa

Documentar a configuração da versão B e verificar o controle de variável em relação à versão A.

## Análise do artefato

| Campo | Registro |
|---|---|
| Data de execução | 11/11/2026. Horários informados: CT01–CT04 às 09:13; CT05–CT06 às 09:14. |
| Código/commit | Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669` |
| Mudança em relação à versão anterior | Prompt B informado: “Responda a pergunta solicitada com base no documento que serviu de base para seu funcionamento”. A versão A usa “Responda a pergunta solicitada de acordo com a Base de Conhecimentos (Knowledge Base) informada”. |
| Prompt | `atividade3/versoes/B/prompt.md`; texto informado após as execuções, sem captura/configuração arquivada para confirmação independente. |
| Modelo/revisão | Gemini Flash-Lite Latest (alias `latest`); revisão não congelável. |
| Parâmetros | [NÃO INFORMADOS; igualdade com A não verificada.] |
| Fonte/contexto | DOC-01 e DOC-04 são fontes sintéticas preparadas com auxílio de IA. A captura B-CT04 mostra o painel DOC-04, cujo texto ainda o identifica como rascunho sintético sujeito a revisão/aprovação. O estudante confirmou conversa nova para cada caso B; igualdade da base e dos contextos recuperados em relação a A não foi documentada. |
| Casos/referências | CT01–CT06 em `atividade3/casos/casos-e-referencias2.csv`. A fonte é sintética e preparada com IA; o estudante relata revisão humana posterior, sem nome/data ou confirmação independente. |
| Rubrica/limiar | Rubrica original e limiar pré-teste não fornecidos. `tau = 0,5` foi escolhido posteriormente como parâmetro exploratório, não pré-registrado verificável. |
| Resultados | Seis respostas B registradas. R1 reportado: correção=2, relevância=2, suporte=2, falha crítica=0 em todas (6/6 aprovações provisórias). O avaliador também reportou 10/10 geral por saída. F1 médio exploratório=0,503373; 3/6 sinais automáticos positivos com tau=0,5 pós-hoc. Justificativas individuais não fornecidas. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão; a mudança de prompt foi relatada após as execuções e não está corroborada por captura/configuração; parâmetros exatos e igualdade da base/contexto não demonstrados. Há capturas parciais B-CT02 e B-CT04, mas nenhuma mostra o prompt de sistema. |

## Resultados

As seis respostas e os escores R1 reportados estão registrados; resultado provisório de aprovação R1: 6/6. O F1 está registrado em `atividade3/resultados/f1-lexical.csv`; resultado exploratório, não pré-registrado. Justificativas individuais ausentes.
