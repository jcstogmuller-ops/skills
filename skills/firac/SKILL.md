---
name: firac
version: 4.0
short_name: FIRAC
category: juridico-raciocinio-estruturado
status: permanente
priority: alta
description: >
  Aplica o método FIRAC como protocolo de raciocínio jurídico estruturado para peças,
  pareceres, estratégias processuais e revisão técnica. Opera em duas camadas: (1) bloco
  FIRAC de primeira página, com até 100 palavras, obrigatório no topo de peças substantivas;
  (2) FIRAC analítico completo, para estudo do caso, decomposição de questões complexas,
  construção de tese, revisão de sentença, recursos, contestações, iniciais, embargos,
  memoriais e manifestações complexas.
triggers:
  - /firac
  - gera o FIRAC
  - aplique o FIRAC
  - aplique o método FIRAC
  - método FIRAC
  - análise FIRAC
  - bloco FIRAC
  - FIRAC de abertura
  - resumo de primeira página
  - resumo do caso
  - síntese FIRAC
  - cabeçalho FIRAC
  - organizar pelo FIRAC
  - estruturar pelo FIRAC
  - FIRAC analítico
  - FIRAC completo
  - resumo técnico de abertura
  - parágrafo-tese de abertura
  - primeira página FIRAC
---

# FIRAC V4 — Protocolo Operacional de Raciocínio Jurídico Estruturado

## 1. Finalidade

A skill transforma fatos, documentos, pedidos e decisões em raciocínio jurídico claro, verificável e orientado ao julgamento.

O FIRAC deve servir simultaneamente a três funções:

1. **Organizar o raciocínio do advogado** antes da redação da tese.
2. **Orientar o magistrado** logo na primeira leitura da peça.
3. **Fixar a tese principal nos primeiros parágrafos**, favorecendo leitura, triagem e indexação por sistemas de IA judicial.

A IA atua apenas como instrumento de apoio. Toda conclusão deve permanecer dependente da revisão crítica do advogado, dos documentos dos autos e da aderência aos pedidos reais da peça.

---

## 2. Princípio central

O FIRAC não é resumo decorativo. É o esqueleto lógico da peça.

Nenhuma peça substantiva deve avançar sem conexão verificável entre:

```text
Fato provado → questão jurídica → regra aplicável → aplicação dedutiva → pedido coerente
```

---

## 3. Camadas de aplicação

### 3.1. Camada 1 — FIRAC de primeira página

Usar no topo de qualquer peça jurídica substantiva, **antes do endereçamento ao juízo**.

Características:

- até 100 palavras;
- formato F/I/R/A/C;
- direto, técnico e verificável;
- sem adjetivação;
- alinhado aos pedidos finais;
- máximo de 2 fatos;
- máximo de 3 referências jurídicas;
- obrigatório em peças que busquem convencimento judicial.

### 3.2. Camada 2 — FIRAC analítico completo

Usar para análise interna, parecer, estudo de caso, construção de tese, revisão de sentença, estratégia recursal, contestação, inicial, embargos, memoriais, produção de provas, auditoria contábil judicial e manifestações complexas.

Características:

- admite desenvolvimento técnico;
- inclui pontos controvertidos;
- permite subquestões;
- permite matriz probatória;
- exige direito aplicável seguro;
- explicita riscos, lacunas e limites dos documentos;
- conclui com providência jurídica específica.

---

## 4. Modo de escolha automática

| Situação | Camada aplicada |
|---|---|
| Criação de peça processual substantiva | Camada 1 no topo + Camada 2 como base interna, se necessário |
| Usuário pede apenas “resumo”, “cabeçalho”, “primeira página” | Camada 1 |
| Usuário pede “análise”, “parecer”, “estratégia”, “estudo do caso” | Camada 2 |
| Usuário pede recurso, contestação, inicial, embargos ou memoriais | Camada 1 na peça + Camada 2 para construir a tese |
| Peça existente sem FIRAC | Inserir Camada 1 no topo sem alterar o restante |
| Peça formal isenta | Não aplicar FIRAC, salvo pedido expresso do usuário |

---

## 5. Os cinco movimentos

| Letra | Movimento | Função | Limite na Camada 1 | Regra crítica |
|---|---|---|---|---|
| F | Fatos | Identificar fatos objetivos, verificáveis e juridicamente relevantes | Até 2 fatos | Não qualificar juridicamente o fato |
| I | Issue / Questão Jurídica | Formular a pergunta que decide o caso | 1 pergunta | Pergunta direta, sem retórica |
| R | Regras | Indicar direito aplicável seguro | Até 3 referências | Nunca inventar precedente, tema ou súmula |
| A | Análise | Conectar fatos e regras por lógica dedutiva | 1 ou 2 frases | Demonstrar, não adjetivar |
| C | Conclusão | Fixar desfecho pretendido | 1 frase | Deve coincidir com os requerimentos |

---

## 6. Regras de segurança jurídica

1. Não inventar fatos.
2. Não inventar jurisprudência.
3. Não inventar súmula, tema, tese, precedente, número de julgado ou ementa.
4. Não extrapolar documentos, briefing ou dados processuais fornecidos.
5. Quando faltar dado, indicar a lacuna e prosseguir com a melhor análise possível.
6. Quando precedente específico for desconhecido, escrever: **“Incerteza quanto à existência de precedente específico.”**
7. Quando houver conflito entre conclusão FIRAC e requerimentos finais, prevalece o pedido real da peça.
8. Usar texto técnico, direto, sem adjetivação, sem retórica vazia e sem dramatização.
9. Não usar “jurisprudência pacífica”, “entendimento consolidado” ou expressões equivalentes sem fonte segura.
10. Não inserir tese nova no FIRAC que não será sustentada no corpo da peça.
11. Não omitir fato desfavorável essencial quando ele for decisivo para risco, admissibilidade ou mérito.
12. Em recursos, não formular C sem pedido recursal claro: reforma, anulação, integração, esclarecimento ou prequestionamento.

---

## 7. Formato obrigatório — Camada 1

```text
─────────────────────────────────────────────────────────
RESUMO DO CASO — MÉTODO FIRAC
─────────────────────────────────────────────────────────
F: [Fato central verificável. Fato secundário se necessário.]

I: [Controvérsia jurídica formulada como pergunta direta?]

R: [Norma 1; Norma 2; precedente seguro ou “Incerteza quanto à existência de precedente específico.”]

A: [Fatos provam X; norma exige Y; portanto Z.]

C: [Desfecho específico: tutela, declaração, condenação, anulação, reforma, integração, desbloqueio, homologação ou improcedência.]
─────────────────────────────────────────────────────────
[XX palavras]
```

### 7.1. Regras de contagem

Contar apenas o conteúdo dos campos F, I, R, A e C. Não contar título, linhas separadoras nem marcador final de palavras.

### 7.2. Ordem de corte se passar de 100 palavras

1. Cortar conectivos dispensáveis.
2. Reduzir R para as referências indispensáveis.
3. Reduzir A para uma frase dedutiva.
4. Reduzir F para o fato central.
5. Preservar C sempre que possível.

---

## 8. Formato recomendado — Camada 2

```text
## ANÁLISE PELO MÉTODO FIRAC

### F — Fatos juridicamente relevantes
- [Fato 1] — prova/documento: [ID, fls., anexo ou “não indicado”].
- [Fato 2] — prova/documento: [ID, fls., anexo ou “não indicado”].
- [Fato desfavorável relevante, se existir] — impacto: [risco].

### I — Questão jurídica central
[Uma pergunta principal que o julgador precisa responder.]

### Subquestões, se necessárias
1. [Pergunta auxiliar 1]
2. [Pergunta auxiliar 2]
3. [Pergunta auxiliar 3]

### Pontos controvertidos
| Ponto | Quem afirma | Prova indicada | Ônus probatório | Risco |
|---|---|---|---|---|
| [ponto] | [parte] | [prova] | [art. 373 CPC, CLT, CPP ou regra aplicável] | [baixo/médio/alto] |

### R — Direito aplicável
- [Norma constitucional, se pertinente]
- [Lei/artigo aplicável]
- [Súmula, tema ou precedente seguro]
- [Se não houver segurança: “Incerteza quanto à existência de precedente específico.”]

### A — Aplicação das normas aos fatos
[Demonstrar o encaixe entre fato provado, requisito normativo e consequência jurídica.]

### C — Conclusão técnica
[Conclusão específica, com pedido coerente, risco processual e providência recomendada.]
```

---

## 9. Engenharia de prompt para uso eficiente

Quando o usuário pedir aplicação do FIRAC, preferir trabalhar com este conjunto mínimo de dados:

1. tipo de peça ou finalidade;
2. parte representada;
3. fase processual;
4. fatos essenciais;
5. documentos que comprovam cada fato;
6. decisão, sentença ou ato a combater, quando houver;
7. pedido pretendido;
8. pontos controvertidos;
9. riscos conhecidos;
10. limites: não extrapolar documentos e não inventar jurisprudência.

Se algum dado faltar, a skill deve prosseguir e sinalizar a lacuna de modo objetivo.

---

## 10. Decomposição obrigatória em casos complexos

Usar quando houver múltiplos pedidos, várias teses, decisão longa, prova técnica, cálculo, recurso ou matéria de ordem pública.

Perguntas de decomposição:

1. Qual fato decide o caso?
2. Esse fato está provado por qual documento?
3. Quem tem o ônus de provar esse fato?
4. Qual norma exige ou dispensa essa prova?
5. A decisão recorrida enfrentou esse ponto?
6. Existe vício: omissão, contradição, obscuridade, erro material, error in judicando ou error in procedendo?
7. Qual pedido corrige o problema?
8. Qual risco existe se o ponto não for tratado?

A decomposição pode ser silenciosa no bloco de primeira página. Deve aparecer expressamente quando o usuário pedir análise, parecer, estratégia ou revisão.

---

## 11. Adaptação por tipo de peça

| Peça | F | I | R | A | C |
|---|---|---|---|---|
| Inicial | Fato gerador do direito | Lesão, ameaça, inadimplemento ou resistência | Fundamento legal do pedido | Demonstração dos requisitos da pretensão | Tutela, declaração, condenação ou obrigação pretendida |
| Contestação | Fato impeditivo, modificativo ou extintivo | Ausência de direito, ilegitimidade, prescrição, decadência ou insuficiência probatória | Regra defensiva central | Confronto entre ônus da prova e falhas da inicial | Improcedência, extinção, limitação ou acolhimento de preliminar |
| Réplica | Fato/prova que neutraliza a defesa | Persistência do direito apesar da contestação | Norma que afasta preliminar ou mérito defensivo | Demonstração da insuficiência defensiva | Rejeição da defesa e procedência |
| Recurso | Fundamento decisório e ponto impugnado | Erro de julgamento, procedimento, omissão ou contradição | Norma violada + precedente seguro | Demonstração do equívoco decisório | Reforma, anulação, integração, prequestionamento ou efeito suspensivo |
| Contrarrazões | Acerto da decisão recorrida | Ausência de erro recursal ou inadmissibilidade | Regra de manutenção da decisão | Demonstração de que o recurso não supera os fundamentos | Desprovimento ou não conhecimento |
| Embargos de declaração | Trecho com omissão, contradição, obscuridade ou erro material | Vício integrativo | CPC art. 1.022 + norma omitida | Relação entre vício, prejuízo e necessidade de integração | Integração, correção, esclarecimento e prequestionamento |
| Manifestação substantiva | Ato processual que exige resposta | Providência jurisdicional necessária | Norma processual aplicável | Razão pela qual a providência é devida | Deferimento da providência específica |
| Memoriais | Prova central produzida | Ponto que decide o mérito | Regra decisória mais segura | Síntese da prova vencedora | Julgamento favorável |
| Produção de provas | Fato controvertido | Prova necessária para resolver o ponto | Ônus probatório e norma processual | Necessidade, pertinência e utilidade da prova | Deferimento da prova |
| Auditoria contábil judicial | Comando judicial e cálculo apresentado | Erro metodológico, matemático ou de indexação | Parâmetro da decisão e regra de atualização | Demonstração do desvio numérico | Correção, homologação alternativa ou perícia |
| Execução/cumprimento | Título, obrigação e inadimplemento | Exigibilidade, excesso, nulidade ou satisfação | Título judicial/extrajudicial + regra executiva | Confronto entre título, cálculo e atos constritivos | Prosseguimento, desbloqueio, impugnação ou extinção |
| Penal | Fato imputado e prova central | Tipicidade, autoria, materialidade, nulidade ou medida cautelar | CPP/CP/CF e precedente seguro | Confronto entre prova, tipo penal e garantia processual | Absolvição, nulidade, revogação, relaxamento ou desclassificação |

---

## 12. Matriz de consistência obrigatória

Antes de entregar qualquer FIRAC, verificar internamente:

| Critério | Pergunta de controle | Ação se falhar |
|---|---|---|
| Fatos | Os fatos são verificáveis e não opinativos? | Reescrever sem adjetivos |
| Prova | Há indicação documental quando disponível? | Inserir ID/fls./anexo ou sinalizar lacuna |
| Issue | A questão está em forma de pergunta direta? | Converter em pergunta objetiva |
| Regras | As referências são reais, seguras e essenciais? | Remover referência insegura |
| Análise | Há conexão lógica entre fatos, regras e conclusão? | Reescrever em fórmula dedutiva |
| Conclusão | O desfecho coincide com os pedidos finais? | Alinhar ao pedido real |
| Limite | O bloco de primeira página tem até 100 palavras? | Cortar conforme ordem do item 7.2 |
| Segurança | Houve invenção de fato, tese, tema, súmula ou precedente? | Excluir e sinalizar incerteza |
| Estratégia | A tese principal aparece no primeiro campo útil? | Reordenar F e C |

---

## 13. Isenções

Não aplicar FIRAC automaticamente em atos meramente formais:

1. petição de ciência;
2. manifestação de ciência;
3. mera juntada de documentos;
4. substabelecimento;
5. procuração simples;
6. certidão;
7. declaração sem argumentação;
8. pedido de vista;
9. pedido de carga;
10. habilitação simples sem tese;
11. correção cadastral sem argumentação;
12. requerimento administrativo simples sem tese;
13. pedido de expedição de guia, salvo se houver controvérsia;
14. pedido de desarquivamento simples;
15. comunicação de endereço sem pedido controvertido;
16. renúncia simples sem fundamentação;
17. desistência simples sem tese jurídica;
18. petição de regularização formal sem debate jurídico.

Se o ato formal contiver tese, resistência, pedido controvertido ou risco de indeferimento, aplicar FIRAC.

---

## 14. Integração com o sistema jurídico do escritório

| Skill/componente | Integração |
|---|---|
| `peticoes-ia-judicial.md` | FIRAC é Fase 1 obrigatória da produção de peça substantiva |
| `/pecas-persuasivas` | FIRAC é item A1 do Bloco A e pesa no score de assertividade |
| `/teste-peticao` | Critério C2 verifica tese de abertura, coerência e aderência ao pedido |
| `Revisor de Recursos` | Identifica fundamento recorrido, vício, norma violada e pedido recursal |
| `Produção de Provas` | Conecta fato controvertido, ônus probatório e prova necessária |
| `Auditor Contábil Judicial` | Conecta comando judicial, erro de cálculo e correção pretendida |
| `FIRAC-01` | Bloco obrigatório de primeira página |
| `PIFE` | O campo A deve usar prova, inferência, fundamento e efeito |
| `TR-01` | Valida tema, fatos, fundamentos, pedidos, palavras-chave e suficiência |
| `RCD-01` | Reforça conclusão decisória e critério provável do julgador |

---

## 15. Saída quando houver lacunas

Não paralisar a entrega. Usar uma das fórmulas:

```text
Informação insuficiente para indicar o documento comprobatório do fato.
```

```text
Informação insuficiente para quantificar o pedido.
```

```text
Incerteza quanto à existência de precedente específico.
```

```text
Não há, nos dados fornecidos, identificação segura do ID/fls. do documento.
```

A lacuna deve ser objetiva, curta e vinculada ao ponto faltante.

---

## 16. Exemplo — FIRAC de primeira página

```text
─────────────────────────────────────────────────────────
RESUMO DO CASO — MÉTODO FIRAC
─────────────────────────────────────────────────────────
F: A autora quitou a obrigação em 14/03/2024, mas a ré manteve a negativação após a baixa do débito.

I: A manutenção da restrição após quitação comprovada gera dever de indenizar?

R: CDC art. 43, § 3º; CC arts. 186 e 927; Incerteza quanto à existência de precedente específico.

A: A quitação afasta a legitimidade da restrição; a manutenção do apontamento viola o dever de correção cadastral.

C: Requer-se cancelamento da negativação e condenação por dano moral.
─────────────────────────────────────────────────────────
[74 palavras]
```

---

## 17. Exemplo — FIRAC analítico completo resumido

```text
## ANÁLISE PELO MÉTODO FIRAC

### F — Fatos juridicamente relevantes
- O comprador adquiriu imóvel na planta em 2019, com entrega prevista para dezembro de 2021 e tolerância de 180 dias.
- A entrega atrasou mais de 12 meses, e a construtora atribuiu a mora à pandemia.

### I — Questão jurídica central
A pandemia justifica atraso superior ao prazo contratual de tolerância e impede a rescisão com devolução integral dos valores pagos?

### Pontos controvertidos
| Ponto | Quem afirma | Prova indicada | Ônus probatório | Risco |
|---|---|---|---|---|
| Força maior | Construtora | Não indicada | Construtora | Médio |
| Atraso superior ao prazo tolerado | Comprador | Contrato e cronograma | Comprador | Baixo, se documentado |

### R — Direito aplicável
- CDC arts. 6º, III e VI, 14 e 51.
- CC arts. 393, 475 e 884.
- Incerteza quanto à existência de precedente específico.

### A — Aplicação das normas aos fatos
A cláusula de tolerância absorve atrasos ordinários. A força maior exige prova concreta de nexo causal entre pandemia e impossibilidade específica de entrega. Sem essa prova, o atraso prolongado configura inadimplemento substancial e autoriza rescisão.

### C — Conclusão técnica
A solução mais segura é requerer rescisão por culpa da construtora, devolução integral dos valores pagos, correção monetária, juros e eventual indenização se comprovado dano autônomo.
```

---

## 18. Regra final de entrega

Ao entregar peça jurídica substantiva, incluir o bloco FIRAC no topo.

Ao entregar análise, parecer ou estratégia, usar FIRAC analítico completo.

Ao entregar ambos, primeiro apresentar o FIRAC de primeira página e depois desenvolver a análise.
