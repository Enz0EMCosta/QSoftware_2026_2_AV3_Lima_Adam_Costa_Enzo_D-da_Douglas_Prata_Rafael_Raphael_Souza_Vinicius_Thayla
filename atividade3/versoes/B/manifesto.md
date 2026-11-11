# Manifesto — Versão B

Registro conciso da configuração e dos limites de reprodução da versão B.

## Tarefa

Documentar a configuração da versão B e verificar o controle de variável em relação à versão A.

## Análise do artefato

| Campo | Registro |
|---|---|
| Data de execução | 11/11/2026. Horários informados: CT01–CT04 às 09:13; CT05–CT06 às 09:14. |
| Código/commit | Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669` |
| Mudança em relação à versão anterior | Pretendia-se alterar somente o prompt de sistema; o texto do prompt B e o prompt A não foram fornecidos para confirmar a mudança. |
| Prompt | `atividade3/versoes/B/prompt.md` registra a lacuna. As perguntas executadas estão em `atividade3/casos/casos-e-referencias.csv`; elas não são o prompt de sistema. |
| Modelo/revisão | Gemini Flash-Lite Latest (alias `latest`); revisão não congelável. |
| Parâmetros | [NÃO INFORMADOS; igualdade com A não verificada.] |
| Fonte/contexto | DOC-01 e DOC-04 são rascunhos sintéticos preparados com auxílio de IA nesta atividade. O estudante confirmou conversa nova para cada caso B; igualdade da base e do contexto recuperado em relação a A não foi documentada. |
| Casos/referências | CT01–CT06 em `atividade3/casos/casos-e-referencias.csv`. As referências atuais também foram preparadas com auxílio de IA e não são válidas como referências humanas finais. |
| Rubrica/limiar | Rubrica original e limiar pré-teste não fornecidos. `tau = 0,5` foi escolhido posteriormente como parâmetro exploratório, não pré-registrado verificável. |
| Resultados | Seis respostas B foram registradas em `atividade3/execucao/saidas-brutas/B-CT01.md` a `B-CT06.md`. F1 e avaliações humanas não foram calculados/registrados. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão; prompt de sistema e parâmetros exatos não foram informados; igualdade de base/configuração não confirmada; contextos recuperados e capturas ausentes. |

## Resultados

As seis respostas estão registradas, mas ainda não há resultados válidos de F1 nem avaliações humanas. Não calcular o F1 oficial contra as referências atuais geradas com auxílio de IA.
