<div align="center">
  <h1>🎓 EduData AI V3</h1>
  <p><strong>Automação inteligente para identificação de aprovados em vestibulares.</strong></p>
</div>
 <p>
   <div align="center">
    <img src="https://img.shields.io/badge/Versão-3.0-blue.svg" alt="Versão">
    <img src="https://img.shields.io/badge/Python-3.9%2B-blue" alt="Python">
    <img src="https://img.shields.io/badge/Status-Em_Desenvolvimento-brightgreen.svg" alt="Status">
    <img src="https://img.shields.io/badge/Licença-MIT-green.svg" alt="Licença">
     </div>
  </p>
<hr>

## 📖 Sobre o Projeto

O **EduData AI V3** é uma ferramenta interna desenvolvida para automatizar a identificação de alunos do **Colégio Olimpo** aprovados em processos seletivos e vestibulares brasileiros. 

Seu principal objetivo é reduzir drasticamente o tempo gasto com conferências manuais e aumentar a confiabilidade dos relatórios entregues à gestão da escola. A ferramenta soluciona o problema de cruzar, com alta precisão, listas oficiais de aprovados (frequentemente em PDF) com a base institucional de alunos matriculados.

*Este sistema foi projetado para uso exclusivo interno (Analista de Dados do Colégio Olimpo) e não possui previsão de comercialização ou disponibilização pública.*

## ⚙️ Como Funciona (Fluxo de Processamento)

A solução utiliza **Inteligência Artificial Local** como uma ferramenta de apoio — e não como o núcleo de tomada de decisão. A IA é encarregada apenas de transformar dados não estruturados em dados estruturados. Toda a lógica de cruzamento pertence ao sistema.

O fluxo segue as seguintes etapas:
1. **Upload:** O usuário fornece manualmente a Lista Oficial (PDF).
2. **Extração:** Uma IA Local lê e extrai as informações do PDF.
3. **Normalização:** Os dados extraídos são padronizados e limpos.
4. **Cruzamento:** O sistema compara a lista extraída com a Base Institucional de Alunos.
5. **Resultados:** Geração de relatórios precisos com os alunos do colégio aprovados.

*(Nota: Funções como web scraping de editais, monitoramento de sites ou busca automática de PDFs estão fora do escopo desta ferramenta, mantendo o sistema focado, simples e de alta qualidade).*

## 🛣️ Roadmap de Desenvolvimento

O projeto encontra-se em fase inicial, guiado pela filosofia de que "código funcional vale mais do que código bonito" e "simplicidade acima de complexidade". O desenvolvimento está dividido nas seguintes Sprints:

*   **Sprint 0:** Planejamento e definição da arquitetura *(Fase Atual)*
*   **Sprint 1:** Reconstrução do pipeline funcional
*   **Sprint 2:** Integração da Base Institucional
*   **Sprint 3:** Integração do Modelo de IA Local para extração de dados
*   **Sprint 4:** Suporte ao processamento do primeiro vestibular
*   **Sprint 5:** Geração de relatórios de saída
*   **Sprint 6:** Expansão da arquitetura para suportar novos vestibulares
*   **Sprint 7:** Melhorias, otimizações e refatorações contínuas

## 📁 Estrutura do Repositório

Atualmente, o projeto está estruturado da seguinte forma (em processo de construção):

```text
edudata-ai/
│
├── docs/             # Documentações de Visão, Filosofia e Roadmap
├── src/              # Código fonte principal (Em breve)
├── tests/            # Testes automatizados (Em breve)
├── examples/         # Exemplos e templates
├── scripts/          # Scripts utilitários
├── assets/           # Arquivos estáticos
│
├── README.md
├── LICENSE
└── .gitignore
```

---
<p align="center">
  Desenvolvido por <a href="https://github.com/ErickCorreia">ErickCorreia</a>
</p>
