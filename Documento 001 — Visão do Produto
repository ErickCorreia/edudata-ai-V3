# 🎓 EduData AI

> **Documento de Visão do Produto**

O **EduData AI** é uma ferramenta interna desenvolvida para automatizar a identificação de alunos do **Colégio Olimpo** aprovados em processos seletivos brasileiros.

---

# 📌 Visão do Produto

## 🎯 Missão

O sistema utiliza **Inteligência Artificial Local** exclusivamente para extrair informações de documentos oficiais, sendo toda a lógica de negócio responsável pelo cruzamento de dados implementada pelo próprio **EduData AI**.

Seu objetivo é **reduzir o tempo gasto com conferências manuais** e **aumentar a confiabilidade dos relatórios** entregues à gestão.

---

# 👤 Público-alvo

O sistema possui **um único usuário**.

> **Analista de Dados do Colégio Olimpo**

Não existe, neste momento, intenção de comercialização ou disponibilização pública da ferramenta.

> **Decisão arquitetural:** todas as escolhas de projeto devem considerar esse contexto.

---

# ❗ Problema

Após a divulgação dos resultados dos vestibulares, torna-se necessário identificar rapidamente quais aprovados pertencem ao **Colégio Olimpo**.

Atualmente esse processo depende da comparação entre:

- 📄 Base institucional de alunos
- 📄 Lista oficial de aprovados

Esse procedimento precisa ser realizado com **alta precisão**.

---

# 💡 Solução

O **EduData AI** automatiza todo esse processo.

## Fluxo resumido

┌──────────────────────────────┐
│      Lista Oficial (PDF)     │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Extração por IA Local    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│         Normalização         │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│ Cruzamento com Base Interna  │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│         Relatórios           │
└──────────────────────────────┘
```

---

# 🎯 Objetivo Principal

Identificar automaticamente quais candidatos aprovados pertencem ao **Colégio Olimpo**.

> Este é o principal objetivo do sistema.

Todas as funcionalidades deverão contribuir **direta ou indiretamente** para esse objetivo.

---

# 📦 Escopo Atual

Nesta versão, o sistema deverá ser capaz de:

- ✅ Receber PDFs contendo listas oficiais de aprovados;
- ✅ Extrair os dados utilizando IA Local;
- ✅ Estruturar essas informações;
- ✅ Cruzar os dados com a base institucional;
- ✅ Gerar relatórios finais.

---

# 🚫 Fora do Escopo

Nesta versão o sistema **NÃO** deverá:

- ❌ Buscar PDFs automaticamente;
- ❌ Monitorar sites;
- ❌ Fazer scraping;
- ❌ Interpretar editais;
- ❌ Processar cronogramas;
- ❌ Processar chamadas;
- ❌ Baixar documentos da internet.

> Todos os documentos serão fornecidos manualmente pelo usuário.

---

# 🤖 Papel da IA

A **Inteligência Artificial não toma decisões**.

Sua única responsabilidade é transformar documentos não estruturados em **dados estruturados**.

Toda decisão de negócio pertence ao **EduData AI**.

---

# 🏛️ Princípios

O projeto seguirá os seguintes princípios:

| Nº | Princípio |
|:--:|-----------|
| 1 | Simplicidade acima de complexidade |
| 2 | Arquitetura evolutiva |
| 3 | Não reescrever código funcional sem necessidade |
| 4 | Escalabilidade controlada |
| 5 | Qualidade acima de velocidade |
| 6 | IA como ferramenta, não como núcleo do sistema |
| 7 | Todo comportamento deverá ser reproduzível |

---

# 🚀 Visão de Longo Prazo

Embora inicialmente o sistema seja utilizado apenas pelo **Analista de Dados do Colégio Olimpo**, sua arquitetura deverá permitir a inclusão de novos vestibulares sem necessidade de reescrever o núcleo da aplicação.

Ao mesmo tempo, novas funcionalidades serão adicionadas **somente quando existir necessidade real**, preservando a simplicidade, a manutenção e a evolução do projeto.

---

---

<p align="center">
  <strong>EduData AI</strong><br>
  <em>Automação inteligente para identificação de aprovados.</em>
</p>
