# 📊 analise de dados industriais 🎲🏭

## 🛠️ Desafio Dados: Análise de Produção e Eficiência - Alpha SP

Este projeto consiste em uma análise detalhada dos dados de produção diária, cadastro de maquinários e metas mensais da fábrica **Alpha SP**. O objetivo principal é consolidar diferentes fontes de dados para extrair insights estratégicos sobre o desempenho operacional das máquinas, cumprimento de metas de produção, controle de qualidade e custos de operação ao longo de um período de 6 meses (Janeiro a Junho de 2025).

---

### 🛠️ Tecnologias e Ferramentas Utilizadas

No desenvolvimento deste projeto, foram utilizadas as seguintes ferramentas e bibliotecas:

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)

---

### 📋 Estrutura dos Dados

A análise foi construída unificando três bases de dados principais:
1. **Produção Diária (`alpha_sp_producao_diaria.csv`):** Histórico diário contendo horas de uso, temperatura, vibração, total produzido, peças defeituosas e eficiência de cada máquina.
2. **Cadastro das Máquinas (`dados_complementares_alpha_sp.xlsx` - Aba 1):** Informações de fabricante, modelo, ano de aquisição, capacidade máxima e custo por hora de operação.
3. **Metas Mensais (`dados_complementares_alpha_sp.xlsx` - Aba 2):** Planejamento mensal de metas de produção diária e limites máximos toleráveis para a taxa de defeitos por setor.

---

### 🔍 Principais Insights Obtidos

#### 1. Custos de Operação
* O custo total de operação de todas as máquinas somou **R$ 163.350,10**.
* A máquina **Solda Robô 01** foi a mais cara de se operar no período, totalizando **R$ 69.665,40** devido ao seu custo por hora de operação mais elevado.
<img width="713" height="471" alt="maquina_custo_operacao" src="https://github.com/user-attachments/assets/61e95319-6d53-4955-bc04-ebfa699657a4" />

#### 2. Relação Idade x Qualidade
* Foi identificada uma correlação de **-0.99** entre o ano de aquisição e a taxa de defeito média das máquinas.
* **Conclusão:** Máquinas mais antigas (ex: Prensa 12 de 2015) apresentam uma taxa média de peças defeituosas significativamente maior que as mais novas (ex: Solda Robô 01 de 2021).

#### 3. Cumprimento de Metas de Produção
* Houve um total de **388 dias** em que a produção ficou abaixo das metas diárias estabelecidas por setor, evidenciando oportunidades de melhoria de gargalos principalmente no setor de **Estamparia** durante o mês de Maio.

#### 4. Metas de Qualidade (Peças Defeituosas)
* Em **169 dias** a taxa de peças defeituosas ultrapassou o limite máximo estabelecido pelas metas de qualidade.
* O setor de **Estamparia** foi o que descumpriu a meta com maior frequência (79 vezes).

#### 5. Capacidade Operacional vs. Realidade
* **Solda Robô 01** opera mais próxima de sua capacidade total limite, utilizando **73.63%** de sua capacidade máxima de projeto.
* **Prensa 12** possui a maior folga média diária de produção, operando com **66.31%** de sua capacidade cadastrada.

---

### 📈 Visualizações do Projeto

O projeto conta com gráficos de análises visuais gerados com `matplotlib` para facilitar a tomada de decisão das equipes de manutenção e produção, abordando de forma clara as relações de:
- Quantidade de Peças Defeituosas por Máquina.
- Produção Total Acumulada por Turno.
- Custos Totais de Operação de cada Equipamento.
