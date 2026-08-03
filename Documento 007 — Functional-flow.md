# Fluxo Funcional

## Objetivo

Este documento descreve o fluxo funcional do EduData AI.

O objetivo é representar como o trabalho é realizado do ponto de vista do usuário e das regras de negócio, sem considerar detalhes de implementação.

---

# Visão Geral

O EduData AI recebe uma Lista Oficial de aprovados e identifica automaticamente quais candidatos pertencem ao Colégio Olimpo.

Todo o fluxo é iniciado manualmente pelo Analista de Dados.

---

# Fluxo Principal

## Etapa 1 — Recebimento da Lista Oficial

O Analista recebe um documento oficial contendo os candidatos aprovados em um Processo Seletivo.

Atualmente esse documento é fornecido em formato PDF.

Exemplos:

- UFU
- PAS/UnB
- ENEM
- PUC-Rio

---

## Etapa 2 — Seleção da Base Institucional

O sistema utiliza a Base Institucional do Colégio Olimpo.

Essa base representa a fonte oficial de alunos ativos utilizada para o cruzamento.

Atualmente a Base Institucional é fornecida em formato PDF.

---

## Etapa 3 — Extração

A Lista Oficial é enviada ao modelo de IA Local.

A IA possui apenas uma responsabilidade:

Transformar o documento PDF em dados estruturados.

Nesta etapa nenhuma decisão de negócio é realizada.

---

## Etapa 4 — Validação

Os dados extraídos são verificados.

Exemplos:

- estrutura válida
- campos obrigatórios
- registros incompletos
- inconsistências

Caso existam erros, o processo deverá informar o usuário.

---

## Etapa 5 — Normalização

Após a validação, os dados são padronizados.

Exemplos:

- remoção de espaços excedentes
- padronização de caracteres
- padronização de nomes
- tratamento de acentos
- ajuste de capitalização

O objetivo é preparar os dados para o cruzamento.

---

## Etapa 6 — Cruzamento

Esta é a principal etapa do EduData AI.

Os candidatos aprovados são comparados com a Base Institucional.

Como resultado, o sistema identifica:

- alunos do Colégio Olimpo;
- candidatos não pertencentes ao Colégio;
- casos que necessitam de revisão.

---

## Etapa 7 — Geração dos Relatórios

Após o cruzamento, o sistema gera os documentos finais.

Os relatórios devem conter apenas informações relevantes para análise.

---

## Etapa 8 — Exportação

Os resultados são exportados nos formatos definidos pelo projeto.

Os arquivos produzidos deverão ser reproduzíveis.

---

# Fluxo Resumido

Receber Lista Oficial

↓

Extrair informações

↓

Validar

↓

Normalizar

↓

Cruzar com Base Institucional

↓

Gerar Relatórios

↓

Exportar Resultados

---

# Responsabilidades

## Analista de Dados

- selecionar os documentos;
- iniciar o processamento;
- analisar os resultados;
- encaminhar os relatórios.

---

## IA Local

- interpretar documentos;
- extrair informações estruturadas.

Não realiza decisões de negócio.

---

## EduData AI

- validar dados;
- normalizar informações;
- realizar o cruzamento;
- produzir relatórios;
- exportar resultados.

---

# Regra Fundamental

Nenhuma etapa poderá modificar o resultado do cruzamento sem justificativa documentada.

O cruzamento representa a principal regra de negócio do EduData AI.
