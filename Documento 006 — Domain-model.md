# Modelo de Domínio

## Objetivo

Este documento descreve os principais conceitos do domínio do EduData AI.

Ele representa o conhecimento do negócio e não a implementação em código.

As entidades aqui descritas deverão permanecer estáveis ao longo do tempo, independentemente da linguagem de programação, banco de dados ou modelo de Inteligência Artificial utilizado.

---

# Visão Geral

O EduData AI possui um único objetivo de negócio:

**Identificar automaticamente quais candidatos aprovados pertencem ao Colégio Olimpo.**

Todo o restante do sistema existe para suportar esse processo.

---

# Entidades do Domínio

## Base Institucional

Representa a relação oficial de alunos do Colégio Olimpo.

É a principal fonte de verdade utilizada durante o cruzamento de dados.

### Responsabilidades

- Armazenar os alunos do Colégio Olimpo.
- Servir como referência para o cruzamento.
- Permitir identificação da turma de cada aluno.

---

## Aluno

Representa um estudante pertencente ao Colégio Olimpo.

Um aluno pode ou não aparecer em listas oficiais de aprovados.

### Informações esperadas

- Nome
- Turma
- Ano letivo (quando aplicável)

---

## Processo Seletivo

Representa um vestibular ou seleção acadêmica.

Exemplos:

- PAS/UnB
- UFU
- ENEM
- FUVEST
- PUC-Rio

Cada Processo Seletivo possui regras próprias de publicação dos resultados.

---

## Lista Oficial

Documento publicado oficialmente contendo candidatos aprovados.

Atualmente o EduData AI trabalha apenas com listas em formato PDF.

Cada Lista Oficial pertence a um Processo Seletivo.

---

## Aprovado

Representa um candidato identificado na Lista Oficial.

Um Aprovado não é necessariamente um aluno do Colégio Olimpo.

Essa confirmação ocorre apenas após o cruzamento.

---

## Extração

Processo responsável por transformar um documento PDF em dados estruturados.

Essa etapa utiliza exclusivamente um modelo de IA Local.

O EduData AI não toma decisões durante esta etapa.

---

## Normalização

Processo responsável por padronizar os dados extraídos.

Exemplos:

- espaços extras
- caracteres especiais
- padronização de nomes
- ajustes de formatação

A normalização prepara os dados para o cruzamento.

---

## Cruzamento

Principal processo do EduData AI.

Consiste na comparação entre:

- Base Institucional
- Lista Oficial

O objetivo é identificar quais aprovados pertencem ao Colégio Olimpo.

Este é o núcleo da lógica de negócio do sistema.

---

## Relatório

Documento produzido após o cruzamento.

Seu conteúdo apresenta os alunos identificados e demais informações relevantes para análise.

---

# Fluxo do Domínio

Base Institucional

+

Lista Oficial

↓

Extração

↓

Normalização

↓

Cruzamento

↓

Relatórios

---

# Regra Central do Sistema

Toda funcionalidade implementada deverá contribuir direta ou indiretamente para o processo de cruzamento entre a Base Institucional e a Lista Oficial.

Caso uma funcionalidade não contribua para esse objetivo, sua inclusão deverá ser justificada.
