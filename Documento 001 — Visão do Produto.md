# EduData AI

> **Documento de Visão do Produto**
>
> Ferramenta interna para automatizar a identificação de alunos do **Colégio Olimpo** aprovados em processos seletivos brasileiros.

---

## Visão do Produto

### Missão

O **EduData AI** utiliza **Inteligência Artificial Local** exclusivamente para extrair informações de documentos oficiais, sendo toda a lógica de negócio responsável pelo cruzamento de dados implementada pelo próprio sistema.

Seu objetivo é:

- reduzir o tempo gasto com conferências manuais;
- aumentar a confiabilidade dos relatórios entregues à gestão.

---

## Público-alvo

| Informação | Descrição |
|------------|-----------|
| Usuário | Analista de Dados do Colégio Olimpo |
| Comercialização | Não prevista |
| Disponibilização pública | Não prevista |

> **Diretriz de arquitetura**
>
> Todas as decisões arquiteturais deverão considerar que o sistema possui apenas um usuário.

---

## Problema

Após a divulgação dos resultados dos vestibulares, torna-se necessário identificar rapidamente quais aprovados pertencem ao **Colégio Olimpo**.

Atualmente esse processo depende da comparação entre:

- Base institucional de alunos;
- Lista oficial de aprovados.

Esse procedimento precisa ser realizado com **alta precisão**.

---

## Solução

O **EduData AI** automatiza esse processo.

### Fluxo de processamento

```text
Lista Oficial (PDF)
        │
        ▼
Extração por IA Local
        │
        ▼
Normalização
        │
        ▼
Cruzamento com Base Institucional
        │
        ▼
Relatórios
```

---

## Objetivo Principal

Identificar automaticamente quais candidatos aprovados pertencem ao **Colégio Olimpo**.

> Todas as funcionalidades do sistema deverão contribuir direta ou indiretamente para esse objetivo.

---

## Escopo Atual

Nesta versão o sistema deverá:

- Receber PDFs contendo listas oficiais de aprovados;
- Extrair os dados utilizando IA Local;
- Estruturar essas informações;
- Cruzar os dados com a base institucional;
- Gerar relatórios finais.

---

## Fora do Escopo

Nesta versão o sistema **não deverá**:

- Buscar PDFs automaticamente;
- Monitorar sites;
- Fazer scraping;
- Interpretar editais;
- Processar cronogramas;
- Processar chamadas;
- Baixar documentos da internet.

> **Observação**
>
> Todos os documentos serão fornecidos manualmente pelo usuário.

---

## Papel da Inteligência Artificial

A Inteligência Artificial **não toma decisões**.

Sua única responsabilidade é transformar documentos não estruturados em dados estruturados.

Toda decisão de negócio pertence ao **EduData AI**.

---

## Princípios

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

## Visão de Longo Prazo

Embora inicialmente o sistema seja utilizado apenas pelo **Analista de Dados do Colégio Olimpo**, sua arquitetura deverá permitir a inclusão de novos vestibulares sem necessidade de reescrever o núcleo da aplicação.

Entretanto, funcionalidades serão adicionadas apenas quando existir necessidade real.

---

<p align="center">
  <strong>EduData AI</strong><br>
  <sub>Automação inteligente para identificação de aprovados</sub>
</p>
