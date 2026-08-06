# Pipeline de Extração

## Objetivo

Este documento descreve o funcionamento da etapa de extração do EduData AI.

O objetivo é documentar o comportamento esperado do sistema, independentemente da implementação utilizada.

Este documento servirá como referência para qualquer alteração futura na etapa de extração.

---

# Responsabilidade

A etapa de Extração possui uma única responsabilidade:

> Transformar um documento oficial não estruturado em dados estruturados.

Nenhuma decisão de negócio deverá ocorrer nesta etapa.

A Extração não realiza:

- cruzamento;
- validação de negócio;
- geração de relatórios;
- identificação de alunos do Colégio Olimpo.

---

# Entrada

A Extração recebe:

- Lista Oficial em formato PDF.

O documento é fornecido manualmente pelo Analista de Dados.

---

# Processamento

O fluxo esperado é:

PDF

↓

Leitura do Documento

↓

Envio para IA Local

↓

Resposta da IA

↓

Conversão para Modelo Interno

↓

Validação Estrutural

↓

Saída Estruturada

---

# Papel da IA Local

A IA Local possui apenas uma responsabilidade.

Converter um documento PDF em dados estruturados.

A IA não possui conhecimento sobre:

- Base Institucional;
- Alunos do Colégio Olimpo;
- Cruzamento;
- Relatórios;
- Regras de negócio.

---

# Modelo de Saída

Ao final da extração o sistema deverá produzir uma coleção de objetos do tipo:

Aprovado

Cada registro deverá conter, sempre que possível:

- nome;
- curso;
- campus (quando existir);
- modalidade (quando existir);
- classificação (quando existir);
- turno (quando existir).

Campos ausentes deverão permanecer vazios.

Nunca deverão ser inventados pela IA.

---

# Conversão

A resposta da IA nunca será utilizada diretamente.

Ela deverá ser convertida para o Modelo Interno de Dados do EduData AI.

Essa conversão é responsabilidade do próprio sistema.

---

# Validação Estrutural

Antes da próxima etapa deverão ser realizadas verificações como:

- resposta vazia;
- estrutura inválida;
- campos obrigatórios;
- registros duplicados;
- caracteres inválidos.

Falhas deverão ser registradas para auditoria.

---

# Saída

A saída da Extração consiste em uma Lista Oficial estruturada contendo candidatos aprovados.

Essa saída será utilizada pela etapa de Normalização.

---

# Restrições

A Extração não poderá:

- acessar a Base Institucional;
- realizar cruzamentos;
- gerar relatórios;
- modificar regras de negócio.

---

# Critérios de Aceite

A etapa será considerada correta quando:

- o PDF for interpretado corretamente;
- os dados forem convertidos para o Modelo Interno;
- nenhuma regra de negócio for aplicada;
- todos os registros produzidos puderem ser utilizados pela etapa seguinte.

---

# Observações

O comportamento da Extração deverá permanecer estável independentemente do modelo de IA utilizado.

Trocas de modelo, prompts ou bibliotecas não deverão impactar as etapas posteriores do pipeline.
