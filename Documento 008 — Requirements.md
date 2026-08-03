# Requisitos do Sistema

## Objetivo

Este documento define os requisitos funcionais e não funcionais do EduData AI.

Ele representa o contrato do sistema.

Toda funcionalidade implementada deverá atender aos requisitos aqui definidos.

---

# Requisitos Funcionais

## RF-001 — Processamento de Lista Oficial

O sistema deverá receber uma Lista Oficial de aprovados fornecida manualmente pelo usuário.

---

## RF-002 — Processamento da Base Institucional

O sistema deverá utilizar uma Base Institucional contendo os alunos do Colégio Olimpo.

Essa base será utilizada como referência para o cruzamento.

---

## RF-003 — Extração de Dados

O sistema deverá utilizar um modelo de IA Local para extrair informações estruturadas dos documentos.

---

## RF-004 — Validação

O sistema deverá validar os dados extraídos antes do início do cruzamento.

---

## RF-005 — Normalização

O sistema deverá padronizar os dados antes da comparação.

---

## RF-006 — Cruzamento

O sistema deverá identificar quais aprovados pertencem ao Colégio Olimpo.

Este é o principal requisito funcional do projeto.

---

## RF-007 — Geração de Relatórios

O sistema deverá gerar relatórios contendo os resultados do cruzamento.

---

## RF-008 — Exportação

O sistema deverá exportar os resultados em formatos definidos pelo projeto.

---

## RF-009 — Registro de Processamento

O sistema deverá registrar informações suficientes para permitir auditoria e rastreabilidade do processamento.

---

# Requisitos Não Funcionais

## RNF-001 — Execução Local

O sistema deverá funcionar integralmente em ambiente local.

---

## RNF-002 — IA Local

Nenhum serviço externo será obrigatório para execução.

A extração será realizada utilizando um modelo de IA Local.

---

## RNF-003 — Reprodutibilidade

Um mesmo conjunto de entradas deverá produzir o mesmo resultado.

---

## RNF-004 — Modularidade

O sistema deverá permitir inclusão de novos Processos Seletivos sem necessidade de alterar a lógica principal.

---

## RNF-005 — Manutenibilidade

A arquitetura deverá facilitar manutenção e evolução.

---

## RNF-006 — Simplicidade

Sempre será escolhida a solução mais simples que atenda ao problema.

---

## RNF-007 — Documentação

Toda decisão arquitetural relevante deverá ser documentada.

---

## RNF-008 — Confiabilidade

O cruzamento deverá priorizar precisão e rastreabilidade em vez de velocidade.

---

## RNF-009 — Escalabilidade Controlada

O sistema deverá crescer apenas quando houver necessidade real.

Novas funcionalidades não poderão aumentar a complexidade sem justificativa.

---

# Restrições

- O sistema não realizará busca automática de documentos.
- O usuário fornecerá manualmente os arquivos.
- O foco atual é exclusivamente em listas oficiais de aprovados.
- O sistema possui apenas um usuário.
- Toda regra de negócio pertence ao EduData AI.
- A IA Local é utilizada exclusivamente para extração de informações.
