# Rubrica de avaliação humana

Esqueleto da rubrica para avaliação humana. O conteúdo original atribuído a Raphael não foi fornecido; não foram registrados escores R1/R2 neste repositório.

## Tarefa

Atribuir notas de 0 a 2 para correção, relevância e suporte, além de registrar falha crítica binária (0/1).

## Escala

| Dimensão | 0 | 1 | 2 |
|---|---|---|---|
| Correção | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] |
| Relevância | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] |
| Suporte | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] | [DESCRITOR ORIGINAL NÃO FORNECIDO] |

## Falha crítica

- `0`: nenhuma falha crítica identificada.
- `1`: falha crítica identificada; descrever evidência e regra operacional conforme protocolo original: [NÃO FORNECIDO].

## Regra de aprovação

A saída é aprovada somente quando correção=2, relevância=2, suporte=2 e falha_critica=0.

## Como aplicar

1. Use uma cópia anonimizada da resposta, sem mostrar versão, prompt, F1, sinal automático ou nota de outro avaliador.
2. Leia a pergunta, a referência humana aprovada e o trecho da fonte que sustenta a referência; depois leia a resposta completa.
3. Atribua separadamente uma nota 0, 1 ou 2 para correção, relevância e suporte, aplicando os descritores da rubrica original. Registre justificativa curta com evidência textual da resposta e da fonte.
4. Marque falha crítica como 0 ou 1 conforme a regra operacional definida no protocolo original e justifique qualquer 1.
5. Marque aprovada somente quando as três dimensões forem 2 e falha_critica for 0.
6. R1 registra as 12 saídas em `r1.csv`. R2 registra apenas CT01 e CT05 em A e B (quatro saídas) em `r2.csv`, sem consultar as notas de R1. Calcule igualdade das decisões em 4 antes de qualquer conversa; só depois discuta divergências e registre eventual consenso sem alterar avaliações originais.

## Limite da rubrica disponível

Os descritores originais para os níveis 0/1/2 e a definição operacional de falha crítica não foram fornecidos; os campos da escala acima são marcadores de ausência, não critérios oficiais completos. Solicite a Raphael o arquivo original. Não invente interpretações e apresente-as como rubrica oficial. Se o original não puder ser recuperado, obtenha aprovação do professor para definir rubrica nova, identifique-a como adaptação posterior à coleta e não a use para alegar pré-registro.

O colega foi relatado como avaliador cego e não executor, mas as notas que forneceu foram gerais, em escala 0–10 (A=9/10, B=10/10). Elas não podem ser convertidas em notas 0/1/2 por dimensão. Se ele fizer nova avaliação por dimensão, preserve as notas 0–10 separadamente e registre a nova avaliação com data e condição de cegamento.

As referências atuais são rascunhos gerados com auxílio de IA, não referências humanas aprovadas. Antes de pontuar suporte/correção contra elas, obtenha referências escritas ou reescritas e aprovadas por pessoa, ou instrução do professor para adaptar o método. Não atribuir notas por IA.

## Análise do artefato

Não é possível verificar consistência da aplicação oficial até recuperar os descritores originais, referências humanas válidas e fichas por dimensão.

## Resultados

Não há resultados humanos registrados. Os arquivos `r1.csv` e `r2.csv` permanecem sem linhas de avaliação.
