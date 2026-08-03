
````markdown
# Responsabilidades da V3

## Objetivo

Este documento descreve a arquitetura conceitual do EduData AI V3.

A arquitetura foi construída a partir do domínio do problema e não da tecnologia utilizada.

Seu objetivo é garantir evolução controlada, simplicidade e facilidade de manutenção.

---

# Filosofia

O EduData AI não é um sistema de Inteligência Artificial.

O EduData AI é um sistema de cruzamento de dados que utiliza IA Local exclusivamente para extração de informações.

Toda regra de negócio pertence ao EduData AI.

---

# Arquitetura em Camadas

A arquitetura da V3 será composta por cinco grandes componentes.

```

```
                    Usuário
                       │
                       ▼
              Orquestração do Processo
                       │
      ┌────────────────┼────────────────┐
      ▼                ▼                ▼
 Extração        Base Institucional   Configuração
      │
      ▼
 Validação
      │
      ▼
 Normalização
      │
      ▼
 Cruzamento
      │
      ▼
 Relatórios
      │
      ▼
 Exportação
```

````

---

# 1. Orquestração

Responsável apenas por coordenar o fluxo.

Ela nunca toma decisões de negócio.

Responsabilidades:

* iniciar processamento;
* controlar ordem das etapas;
* registrar execução;
* tratar falhas.

---

# 2. Extração

Responsável por conversar com a IA Local.

Entradas:

* PDF

Saídas:

* Dados estruturados

A extração nunca compara alunos.

Nunca gera relatórios.

Nunca toma decisões.

Sua única responsabilidade é interpretar documentos.

---

# 3. Base Institucional

Representa o conjunto oficial de alunos do Colégio Olimpo.

Responsabilidades:

* disponibilizar alunos;
* disponibilizar turmas;
* servir como fonte oficial.

A Base Institucional nunca conhece vestibulares.

---

# 4. Validação

Responsável por verificar se os dados recebidos possuem qualidade suficiente para continuar o processamento.

Ela nunca altera informações.

Ela apenas aprova ou reprova.

---

# 5. Normalização

Responsável por padronizar dados.

Exemplos:

* espaços;
* acentos;
* capitalização;
* caracteres especiais.

---

# 6. Cruzamento ⭐

Este é o núcleo do EduData AI.

É onde está praticamente toda a regra de negócio.

Entradas:

* Base Institucional
* Lista Oficial

Saídas:

* alunos identificados;
* não identificados;
* possíveis conflitos.

Nenhuma outra parte do sistema poderá modificar o resultado do cruzamento.

---

# 7. Relatórios

Responsável por transformar o resultado do cruzamento em documentos úteis.

Ela não conhece PDF.

Ela não conhece IA.

Ela apenas recebe dados prontos.

---

# 8. Exportação

Última etapa.

Converte os resultados para os formatos definidos pelo projeto.

---

# Fluxo Completo

Usuário

↓

Lista Oficial

↓

Extração

↓

Validação

↓

Normalização

↓

Cruzamento

↓

Relatórios

↓

Exportação

---

# Dependências Permitidas

Orquestração

↓

Extração

↓

Validação

↓

Normalização

↓

Cruzamento

↓

Relatórios

↓

Exportação

Nunca o contrário.

---

# Dependências Proibidas

Relatórios não podem acessar PDF.

Extração não pode acessar Base Institucional.

IA Local não pode conhecer regras de negócio.

Base Institucional não pode conhecer vestibulares.

---

# Regra de Ouro

Cada componente possui apenas uma responsabilidade.

Sempre que um componente precisar executar duas responsabilidades diferentes, sua divisão deverá ser avaliada.


