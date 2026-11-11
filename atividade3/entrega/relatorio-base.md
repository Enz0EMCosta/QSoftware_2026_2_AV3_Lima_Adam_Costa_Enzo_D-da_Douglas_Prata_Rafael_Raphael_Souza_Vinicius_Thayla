# Qualidade de Software — 2026.2

## Atividade 3: Métricas automáticas versus avaliação humana (GQM)

**Equipe 04 — Cherry Studio**

Adam Guilherme Mendes Lima

Enzo Emanuel Maia Costa

Douglas de Oliveira Déda

Rafael Souza Prata

Raphael Ferreira Portella Bacelar

Vinícius Morais Souza

Thayla Almeida Figueiredo

São Cristóvão, Sergipe — 2026

**Repositório:** https://github.com/Enz0EMCosta/QSoftware_2026_2_AV3_Lima_Adam_Costa_Enzo_D-da_Douglas_Prata_Rafael_Raphael_Souza_Vinicius_Thayla

**Vídeo da equipe (apresentação de 12/11/2026):** [inserir URL após publicação]

> As seções estão organizadas por integrante, conforme a divisão da atividade. Quando os artefatos disponíveis não comprovam que a pessoa responsável executou uma tarefa, isso é indicado explicitamente; atribuição planejada não é tratada como prova de contribuição concluída. Não incluímos números de matrícula nesta cópia pública.

## Resumo

Este trabalho relata uma comparação exploratória entre duas configurações informadas do fluxo de Base de Conhecimento do Cherry Studio 2.0.13, usando o modelo Gemini Flash-Lite Latest. Foram registradas seis perguntas em cada condição, A e B, totalizando 12 respostas. A comparação usa F1 lexical contra referências curtas e avaliações humanas reportadas.

Com `tau = 0,5`, escolhido após as execuções, a média de F1 foi 0,479003 em A e 0,503373 em B. O sinal automático aprovou 2/6 respostas A e 3/6 B. Thayla, R1, reportou 6/6 aprovações em cada versão; a concordância entre sinal automático e R1 foi 5/12. Douglas, R2, avaliou posteriormente as 12 respostas. Os quatro escores R2 do subconjunto inicialmente previsto estão registrados e concordam com R1 (4/4); as outras oito notas ainda não foram transcritas.

Os resultados são descritivos: o limiar e a rubrica operacional foram formalizados depois da coleta, as fontes são sintéticas, os registros de avaliação foram reconstruídos retrospectivamente e as evidências de configuração são parciais. Não há base para afirmar que B melhorou a qualidade humana ou para recomendar sua adoção.

## 1- Raphael Ferreira Portella Bacelar

### Bloco 1: Plano GQM e preparação dos casos (Partes A e B)

#### Contexto do experimento

O experimento compara duas formas de instruir o mesmo fluxo de Base de Conhecimento do Cherry Studio, usando documentos sintéticos da empresa fictícia Cereja Eletro. A versão A é o baseline; a versão B usa outro prompt. O desenho prevê seis casos por versão, uma execução por caso e versão, 12 respostas no total. A proposta inicial era mudar somente o prompt, mas essa condição não pôde ser verificada independentemente: os prompts foram informados após as execuções e não há capturas da configuração completa.

#### Objetivo GQM

Analisar as respostas do fluxo de Base de Conhecimento do Cherry Studio, com o propósito de comparar descritivamente a adequação das respostas nas condições A e B e verificar se o sinal de F1 lexical acompanha a avaliação humana, do ponto de vista da equipe da disciplina, no contexto dos seis casos CT01–CT06.

#### Perguntas e medidas

| Pergunta | Medida | Unidade e cálculo | Limitação |
|---|---|---|---|
| Q1. A versão B teve mais respostas aprovadas por R1 do que A? | Aprovação humana por versão | Aprovadas/6. A regra operacional considera aprovada a resposta com correção=2, relevância=2, suporte=2 e falha crítica=0. | São seis casos por versão; os escores foram reportados retrospectivamente. |
| Q2. Com que frequência o sinal automático concordou com R1? | F1 lexical por resposta e concordância automático–R1 | F1 de 0 a 1; sinal positivo se F1 ≥ `tau`. Concordâncias/12. | F1 mede sobreposição lexical, não verdade ou equivalência semântica; `tau` foi escolhido após as execuções. |

Como medida suplementar, a concordância R1–R2 foi calculada no subconjunto inicialmente previsto (CT01 e CT05 em A e B): decisões iguais/4. Embora Douglas tenha avaliado posteriormente todas as respostas, os oito escores adicionais não estão transcritos e não entram nesse cálculo.

#### Limiar, rubrica e critério decisório

O limiar usado na análise foi `tau = 0,5`, mencionado no enunciado como valor didático. Ele foi escolhido depois das execuções, não calibrado em um conjunto independente e não deve ser descrito como pré-registrado. O sinal automático vale 1 quando F1 ≥ 0,5 e 0 quando F1 < 0,5.

A rubrica operacional exige notas 2 em correção, relevância e suporte, além de falha crítica igual a 0. A rubrica e o critério decisório atuais foram formalizados após a coleta com auxílio de IA. O arquivo/commit original do plano, o `tau` originalmente registrado e os critérios originais não foram fornecidos; portanto, esta versão do plano não comprova o pré-registro.

Para eventual nova avaliação, foi registrado um critério pós-hoc: considerar B para uma etapa confirmatória se sua aprovação humana não for inferior à de A e se não houver falha crítica reportada em B. Qualquer falha crítica bloquearia essa consideração até revisão. Esse critério não foi aplicado prospectivamente, não demonstra superioridade e não autoriza produção.

#### Casos e referências

| Caso | Tipo | Pergunta resumida | Fonte indicada |
|---|---|---|---|
| CT01 | Funcional | Reembolso por desistência após 20 dias com produto lacrado e sem uso? | DOC-01, regra 1 |
| CT02 | Funcional | O que informar para avaliar defeito relatado em cinco dias, e isso garante reembolso? | DOC-01, regra 2 |
| CT03 | Funcional | Defeito de fabricação após oito meses, com comprovante e série: o que prevê o manual? | DOC-04, regras 1–3 |
| CT04 | Funcional | Dano por líquido está coberto pela garantia? | DOC-04, regra 4 |
| CT05 | Sem evidência suficiente | É possível afirmar cobertura sem data, comprovante, série e causa? | DOC-04, regras 1–3 |
| CT06 | Variação de CT01 | Reembolso após 20 dias, com produto ainda embalado e sem uso? | DOC-01, regra 1 |

Os casos usados estão registrados em `atividade3/casos/casos-e-referencias2.csv`. DOC-01 e DOC-04 são documentos sintéticos preparados com IA. O estudante relata revisão humana posterior das referências, mas não informou quem revisou nem a data, e não anexou comprovação. A captura B-CT04 mostra que DOC-04 ainda exibia aviso de rascunho sintético sujeito a revisão/aprovação e campos editoriais “PREENCHER”. Assim, não está demonstrado que a fonte foi aprovada antes do teste; as referências não devem ser apresentadas como ground truth humano verificado.

#### Responsabilidade e estado documentado

A Parte 1 foi atribuída a Raphael. A equipe relata que ele preparou um plano antes dos testes, mas o artefato original não foi recuperado. Os documentos e casos sintéticos foram inicialmente preparados por Enzo com auxílio de IA; a revisão posterior das referências é um relato sem identificação ou data. Não atribuímos a Raphael a autoria verificada dos arquivos atuais sem evidência adicional.

## 2- Vinícius Morais Souza

### Bloco 2: Montagem das versões A e B e execução das 12 saídas (Parte B)

#### Ambiente e procedimento informado

| Campo | Registro |
|---|---|
| Data | 11/11/2026 |
| Aplicativo | Cherry Studio 2.0.13 |
| Modelo | Gemini Flash-Lite Latest (`latest`, alias que não congela a revisão do modelo) |
| Casos | CT01–CT06, uma execução por caso em cada versão |
| Conversas | O estudante informou que abriu conversas novas para os casos |
| Configuração | Parâmetros completos, contextos recuperados e igualdade integral da base/configuração não foram preservados |

Os prompts registrados após a execução foram:

- **A:** “Responda a pergunta solicitada de acordo com a Base de Conhecimentos (Knowledge Base) informada”.
- **B:** “Responda a pergunta solicitada com base no documento que serviu de base para seu funcionamento”.

Os textos são distintos, mas não há capturas que demonstrem quais prompts ou parâmetros estavam efetivamente configurados durante cada resposta. Portanto, não se pode confirmar que o prompt foi a única diferença entre A e B.

#### Saídas e evidências

As 12 respostas foram transcritas em `atividade3/execucao/saidas-brutas/`. Há quatro capturas parciais: A-CT01 (09:01), A-CT02 (09:02), B-CT02 e B-CT04/fonte (horários registrados como 09:13). A captura A-CT01 corrige o horário anteriormente informado como 09:02. As outras oito respostas não têm captura arquivada. As imagens não mostram os prompts nem a configuração completa.

#### Responsabilidade e limitações

A execução estava atribuída a Vinícius. Entretanto, os registros recebidos indicam que Enzo executou e transcreveu as 12 respostas. Não há evidência suficiente para afirmar que Vinícius realizou pessoalmente a execução. Não foram relatadas saídas vazias, erros ou truncamentos nos materiais disponíveis; a ausência de relato não substitui uma verificação das 12 capturas.

As limitações principais são: uma execução por caso/versão; capturas de apenas quatro respostas; falta de prompts/configuração e contextos recuperados; e uso do alias `latest`, cuja revisão pode mudar. Os manifestos A/B registram o que foi informado e o que permanece desconhecido, mas não tornam a execução plenamente reproduzível.

## 3- Rafael Souza Prata

### Bloco 3: F1 lexical, anonimização e gráfico (Parte C)

#### Ferramenta e cálculo

O cálculo foi feito pelo script local `atividade3/metricas/f1_lexical.py`, usando as respostas transcritas e as referências de `casos-e-referencias2.csv`. O script normaliza Unicode em NFC, aplica `casefold`, extrai tokens de palavras e compara as contagens como multiconjuntos.

- **Precisão (P)** = tokens em comum ÷ tokens da resposta.
- **Revocação (R)** = tokens em comum ÷ tokens da referência.
- **F1** = 2 × P × R ÷ (P + R). Se P + R = 0, F1 = 0.
- **Sinal automático** = 1 se F1 ≥ `tau`; caso contrário, 0. Nesta análise, `tau = 0,5` foi escolhido após as execuções.

#### Resultados por caso

| Caso | P(A) | R(A) | F1(A) | Sinal A | P(B) | R(B) | F1(B) | Sinal B |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| CT01 | 0,361111 | 0,634146 | 0,460177 | 0 | 0,351351 | 0,634146 | 0,452174 | 0 |
| CT02 | 0,449275 | 0,885714 | 0,596154 | 1 | 0,469697 | 0,885714 | 0,613861 | 1 |
| CT03 | 0,278261 | 0,864865 | 0,421053 | 0 | 0,323232 | 0,864865 | 0,470588 | 0 |
| CT04 | 0,309524 | 0,684211 | 0,426230 | 0 | 0,333333 | 0,684211 | 0,448276 | 0 |
| CT05 | 0,329787 | 0,704545 | 0,449275 | 0 | 0,426471 | 0,659091 | 0,517857 | 1 |
| CT06 | 0,366337 | 0,902439 | 0,521127 | 1 | 0,362745 | 0,902439 | 0,517483 | 1 |

#### Resumo e interpretação

| Versão | F1 médio (6 respostas) | F1 mediano | Sinal automático positivo | Aprovações R1 reportadas |
|---|---:|---:|---:|---:|
| A | 0,479003 | 0,454726 | 2/6 | 6/6 |
| B | 0,503373 | 0,494036 | 3/6 | 6/6 |

A concordância entre o sinal automático e a aprovação R1 reportada foi 5/12. Como R1 reportou todas as respostas aprovadas, as sete respostas abaixo do limiar são discordâncias. A-CT01 ilustra o limite do F1: R1 reportou aprovação, mas o F1 foi 0,460177, abaixo de 0,5. F1 mede sobreposição de palavras, não verdade, semântica ou suporte factual.

O CSV detalhado está em `atividade3/resultados/f1-lexical.csv`; a tabela consolidada está em `atividade3/resultados/tabela-consolidada.csv`; o gráfico está em `atividade3/resultados/grafico-resultados.svg`.

#### Anonimização e estado da contribuição

A chave de anonimização foi criada após as avaliações para organizar os registros, e não comprova que a avaliação ocorreu às cegas. Ela permanece local e ignorada pelo Git. Embora a Parte 3 estivesse atribuída a Rafael, os cálculos, a consolidação e o gráfico foram preparados no repositório com auxílio de IA/script local. Não há evidência suficiente para atribuir pessoalmente essas etapas a Rafael.

## 4- Thayla Almeida Figueiredo

### Bloco 4: Avaliação humana principal — R1 (Parte D)

#### Procedimento e resultados

Thayla foi a avaliadora R1, conforme esclarecimento do estudante. R1 avaliou as 12 respostas, seis em A e seis em B. Os escores reportados para cada resposta foram correção=2, relevância=2, suporte=2 e falha crítica=0. Pela regra operacional documentada posteriormente, isso corresponde a 6/6 aprovações em A e 6/6 em B.

Os escores foram organizados em `atividade3/avaliacao/r1.csv` após as avaliações, portanto esse arquivo é uma reconstrução retrospectiva, não a ficha original. Não foram fornecidas justificativas ou evidências textuais individuais, e não se deve inventá-las. A rubrica operacional atual também foi formalizada depois da coleta; por isso, os escores são tratados como reportados, não como aplicação verificável de um instrumento pré-registrado.

#### Cegamento e limitações

O estudante relata que a avaliação foi feita às cegas. Porém, os IDs anônimos e a chave local foram criados depois das avaliações e não comprovam o cegamento. A chave não deve ser publicada. Há somente quatro capturas parciais das respostas, e elas não mostram a planilha original de avaliação.

Os resultados humanos disponíveis não mostram aumento de aprovação em B: ambas as versões tiveram 6/6 aprovações reportadas. Isso não prova equivalência ou superioridade, pois a amostra é pequena e as fichas originais e justificativas não foram preservadas.

## 5- Douglas de Oliveira Déda

### Bloco 5: Segunda revisão (R2), comparação, consenso e resultados (Partes D e E)

#### Segunda revisão

Douglas foi o avaliador R2, conforme esclarecimento do estudante. O plano inicial previa uma revisão independente de CT01 e CT05 em A e B, totalizando quatro saídas. Os quatro escores registrados coincidem com os reportados por R1: decisões iguais em 4/4. A justificativa geral reportada foi “Respostas Esperadas e Condizentes”; justificativas e evidências individuais não foram fornecidas. Como nenhuma divergência foi reportada nesse subconjunto, não houve consenso formal.

O estudante informou posteriormente que Douglas confirmou a revisão e avaliou todas as 12 respostas. Os oito escores adicionais não foram transcritos nos arquivos disponíveis; assim, não calculamos a concordância R1–R2 para as 12 respostas. `atividade3/avaliacao/r2.csv` contém apenas os quatro escores do subconjunto inicialmente previsto, reconstruídos retrospectivamente.

#### Respostas às perguntas do estudo

**Q1 — A versão B melhorou a qualidade humana?** R1 reportou 6/6 aprovações tanto em A quanto em B. Portanto, os dados humanos disponíveis não mostram aumento na taxa de aprovação de B. A média de F1 de B foi 0,024370 maior, mas isso é uma diferença descritiva e não demonstra melhora da qualidade.

**Q2 — O F1 representa a avaliação humana?** O sinal automático concordou com R1 em 5/12 respostas. A-CT01 mostra uma limitação: R1 aprovou a resposta, embora seu F1 tenha ficado abaixo de `tau`. Uma resposta pode ser considerada adequada por uma pessoa e ainda compartilhar poucos tokens com a referência. A conclusão é limitada pelas referências sintéticas, pelo limiar pós-hoc e pelos escores humanos retrospectivos.

As 12 saídas não são plenamente independentes: A e B respondem às mesmas perguntas e CT06 é uma variação de CT01. A concordância 4/4 de R1–R2 refere-se somente ao subconjunto com escores transcritos, não às outras oito saídas avaliadas posteriormente por Douglas.

## 6- Enzo Emanuel Maia Costa

### Bloco 6: Ciclo de vida e versionamento mínimo (Parte F)

#### Fluxo documentado

```text
Objetivo e plano -> A (baseline) -> mudança de prompt relatada -> B
       -> 6 casos por versão -> saídas e metadados -> avaliação automática/humana
       -> decisão exploratória -> nova avaliação, monitoramento ou retorno a A
```

O fluxo liga objetivo, versões, execuções, saídas, avaliações e decisão. A rastreabilidade disponível é parcial: os prompts foram informados após as execuções, não há commits/tags A e B anteriores à coleta, e faltam capturas da configuração e dos contextos recuperados. Os manifestos estão em `atividade3/versoes/A/manifesto.md` e `atividade3/versoes/B/manifesto.md`.

#### Reprodução e reversão

Os manifestos registram a versão declarada do aplicativo, o modelo e os prompts informados, mas não permitem reconstruir exatamente as saídas. Os parâmetros completos e os contextos recuperados não foram preservados, e o alias `latest` pode mudar com o tempo.

Em uma nova coleta, a equipe deve congelar e versionar A antes do teste, registrar modelo, parâmetros, base e contexto; depois alterar somente o prompt para B, criar novo commit e só então executar. Para voltar a A, desativar B, restaurar a configuração A documentada e anotar data, motivo e verificação. Não criar tags retroativas como se as configurações atuais tivessem sido congeladas antes das execuções.

#### Responsabilidade e uso de IA

Enzo preparou a documentação de ciclo de vida, manifestos, rastreabilidade e limitações depois das execuções, com auxílio de IA. Também relata ter executado e transcrito as 12 respostas e assumido tarefas de consolidação, cálculo e organização dos resultados. A IA foi usada para preparar documentos e referências sintéticas, estruturar documentação, calcular F1, gerar o gráfico e organizar fichas retrospectivas; não atribuiu notas humanas nem deve ser citada como avaliadora.

## 7- Adam Guilherme Mendes Lima

### Bloco 7: Decisão experimental e consolidação (relatório, repositório e vídeo)

#### Decisão experimental

**Decisão: inconclusiva; não recomendar adoção de B nem declarar superioridade confirmada.** R1 reportou 6/6 aprovações em ambas as versões. B teve F1 médio numericamente maior e um sinal automático positivo a mais, mas o limiar foi escolhido após as execuções, F1 é lexical, as condições A/B não foram verificadas independentemente e as fontes/referências têm limitações de validação. R2 avaliou as 12 respostas posteriormente, mas somente os quatro escores do subconjunto inicial estão transcritos; não há cálculo de concordância para o conjunto completo.

O critério atual para uma possível etapa confirmatória foi definido pós-hoc: considerar B se sua aprovação humana não for inferior à de A e se não houver falha crítica reportada em B. Os resultados transcritos satisfazem esses limites descritivos, mas o critério não foi pré-registrado e não autoriza produção.

#### Contribuição e situação das entregas

A Parte 7 foi atribuída a Adam e inclui decisão, consolidação, relatório final, repositório e vídeo. O texto-base deste relatório e a documentação atual de consolidação foram preparados por Enzo com auxílio de IA. Não há evidência disponível de que Adam tenha concluído pessoalmente essas entregas; por isso, a atribuição nesta seção identifica o responsável previsto, não declara trabalho concluído. Adam e a equipe devem revisar o conteúdo e confirmar as contribuições antes da exportação final.

| Entregável | Estado |
|---|---|
| Texto-base deste relatório | Elaborado; falta revisão final pela equipe |
| Relatório em PDF | Pendente de revisão e exportação |
| Slides | Não fornecidos |
| Vídeo e URL | Pendente; inserir o link em `atividade3/entrega/VIDEO.md` e no README |
| Declarações individuais de uso de IA | Cada integrante deve revisar e completar a sua |
| Revisão de segurança do repositório | Conferir antes da publicação que não há chave, credencial ou dado pessoal |

#### Limitações consolidadas

1. O plano original, o commit pré-teste, o `tau` original e os critérios originais não foram anexados; `tau=0,5`, a rubrica operacional e o critério atual são pós-hoc.
2. DOC-01 e DOC-04 são fontes sintéticas preparadas com IA. A revisão humana das referências é relato sem nome/data; a captura B-CT04 mostra aviso de revisão pendente e campos “PREENCHER”.
3. Há quatro capturas parciais; nenhuma mostra os prompts completos e oito saídas não têm captura arquivada. Parâmetros e contextos recuperados não estão preservados.
4. Não é possível confirmar que A e B diferiram apenas no prompt; os prompts foram informados após as execuções.
5. O alias `latest` não congela a revisão do modelo; houve uma execução por caso/versão.
6. Thayla foi R1 e Douglas foi R2, conforme esclarecimento do estudante. As fichas são reconstruções retrospectivas. Douglas avaliou posteriormente todas as respostas, mas somente quatro escores R2 estão transcritos.
7. A chave de anonimização foi criada após as avaliações e não demonstra cegamento prévio.
8. Seis casos, com CT06 relacionado a CT01, não sustentam generalização nem risco zero.

#### Referências

- van Solingen, R.; Basili, V.; Caldiera, G.; Rombach, H. D. “Goal Question Metric (GQM) Approach.” *Encyclopedia of Software Engineering*, 2002. https://onlinelibrary.wiley.com/doi/abs/10.1002/0471028959.sof142
- National Institute of Standards and Technology. *Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile (AI 600-1)*, 2024. https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf

#### Checklist antes da entrega

- [ ] Cada integrante revisar a seção correspondente ao seu nome e confirmar ou corrigir a contribuição.
- [ ] Confirmar os escores R1 reconstruídos com Thayla e transcrever os oito escores adicionais da revisão de Douglas, sem inferi-los.
- [ ] Conferir que nenhum resultado é descrito como pré-registrado ou confirmado sem evidência.
- [ ] Revisar com o professor as limitações das fontes sintéticas e das fichas retrospectivas.
- [ ] Inserir o gráfico e conferir a legibilidade das tabelas no PDF.
- [ ] Exportar e revisar o relatório final em PDF.
- [ ] Inserir os slides e a URL real do vídeo no `VIDEO.md` e no README.
- [ ] Revisar as declarações individuais de uso de IA.
- [ ] Não publicar a chave de anonimização, credenciais ou dados pessoais.
