# Métricas automáticas

Documentação e execução do cálculo de F1 lexical automático com `f1_lexical.py`.

## Tarefa

Calcular precisão, revocação e F1 lexical das 12 respostas A/B contra as referências registradas, e comparar o sinal automático com as aprovações R1 reportadas.

## Definição

Comparar resposta e referência com tokens, normalização Unicode NFC, `casefold` e interseção de multiconjuntos. Registrar o limiar `tau` no plano GQM antes do teste; sinal automático de aprovação quando `F1 >= tau`.

## Entradas e saídas

- Entrada CSV: cabeçalho `caso,versao,resposta,referencia`; uma linha por resposta.
- Referências usadas: `atividade3/casos/casos-e-referencias2.csv`. O estudante relata que uma pessoa reescreveu/revisou as referências, com poucas mudanças; nome e data da revisão não foram informados. A fonte documental continua sendo sintética e foi preparada com auxílio de IA; a autoria/revisão humana não foi verificada independentemente.
- Limiar exploratório pós-hoc: `tau = 0,5`; não comprovado como limiar pré-registrado.
- Respostas: transcrições em `atividade3/execucao/saidas-brutas/`.
- Saída detalhada: `atividade3/resultados/f1-lexical.csv`, com `caso,versao,precisao,revocacao,F1,sinal_auto`. A coluna `sinal_auto` vale 1 quando F1 >= 0,5.

Exemplo de execução do script:

```text
python atividade3/metricas/f1_lexical.py entrada-validada.csv --tau 0.5 --saida resultados-f1.csv
```

O script aplica NFC, `casefold`, tokens Unicode `\w+` e interseção de contagens (multiconjuntos). Se a resposta ou a referência não contiver tokens, a métrica retorna zero para a divisão correspondente; quando precisão e revocação forem ambas zero, F1 também é zero.

## Análise do artefato

O estudante escolheu `tau` após as execuções; portanto, todos os sinais e comparações com esse limiar são exploratórios, não pré-registrados. Embora a revisão humana das referências tenha sido relatada, faltam nome/data e registro verificável. As fontes de apoio são sintéticas e foram preparadas com IA; a captura B-CT04 mostra que DOC-04 ainda exibia aviso de revisão/aprovação pendente e campos editoriais “PREENCHER”. Assim, o cálculo não deve ser tratado como confirmação formal de qualidade ou superioridade entre versões, nem como validação contra ground truth humano verificado. F1 lexical mede sobreposição de tokens, não equivalência semântica, correção ou suporte factual.

## Resultados

| Versão | F1 médio | F1 mediano | Sinal automático (F1 >= 0,5) | Aprovações R1 reportadas |
|---|---:|---:|---:|---:|
| A | 0,479003 | 0,454726 | 2/6 | 6/6 |
| B | 0,503373 | 0,494036 | 3/6 | 6/6 |

Considerando como aprovadas as 12 respostas segundo R1 reportado, a concordância binária entre sinal automático e R1 é 5/12. Essa comparação é apenas exploratória: o limiar foi escolhido pós-hoc, R1 foi informado pelo estudante sem fichas anexas e a rubrica foi formalizada depois da coleta. Para as quatro saídas revisadas, o estudante reportou concordância R1–R2 de 4/4; as justificativas R2 são gerais e os formulários originais não foram fornecidos.

Gráfico comparativo: `atividade3/resultados/grafico-resultados.svg`.
