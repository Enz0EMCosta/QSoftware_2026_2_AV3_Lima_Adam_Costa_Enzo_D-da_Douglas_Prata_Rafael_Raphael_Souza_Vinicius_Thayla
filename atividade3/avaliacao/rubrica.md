# Rubrica de avaliação humana

Rubrica operacional da equipe para correção, relevância, suporte e falha crítica. Conforme relato do estudante, o professor permitiu que a equipe elaborasse a própria rubrica. Os descritores abaixo foram formalizados com auxílio de IA em 11/11/2026, depois das execuções; não são apresentados como pré-registrados.

## Tarefa

Avaliar cada resposta contra a pergunta, a referência e a fonte, atribuindo notas independentes de 0 a 2 para correção, relevância e suporte, além de registrar falha crítica (0/1).

## Escala

| Dimensão | 0 | 1 | 2 |
|---|---|---|---|
| Correção | Contém erro material ou contradiz a fonte/referência em ponto central. | É parcialmente correta, mas contém imprecisão ou omissão material que reduz a confiabilidade. | As afirmações materiais respondem corretamente ao caso e não contradizem a fonte/referência. |
| Relevância | Não responde ao pedido ou se desvia do caso. | Responde parcialmente, mas deixa sem resposta um aspecto importante da pergunta. | Responde aos aspectos solicitados, incluindo limites ou condições relevantes. |
| Suporte | Afirmações centrais não são sustentadas pelas fontes disponíveis ou as contradizem. | Há suporte parcial, mas uma afirmação material carece de evidência ou de ressalva. | As afirmações materiais são rastreáveis às fontes/contexto disponíveis e não extrapolam sua evidência. |

## Falha crítica

- `0`: não foi identificada afirmação que possa induzir materialmente a uma decisão incorreta sobre reembolso ou garantia.
- `1`: há afirmação materialmente falsa, contraditória ou sem suporte que possa induzir a pessoa a acreditar que tem direito a reembolso/cobertura ou que não tem esse direito, em desacordo com a fonte; ou a resposta ignora a insuficiência de evidência de modo a afirmar uma conclusão categórica.

Registrar a passagem da resposta e a regra/fonte que sustentam qualquer `1`. A falha crítica é independente das três notas.

## Regra de aprovação

A saída é aprovada somente quando correção=2, relevância=2, suporte=2 e falha_critica=0.

## Procedimento

1. Avaliar cada saída individualmente, sem usar o F1 ou o sinal automático para orientar as notas.
2. Para reduzir viés, ocultar versão e ordem de avaliação; ler pergunta, resposta e fonte pertinente.
3. Registrar justificativa específica e evidência textual para cada nota. Não inventar justificativas ausentes.
4. O protocolo inicial previa R1 em 12 saídas e R2 em CT01 e CT05 em A e B (quatro saídas) de forma independente. Segundo esclarecimento posterior do estudante, Thayla foi R1 e Douglas foi R2; Douglas também avaliou as 12 saídas posteriormente.
5. Comparar R1 e R2 antes de conversa; calcular decisões iguais/4. Só então discutir divergências e registrar consenso sem sobrescrever as notas originais.

## Estado e limitações

O avaliador informou, por intermédio do estudante, ter dado notas separadas `2,2,2,0` para cada saída A e B e ter avaliado às cegas; não foram fornecidas fichas originais nem justificativas/evidências por dimensão. A equipe formalizou os descritores desta rubrica após as execuções. Assim, os escores transcritos em `r1.csv` são atribuídos ao avaliador no nível de dimensão, mas a correspondência dos julgamentos originais com cada descritor operacional acima não foi verificada. As referências atuais dos casos também foram rascunhadas com IA e precisam de revisão humana.

## Análise do artefato

Os critérios agora distinguem correção, relevância, suporte e falha crítica. Como a definição textual foi formalizada depois da coleta, a rubrica não comprova pré-registro; faltam as justificativas originais para auditar a aplicação dos descritores.

## Resultados

As notas R1 reportadas pelo estudante foram transcritas em `r1.csv`; os quatro escores R2 inicialmente previstos estão em `r2.csv`. Embora Douglas tenha avaliado posteriormente todas as 12 saídas, os oito escores adicionais não foram transcritos. As notas existentes satisfazem aritmeticamente a regra de aprovação (três notas 2 e falha crítica 0), mas os resultados devem ser tratados como relatados e limitados pelas lacunas de evidência e de pré-registro.
