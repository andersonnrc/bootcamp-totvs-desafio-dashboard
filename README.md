# 🎮 Xbox Game Pass - Sales Dashboard

![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

## 📌 Visão Geral
Este projeto consiste em um Dashboard interativo desenvolvido inteiramente no **Microsoft Excel** para analisar as vendas de assinaturas do Xbox Game Pass. O objetivo é extrair insights valiosos sobre o faturamento de diferentes planos, taxas de renovação automática e o desempenho de serviços adicionais como EA Play e Minecraft Season Pass.

---

## 📸 Preview do Dashboard
![](/images/dashboard.png "Dashboard Preview")

---

## 📊 Perguntas de Negócio Respondidas
O dashboard foi modelado para responder de forma rápida e visual às seguintes questões estratégicas:
1. Qual é o faturamento total de vendas de planos anuais (agregando todas as assinaturas)?
2. Qual é o faturamento total de planos anuais segmentado por status de renovação automática (Auto Renewal)?
3. Qual é o total de vendas gerado especificamente pelas assinaturas do *EA Play*?
4. Qual é o total de vendas gerado especificamente pelo *Minecraft Season Pass*?

---

## 📁 Estrutura do Projeto
A solução foi dividida nas seguintes abas dentro da pasta de trabalho:
* **`Assets`**: Recursos visuais, logotipos (Xbox, EA Play, Minecraft) e paleta de cores em Hexadecimal (ex: Verde `#5BF6A8`).
* **`Bases`**: Base de dados bruta contendo os registros de assinaturas.
* **`Cálculos`**: Motor analítico do projeto, onde residem as Tabelas Dinâmicas e as lógicas de extração.
* **`Dashboard`**: Interface final para o usuário, contendo os gráficos e segmentadores de dados formatados.

---

## 🚀 Como foi construído (Passos Técnicos)

### 1. Modelagem e Tabelas Dinâmicas
* Seleção da base de dados completa (a partir da coluna `Subscriber ID`).
* Criação de Tabelas Dinâmicas na aba **Cálculos**:
  * **Faturamento Anual Total:** Agrupamento por `Name` (Linhas) e soma de `Total Value` (Valores), com formatação monetária. Filtro aplicado na coluna `Subscription Type` para exibir apenas planos "Annual".
  * **Análise de Renovação:** Inclusão do campo `Auto Renewal` no filtro para segmentar o faturamento por renovação automática.
  * **Análise de Serviços Específicos:** Duplicação da tabela base para isolar os planos *EA Play* e *Minecraft Season Pass* usando os filtros adequados e extraindo o `Total Geral` via fórmula nas células (ex: `=E25`, `=E36`) para exibição dinâmica no dashboard.

### 2. Visualização de Dados (Gráficos)
* Geração de Gráficos Dinâmicos de Barras a partir das tabelas criadas.
* **Limpeza Visual:** Remoção de legendas, contornos e preenchimentos de fundo dos gráficos.
* **Identidade Visual:** Aplicação da cor personalizada `#5BF6A8` nas barras de dados.
* **Interatividade:** Inserção de Segmentação de Dados (Filtros interativos) focados no campo `Subscription Type`, com estilo customizado.

### 3. Montagem do Dashboard (Interface)
* **Estruturação da Tela:** Configuração da Coluna A como um menu lateral verde (cor `#2AE6B1`), abrigando o logo do Xbox (formatado e cortado).
* **Área de Gráficos:** Definição da área principal com fundo `#E8E6E9` e adição do título "XBOX GAME PASS SUBSCRIPTIONS SALES".
* **Posicionamento:** Migração dos gráficos e filtros da aba Cálculos para o Dashboard, utilizando a configuração *"Não mover ou dimensionar com células"* para garantir a estabilidade do layout.
* **Cards de Indicadores (KPIs):** Criação de retângulos com bordas arredondadas, agrupados com as imagens dos serviços (EA Play/Minecraft) e vinculados dinamicamente às células de totalização da aba Cálculos.
* **Finalização:** Ocultamento de abas auxiliares, títulos, linhas de grade e configuração para o modo de exibição em tela inteira, garantindo uma experiência imersiva de aplicativo.

---

## 🔮 Próximos Passos
Como projetos de dados estão sempre em evolução, algumas melhorias futuras podem incluir:
* Migrar a modelagem destes dados para o **Power BI**, permitindo atualizações automatizadas e cruzamento com outras bases.
* Utilizar **Python** para fazer um tratamento prévio (ETL) mais robusto caso a base de assinaturas escale em volume.

---

## 🧑‍💼 Contato

[Linkedin](https://www.linkedin.com/in/anderson-ribeiro-carvalho)
