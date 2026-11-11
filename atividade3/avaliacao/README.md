# Avaliação humana

Registro do processo de avaliação humana e de suas limitações; resultados de IA ou métricas automáticas não são avaliação humana.

## Tarefa

O protocolo previsto é R1 em 12 saídas e R2 em CT01/CT05 nas duas versões (quatro saídas). Um colega não executor realizou, segundo o estudante, avaliação geral cega em escala 0–10; isso é independente da execução, mas não segue a rubrica oficial. Nenhuma avaliação formal R1/R2 em escala 0/1/2 ou consenso foi registrada.

## Avaliação humana complementar recebida

O estudante informou que um colega, identificado aqui apenas como revisor humano, avaliou individualmente as 12 saídas às cegas e não participou da execução. Segundo o relato, atribuiu nota geral **9/10 a cada saída A** e **10/10 a cada saída B**. Essa informação é um relato do estudante; as fichas originais e justificativas por saída não foram anexadas.

Essas notas não são equivalentes à rubrica exigida (correção, relevância e suporte, cada uma 0–2, mais falha crítica 0/1). Não convertê-las em notas por dimensão, não preencher `r1.csv` com valores inferidos e não calcular aprovação `x/6` a partir delas. Podem ser mencionadas apenas como avaliação geral complementar, com escala e limitação explícitas. O mesmo prompt de sistema foi informado para A e B, portanto a diferença 9/10 versus 10/10 não pode ser atribuída a uma mudança de prompt.

## Cegamento e anonimização

O estudante relata que a avaliação geral complementar foi feita às cegas. Não foi fornecida planilha anonimizada, chave separada nem evidência documental do procedimento; registrar o cegamento como autorrelato, não como verificado.

O arquivo `chave-anonimizacao.csv` fica ignorado pelo Git até que R1 e R2 terminem, para preservar o cegamento. Não publicar chaves, dados pessoais ou credenciais.

## Arquivos

- `rubrica.md`: critérios e regra de aprovação.
- `r1.csv`: uma linha por saída, total de 12.
- `r2.csv`: uma linha por saída revisada, total de 4.
- `consenso.md`: somente divergências e respectivas decisões finais.
- `chave-anonimizacao.csv`: chave local, não publicar antes do encerramento das revisões.

## Análise do artefato

As 12 notas gerais 0–10 foram relatadas como provenientes de um colega não executor. Porém, não cumprem a rubrica 0/1/2 e não substituem R1/R2 conforme o protocolo. Uma IA não pode atribuir notas. A rubrica original e referências escritas por pessoas também não foram fornecidas.

## Resultados

Há relato de nota geral 9/10 para cada A e 10/10 para cada B, sem fichas/justificativas anexas. Não há resultados R1/R2 pela rubrica oficial. `r1.csv`, `r2.csv` e `consenso.md` permanecem sem avaliações por dimensão; não preencher notas por inferência.
