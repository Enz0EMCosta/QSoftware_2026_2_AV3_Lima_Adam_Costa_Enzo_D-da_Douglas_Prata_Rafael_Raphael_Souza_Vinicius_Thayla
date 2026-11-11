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
| Fonte/contexto | DOC-01 e DOC-04 são rascunhos sintéticos preparados com auxílio de IA nesta atividade. O estudante confirmou conversa nova para cada caso B; igualdade da base e do contexto recuperado em relação a A não foi documentada. |
| Casos/referências | CT01–CT06 em `atividade3/casos/casos-e-referencias.csv`. As referências atuais também foram preparadas com auxílio de IA e não são válidas como referências humanas finais. |
| Rubrica/limiar | Rubrica original e limiar pré-teste não fornecidos. `tau = 0,5` foi escolhido posteriormente como parâmetro exploratório, não pré-registrado verificável. |
| Resultados | Seis respostas B foram registradas em `atividade3/execucao/saidas-brutas/B-CT01.md` a `B-CT06.md`. F1 e avaliações pela rubrica 0/1/2 não foram calculados/registrados. O estudante relata avaliação de colega em escala 10/10, sem detalhamento por dimensão. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão; a mudança de prompt foi relatada após as execuções e não está corroborada por captura/configuração arquivada; parâmetros exatos, igualdade da base/contexto e capturas ausentes. |

## Resultados

As seis respostas estão registradas, mas ainda não há resultados válidos de F1 nem avaliações humanas. Não calcular o F1 oficial contra as referências atuais geradas com auxílio de IA.
