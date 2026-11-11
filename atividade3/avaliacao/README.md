# Avaliação humana

Registro do processo de avaliação humana e de suas limitações; resultados de IA ou métricas automáticas não são avaliação humana.

## Tarefa

O protocolo prevê R1 em 12 saídas e R2 em CT01/CT05 nas duas versões (quatro saídas). Segundo o estudante, Vinicius Souza Morais não executou as respostas e avaliou as 12 às cegas. O estudante reportou posteriormente os escores por dimensão 2,2,2,0 para todas as saídas; as fichas originais e justificativas individuais não foram fornecidas.

## Avaliação humana complementar recebida

O estudante informou que o avaliador deu nota geral **9/10 a cada saída A** e **10/10 a cada saída B**. Depois, informou também escores separados de correção, relevância, suporte e falha crítica: **2,2,2,0 para cada uma das 12 saídas**. As fichas do avaliador e justificativas/evidências por saída não foram anexadas.

As notas gerais 0–10 não foram convertidas. Os escores 2,2,2,0 foram transcritos em `r1.csv` conforme relato explícito do estudante, não inferidos pela IA. A regra aritmética da rubrica classifica os 12 como aprovados, mas faltam justificativas e evidências individuais e os descritores atuais foram formalizados após as execuções; apresentar como resultado reportado com essa limitação.

## Cegamento e anonimização

O estudante relata que o avaliador avaliou às cegas. Os IDs aleatórios e a chave local foram criados depois das avaliações para organização, portanto não são evidência de que esses IDs foram usados durante a avaliação. O cegamento é autorrelato, não verificado por planilha ou registro contemporâneo.

O arquivo `chave-anonimizacao.csv` fica ignorado pelo Git. Foi criado após as avaliações para mapear os IDs às condições e não deve ser publicado enquanto houver revisão cega pendente. Não publicar dados pessoais ou credenciais.

## Arquivos

- `rubrica.md`: critérios e regra de aprovação.
- `r1.csv`: uma linha por saída, 12 escores transcritos do relato do estudante.
- `r2.csv`: uma linha por saída revisada, total de 4.
- `consenso.md`: somente divergências e respectivas decisões finais.
- `chave-anonimizacao.csv`: chave local, não publicar antes do encerramento das revisões.

## Análise do artefato

Os escores dimensionais 0/1/2 foram reportados pelo estudante como avaliação de um colega não executor. A IA apenas os transcreveu; não atribuiu notas. Faltam os formulários originais e justificativas por saída. A rubrica operacional foi formalizada depois das execuções com auxílio de IA, e as referências atuais dos casos também foram rascunhadas com IA.

## Resultados

Há relato de nota geral 9/10 para cada A e 10/10 para cada B, além de escores 2,2,2,0 para cada saída transcritos em `r1.csv`. Pela regra, os escores reportados resultam provisoriamente em 6/6 aprovações R1 por versão; faltam justificativas individuais. R2 e consenso não foram fornecidos; `r2.csv` permanece vazio. Não há concordância R1–R2.
