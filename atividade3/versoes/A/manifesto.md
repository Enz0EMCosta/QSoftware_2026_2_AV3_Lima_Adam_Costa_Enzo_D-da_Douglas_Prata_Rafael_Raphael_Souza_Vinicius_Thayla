# Manifesto — Versão A

Registro conciso da configuração e dos limites de reprodução da versão A (baseline).

## Tarefa

Documentar a configuração da versão A para rastreabilidade da execução.

## Análise do artefato

| Campo | Registro |
|---|---|
| Data de execução | 11/11/2026. Horários informados: CT01 e CT02 às 09:02; CT03, CT04 e CT05 às 09:03; CT06 às 09:04. |
| Código/commit | Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669` |
| Mudança em relação à versão anterior | Baseline. Prompt informado: “Responda a pergunta solicitada de acordo com a Base de Conhecimentos (Knowledge Base) informada”. |
| Prompt | `atividade3/versoes/A/prompt.md`; texto informado após as execuções, sem captura/configuração arquivada para confirmação independente. |
| Modelo/revisão | Gemini Flash-Lite Latest (alias `latest`); revisão não congelável. |
| Parâmetros | [NÃO INFORMADOS; não presumir temperatura, top-p ou outros valores.] |
| Fonte/contexto | DOC-01 e DOC-04 são rascunhos sintéticos preparados com auxílio de IA nesta atividade. Arquivos/contextos efetivamente recuperados por execução não foram preservados no registro recebido. |
| Casos/referências | CT01–CT06 em `atividade3/casos/casos-e-referencias.csv`. As referências atuais também foram preparadas com auxílio de IA e não são válidas como referências humanas finais. |
| Rubrica/limiar | Rubrica original e limiar pré-teste não fornecidos. `tau = 0,5` foi escolhido posteriormente como parâmetro exploratório, não pré-registrado verificável. |
| Resultados | Seis respostas A foram registradas em `atividade3/execucao/saidas-brutas/A-CT01.md` a `A-CT06.md`. F1 e avaliações pela rubrica 0/1/2 não foram calculados/registrados. O estudante relata avaliação de colega em escala 9/10, sem detalhamento por dimensão. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão; parâmetros exatos, contextos recuperados e capturas ausentes; prompt informado sem evidência visual da configuração. |

## Resultados

As seis respostas estão registradas, mas ainda não há resultados válidos de F1 nem avaliações humanas. Não calcular o F1 oficial contra as referências atuais geradas com auxílio de IA.
