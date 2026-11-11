# Manifesto — Versão B

Registro conciso da configuração e dos limites de reprodução da versão B.

## Tarefa

Documentar a configuração da versão B e verificar o controle de variável em relação à versão A.

## Análise do artefato

| Campo | Registro |
|---|---|
| Data de execução | [PREENCHER: registrar a data real após executar os casos; ainda não informada] |
| Código/commit | Cherry Studio v2.0.13, commit `6e3af1beac02cdc53dd2aba382cb6af7475dc669` |
| Mudança em relação à versão anterior | Somente o prompt de sistema. A mudança concreta depende do prompt definido para o experimento e ainda não foi registrada. |
| Prompt | `atividade3/versoes/B/prompt.md` — ainda não definido/transcrito; registrar o prompt aprovado e confirmar que somente ele difere de A. |
| Modelo/revisão | Gemini Flash-Lite Latest (alias `latest`); revisão não congelável. |
| Parâmetros | [PREENCHER: registrar parâmetros reais e confirmar igualdade com A] |
| Fonte/contexto | Usar as mesmas fontes e o mesmo contexto da versão A. Fontes sintéticas planejadas: Cereja Eletro, incluindo DOC-01 (política de reembolso v2) e DOC-04 (manual de garantia); confirmar arquivos e contexto efetivamente usados. |
| Casos/referências | CT01–CT06; referências em `atividade3/casos/casos-e-referencias.csv`. Registrar a revisão do arquivo efetivamente usada e confirmar igualdade com A. |
| Rubrica/limiar | Rubrica em `atividade3/avaliacao/rubrica.md`; `tau` e rubrica precisam estar definidos e registrados antes das execuções: [PREENCHER]. |
| Resultados | Pendente: preencher após as seis execuções B, cálculo de F1 e avaliações humanas; não há resultados registrados neste repositório. |
| Limitações de reprodução | O alias `latest` pode mudar; uma execução por caso/versão. |

## Resultados

Ainda não disponíveis. Após a execução, registrar aprovação humana sobre 6, sinal automático e referência às saídas B-CT01 a B-CT06 e à tabela consolidada.
