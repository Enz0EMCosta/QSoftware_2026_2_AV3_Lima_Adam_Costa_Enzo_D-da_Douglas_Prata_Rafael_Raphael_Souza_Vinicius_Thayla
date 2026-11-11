# Métricas automáticas

Documentação e execução do cálculo de F1 lexical automático com `f1_lexical.py`.

## Tarefa

[PREENCHER: descrever o uso do script, entradas, saídas e comando de execução.]

## Definição

Comparar resposta e referência com tokens, normalização Unicode NFC, `casefold` e interseção de multiconjuntos. Registrar o limiar `tau` no plano GQM antes do teste; sinal automático de aprovação quando `F1 >= tau`.

## Entradas e saídas

- Entrada CSV: cabeçalho `caso,versao,resposta,referencia`; uma linha por resposta.
- Referências: usar somente referências humanas válidas, depois de revisão e autorização; as referências atuais em `atividade3/casos/casos-e-referencias.csv` são rascunhos gerados com IA e não devem ser usadas como ground truth oficial.
- Limiar exploratório pós-hoc: `tau = 0,5`; não comprovado como limiar pré-registrado.
- Saída do script: CSV com `caso,versao,precisao,revocacao,F1,sinal_auto`.

Exemplo de execução, quando houver entrada válida:

```text
python atividade3/metricas/f1_lexical.py entrada-validada.csv --tau 0.5 --saida resultados-f1.csv
```

O script aplica NFC, `casefold`, tokens Unicode `\w+` e interseção de contagens (multiconjuntos). Se a resposta ou a referência não contiver tokens, a métrica retorna zero para a divisão correspondente; quando precisão e revocação forem ambas zero, F1 também é zero.

## Análise do artefato

O estudante pediu a escolha de `tau` após as execuções; para exploração foi adotado `0,5`, sem validade de pré-registro. As referências atualmente no CSV foram preparadas com auxílio de IA, apesar de a atividade exigir referências humanas. Por isso, não calcular/apresentar F1 oficial com essas referências. Primeiro obter referências humanas válidas e orientação do professor sobre a alteração pós-teste; eventual cálculo posterior deve ser marcado como exploratório e baseado em referência nova, sem alegar que foi a referência usada antes dos testes.

## Resultados

F1, precisão, revocação, média, mediana e sinais automáticos ainda não calculados. Não há resultados numéricos válidos registrados.
