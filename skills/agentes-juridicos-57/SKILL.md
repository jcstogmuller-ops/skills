---
name: agentes-juridicos-57
description: Pacote de 57 agentes jurídicos para rotinas de escritório, contencioso, pesquisa, contratos, família, trabalhista, previdenciário, tributário, empresarial, consumidor e execução. Ativa em pedidos como "use os 57 agentes", "instale os agentes", "roteie para agente", "qual agente usar", "orquestre agentes jurídicos" e "biblioteca de agentes jurídicos".
---

# Agentes Jurídicos 57 — Biblioteca Operacional

## Finalidade

Esta skill registra e orquestra os 57 agentes jurídicos do pacote `57 Agents advocacia`, permitindo selecionar o agente adequado conforme a tarefa processual ou administrativa.

A lógica de uso é:

```text
Pedido do usuário → área jurídica → fase processual → agente adequado → produto final
```

## Regras gerais

1. Selecionar o agente mais específico disponível.
2. Não usar agente genérico quando houver agente especializado.
3. Aplicar FIRAC quando houver peça substantiva, recurso, parecer ou manifestação com tese.
4. Aplicar análise de provas quando a tarefa envolver documentos, fatos controvertidos, laudo, audiência ou instrução.
5. Não inventar fatos, documentos, jurisprudência, folhas, IDs ou eventos.
6. Quando faltar informação, sinalizar a lacuna e prosseguir com a melhor estrutura possível.
7. Em tarefas complexas, usar Graphity para ordenar dependências entre agentes.

## Lista dos 57 agentes

| Nº | Agente | Função principal |
|---:|---|---|
| 01 | monitor-dje-djen | Monitoramento de publicações judiciais e diários oficiais |
| 02 | lembrete-prazo | Controle e lembrete de prazos processuais |
| 03 | andamento-processual | Leitura e síntese de andamento processual |
| 04 | intimacao | Análise de intimações e providências cabíveis |
| 05 | ciencia | Petições simples de ciência e registro processual |
| 06 | peticao-inicial-civel | Estruturação de petição inicial cível |
| 07 | contestacao-civel | Defesa cível e contestação ponto a ponto |
| 08 | recurso | Estrutura recursal geral |
| 09 | parecer-juridico | Parecer técnico com riscos, fundamentos e conclusão |
| 10 | procuracao | Procurações, substabelecimentos e poderes |
| 11 | jurisprudencia-stj-stf | Pesquisa e organização de precedentes STF/STJ |
| 12 | doutrina | Organização de fundamento doutrinário |
| 13 | lei-e-sumula | Pesquisa normativa e súmulas aplicáveis |
| 14 | tese-repetitiva | Teses repetitivas e precedentes qualificados |
| 15 | ementario | Organização de ementas e precedentes |
| 16 | triagem-novo-caso | Triagem inicial de novo atendimento ou demanda |
| 17 | orientacao-inicial | Orientação jurídica inicial ao cliente |
| 18 | onboarding-cliente | Entrada de cliente, documentos e briefing |
| 19 | follow-up-cliente | Acompanhamento e comunicação com cliente |
| 20 | revisao-clausula | Revisão de cláusulas contratuais |
| 21 | comparacao-contratos | Comparação entre versões contratuais |
| 22 | direito-digital-lgpd | LGPD, privacidade e direito digital |
| 23 | due-diligence | Due diligence jurídica e documental |
| 24 | cobranca-honorarios | Cobrança de honorários e gestão de recebíveis |
| 25 | agenda-audiencia | Organização de audiência e pauta |
| 26 | resumo-processo | Síntese de autos e linha do tempo processual |
| 27 | backup-escritorio | Rotina de backup e organização documental |
| 28 | apelacao-civel | Apelação cível e estrutura recursal específica |
| 29 | agravo-instrumento | Agravo de instrumento, peças e efeito suspensivo |
| 30 | acao-cobranca | Ação de cobrança e prova da dívida |
| 31 | reclamacao-trabalhista-inicial | Inicial trabalhista |
| 32 | defesa-trabalhista-empregador | Contestação trabalhista pelo empregador |
| 33 | calculo-verbas-rescisorias | Cálculo e conferência de verbas rescisórias |
| 34 | divorcio-consensual | Divórcio consensual e acordo |
| 35 | divorcio-litigioso | Divórcio litigioso e estratégia contenciosa |
| 36 | acao-alimentos | Alimentos, revisão, exoneração e execução |
| 37 | inventario-extrajudicial | Inventário extrajudicial e documentação |
| 38 | guarda-compartilhada | Guarda, convivência e melhor interesse |
| 39 | defesa-criminal-resposta-acusacao | Resposta à acusação e teses defensivas |
| 40 | habeas-corpus | Habeas corpus e constrangimento ilegal |
| 41 | mandado-seguranca-tributario | Mandado de segurança tributário |
| 42 | embargos-execucao-fiscal | Embargos à execução fiscal |
| 43 | recuperacao-judicial-empresarial | Recuperação judicial empresarial |
| 44 | contrato-social-elaboracao | Elaboração de contrato social |
| 45 | acordo-acionistas | Acordo de acionistas e governança |
| 46 | acao-cdc-pratica-abusiva | Ação consumerista por prática abusiva |
| 47 | acao-despejo | Despejo, locação e retomada do imóvel |
| 48 | acao-renovatoria-locacao | Ação renovatória de locação empresarial |
| 49 | usucapiao-extrajudicial | Usucapião extrajudicial |
| 50 | usucapiao-judicial | Usucapião judicial |
| 51 | aposentadoria-tempo-contribuicao | Aposentadoria por tempo de contribuição |
| 52 | bpc-loas | BPC/LOAS e vulnerabilidade social |
| 53 | auxilio-doenca-recurso | Recurso em auxílio-doença/incapacidade |
| 54 | cumprimento-sentenca | Cumprimento de sentença |
| 55 | impugnacao-cumprimento-sentenca | Impugnação ao cumprimento de sentença |
| 56 | calculo-judicial-atualizacao | Atualização de cálculos judiciais |
| 57 | minuta-contrato-servicos | Minuta de contrato de prestação de serviços |

## Roteamento por tarefa

| Tarefa | Agente principal | Agentes auxiliares |
|---|---|---|
| Analisar processo completo | 26-resumo-processo | 03-andamento-processual, analise-de-provas, firac |
| Responder intimação | 04-intimacao | 03-andamento-processual, 05-ciencia, sistema-de-criacao-de-peticoes-e-recursos |
| Criar inicial cível | 06-peticao-inicial-civel | 11-jurisprudencia-stj-stf, 13-lei-e-sumula, pecas-persuasivas |
| Criar contestação | 07-contestacao-civel | analise-de-provas, firac |
| Interpor recurso | 08-recurso | 28-apelacao-civel, 29-agravo-instrumento, firac |
| Pesquisa de tese | 11-jurisprudencia-stj-stf | 12-doutrina, 13-lei-e-sumula, 14-tese-repetitiva |
| Audiência | 25-agenda-audiencia | analise-de-provas, 26-resumo-processo |
| Execução/cálculo | 54-cumprimento-sentenca | 55-impugnacao-cumprimento-sentenca, 56-calculo-judicial-atualizacao |
| Família | 34-divorcio-consensual | 35-divorcio-litigioso, 36-acao-alimentos, 38-guarda-compartilhada |
| Previdenciário | 51-aposentadoria-tempo-contribuicao | 52-bpc-loas, 53-auxilio-doenca-recurso |
| Tributário | 41-mandado-seguranca-tributario | 42-embargos-execucao-fiscal, 14-tese-repetitiva |
| Empresarial | 43-recuperacao-judicial-empresarial | 44-contrato-social-elaboracao, 45-acordo-acionistas, 23-due-diligence |

## Saída padrão ao acionar a biblioteca

Sempre informar:

1. agente selecionado;
2. razão da seleção;
3. agentes auxiliares necessários;
4. dados mínimos exigidos;
5. produto final esperado;
6. riscos ou lacunas;
7. próxima providência.

## Integração com Graphity

Em casos com mais de três agentes, aplicar Graphity para montar o grafo de execução:

```yaml
workflow:
  objective: [objetivo]
  nodes:
    - id: [agente]
      role: [função]
  edges:
    - from: [agente-a]
      to: [agente-b]
      relation: produces_input_for
```

## Regra final

Esta skill funciona como índice operacional e camada de roteamento dos 57 agentes jurídicos. Quando o conteúdo integral de um agente específico estiver disponível no repositório, ele deve prevalecer sobre esta descrição resumida.
