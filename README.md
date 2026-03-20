# Bright Brains — Desafio Prático de Estágio

Sistema de análise de pacientes desenvolvido como parte do processo seletivo da Bright Brains. O projeto combina um **dashboard no Power BI** com um **dashboard interativo em HTML** que utiliza inteligência artificial (Claude, Anthropic) para gerar insights clínicos automatizados (MAS ESTÁ GERANDO ATUALMENTE UM RELATÓRIO JÁ GERAD0, PARA PROTEÇÃO DA CHAVE DE API, MAS EM PRODUÇÃO PODERIA SER APLICADO UMA CHAVE).

---

## Estrutura do Projeto

```
desafio-bright-brains/
├── README.md                          ← Apresentação do projeto
├── dashboard/
│   └── bright_brains_dashboard.html   ← Dashboard HTML com IA
├── dados/
│   └── bright_brains_dados.xlsx       ← Planilha com dados e fórmulas
├── powerbi/
│   ├── desafio-estagio.Report/        
│   ├── desafio-estagio.SemanticModel/ 
│   ├── desafio-estagio                
│   └── .gitignore                     

```

---

## Visão Geral

O desafio consiste em organizar dados de 8 pacientes com condições como Ansiedade, Depressão, TDAH e Insônia, e responder a 4 perguntas analíticas sobre os resultados dos tratamentos.

### Ferramentas utilizadas

- **Power BI** — Dashboard principal com KPIs, gráficos e medidas DAX
- **HTML/CSS/JS + Chart.js** — Dashboard interativo complementar
- **Claude (Anthropic)** — Geração de insights clínicos via inteligência artificial
- **Excel** — Organização dos dados com fórmulas (AVERAGEIF, COUNTIF, CORREL, INDEX/MATCH)

---

## Respostas do Desafio

### a) Qual condição teve maior melhora média?

**Depressão** — melhora média de **70%**, seguida por TDAH (67.5%), Ansiedade (45%) e Insônia (32.5%).

### b) Qual paciente teve o melhor resultado?

**Pedro** — **80% de melhora** após 30 sessões de tratamento para Depressão.

### c) Existe relação entre número de sessões e melhora?

**Sim, correlação positiva muito forte (r ≈ 0.99).** Quanto mais sessões, maior a melhora. O gráfico de dispersão mostra uma tendência quase perfeitamente linear.

### d) Qual grupo parece precisar de mais sessões?

**Insônia** — menor melhora (32.5%) com apenas 11 sessões em média. Dado que a correlação entre sessões e melhora é de 0.99, este é o grupo que mais se beneficiaria de sessões adicionais.

---

## Dashboard HTML com IA

O dashboard interativo pode ser acessado diretamente pelo navegador abrindo o arquivo `dashboard/bright_brains_dashboard.html`.

### Funcionalidades

- 4 KPIs principais (pacientes, melhora média, melhor condição, melhor paciente)
- Tabela de dados com barras de progresso
- Gráfico de barras — melhora média por condição
- Gráfico de dispersão — correlação sessões × melhora com linha de tendência
- Gráfico horizontal — média de sessões por condição
- Seção de respostas do desafio
- **Insights gerados por IA (Claude, Anthropic)** com efeito de digitação em tempo real

### Sobre a integração com IA

Os insights clínicos foram gerados utilizando o modelo Claude da Anthropic. A análise cobre:

1. **Insights principais** — padrões identificados nos dados
2. **Recomendações clínicas** — ações práticas para a equipe
3. **Análise de idade** — relação entre idade e resultado do tratamento

Em um ambiente de produção, a integração seria feita via API em tempo real. Para esta demonstração, os insights foram pré-processados e são exibidos com simulação de geração.

Pode ser acessado pelo link: https://ckenz0.github.io/desafio-bright-brains/dashboard/bright_brains_dashboard.html

---

## Dashboard Power BI

O dashboard no Power BI contém:

- **Cartões KPI** — Total de pacientes, melhora média, melhor condição e melhor paciente
- **Gráfico de barras** — Melhora média por condição
- **Gráfico de dispersão** — Correlação entre sessões e melhora com linha de tendência
- **Tabela completa** — Dados dos pacientes com formatação condicional
- **Medida de correlação** — Cálculo de Pearson em DAX (r ≈ 0.99)


## Dados

| Paciente | Idade | Condição | Sessões | Melhora (%) |
|----------|-------|----------|---------|-------------|
| João | 45 | Depressão | 20 | 60 |
| Maria | 30 | Ansiedade | 15 | 40 |
| Carlos | 50 | Insônia | 10 | 30 |
| Ana | 28 | TDAH | 25 | 70 |
| Pedro | 60 | Depressão | 30 | 80 |
| Julia | 35 | Ansiedade | 18 | 50 |
| Lucas | 40 | TDAH | 22 | 65 |
| Fernanda | 55 | Insônia | 12 | 35 |

---

## Como executar

1. **Dashboard HTML** — Abra `dashboard/bright_brains_dashboard.html` em qualquer navegador
2. **Power BI** — Abra o arquivo `powerbi/desafio-estagio` no Power BI Desktop
3. **Dados** — O arquivo `dados/bright_brains_dados.xlsx` pode ser aberto no Excel para consulta

---

## Autor - caue

Desenvolvido para o Desafio Prático de Estágio — Bright Brains
