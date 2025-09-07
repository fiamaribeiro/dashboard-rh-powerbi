# 📊 Dashboard de RH — Power BI

## 🎯 Objetivo
Desenvolver um painel interativo no **Power BI** para monitorar indicadores de **Recursos Humanos**, incluindo:
- Contratações
- Desligamentos
- Turnover
- Distribuição de funcionários por área, cargo e cidade
- Controle de horas extras

O objetivo é fornecer **insights rápidos e acionáveis** para apoiar decisões estratégicas da área de RH.

---

## 🗂️ Dataset
- **Fonte:** dataset simulado (dados fictícios para fins de estudo).
- **Tamanho:** ~217 registros.
- **Campos principais:** Cidade, Cargo, Área, Contratações, Demissões, Status, Gênero, Horas Extras.

---

## ⚙️ Modelagem de Dados
- **Tabela de Fatos:** Funcionários
- **Tabelas de Dimensão:** Área, Cargo, Localidade
- **Relacionamentos:**  
  - Área → Funcionários (1:N)  
  - Cargo → Funcionários (1:N)  
  - Localidade → Funcionários (1:N)  

---

## 📐 Métricas em DAX
Exemplos de medidas criadas no dashboard:

- **Turnover (%)**
```DAX
Turnover = DIVIDE([Demissões], [Funcionários Ativos])
