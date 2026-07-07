---
name: graphity
description: Skill de orquestração estrutural para bibliotecas de skills e agentes. Organiza dependências, gatilhos, hierarquia, sequência de execução, recuperação contextual e governança de múltiplas skills/agentes em tarefas complexas. Ativa em pedidos como "graphity", "grafo de skills", "orquestre as skills", "mapear agentes", "rotear tarefa", "dependências entre skills", "instalar agentes" e "organizar biblioteca de skills".
---

# Graphity — Orquestração por Grafo de Skills e Agentes

## Finalidade

A skill Graphity organiza uma biblioteca de skills e agentes como um grafo operacional, permitindo selecionar o conjunto mínimo e correto de capacidades para cada tarefa complexa.

Em vez de carregar todas as skills de forma indiscriminada, o Graphity identifica:

```text
Tarefa → intenção → skills candidatas → dependências → ordem de execução → saída esperada
```

## Contexto técnico

O uso de grafos para organização de skills vem sendo tratado como alternativa ao carregamento integral de bibliotecas extensas. Trabalhos recentes descrevem modelos de recuperação estrutural e dependente de contexto para selecionar skills por relação, dependência e coocorrência, reduzindo excesso de contexto e aumentando precisão operacional.

## Quando usar

Aplicar Graphity quando houver:

- múltiplas skills possíveis;
- tarefa jurídica complexa;
- necessidade de decompor fluxo;
- repositório com muitos agentes;
- instalação ou auditoria de biblioteca de skills;
- criação de manifesto;
- roteamento entre agentes;
- organização de pipeline jurídico;
- risco de sobreposição entre competências.

## Modelo de grafo

Cada skill/agente deve ser tratado como nó:

```yaml
id: nome-da-skill-ou-agente
type: skill | agent | workflow | tool
triggers:
  - gatilho principal
inputs:
  - dados necessários
outputs:
  - produto esperado
dependencies:
  - skill-ou-agente-precedente
conflicts:
  - skill-ou-agente-incompatível
priority: baixa | média | alta | crítica
```

## Tipos de relação

| Relação | Significado |
|---|---|
| prerequisite | Deve ser executada antes |
| enhances | Melhora a saída de outra skill |
| validates | Audita ou revisa a saída |
| conflicts | Não deve ser usada simultaneamente sem critério |
| routes_to | Encaminha para agente especializado |
| produces_input_for | Produz insumo para a próxima etapa |

## Fluxo operacional

1. Identificar a tarefa principal.
2. Extrair intenção dominante e intenções secundárias.
3. Selecionar skills/agentes candidatos.
4. Remover duplicidades funcionais.
5. Definir dependências.
6. Ordenar execução.
7. Definir produto final.
8. Registrar lacunas.
9. Executar o fluxo mínimo suficiente.
10. Revisar consistência entre entrada, processamento e saída.

## Roteamento jurídico padrão

| Tarefa | Skill/agente inicial | Validação |
|---|---|---|
| Analisar autos | analise-completa-de-processos-juridicos-com-ia | firac + analise-de-provas |
| Criar peça | sistema-de-criacao-de-peticoes-e-recursos | pecas-persuasivas + firac |
| Revisar recurso | revisor-de-recursos | firac + prequestionamento |
| Manifestação em provas | analise-de-provas | firac |
| Organização de rotina | organizacao-de-processos-juridicos | graphity |
| Estratégia de caso | sistema-de-analise-estrategica-de-casos | matriz de risco |

## Saída padrão

Ao aplicar Graphity, entregar:

```text
1. Intenção principal
2. Skills/agentes ativados
3. Ordem de execução
4. Dependências
5. Pontos de validação
6. Saída final esperada
7. Riscos de sobreposição ou lacuna
```

## Manifesto mínimo

```yaml
workflow:
  name: [nome]
  objective: [objetivo]
  nodes:
    - id: [skill]
      role: [função]
      input: [entrada]
      output: [saída]
  edges:
    - from: [skill-a]
      to: [skill-b]
      relation: produces_input_for
  validation:
    - [critério]
```

## Regras de segurança

1. Não ativar agente sem pertinência funcional.
2. Não duplicar etapas com nomes diferentes e mesma função.
3. Priorizar a skill mais específica sobre a genérica.
4. Em conflito entre análise ampla e regra especializada, aplicar a regra especializada.
5. Registrar lacuna quando o agente ou skill de origem não estiver disponível.
6. Não inventar conteúdo de agente ausente.

## Regra final

Graphity é a camada de governança. Ele não substitui a análise jurídica; ele escolhe, ordena e audita as skills e agentes necessários para que a análise seja executada com menor ruído e maior coerência.
