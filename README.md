# Teste Tecnico - Analista de Dados

## Contexto

Voce e analista de dados em uma consultoria de analytics e martech. Seu cliente e um **marketplace de eletrodomesticos e produtos para casa** que precisa de ajuda em duas frentes:

1. Entender a **performance dos produtos divulgados no banner** da home do site
2. Analisar o **comportamento de compra por categoria** para otimizar a jornada do usuario

O cliente tem uma operacao em **VTEX** e usa **Google Analytics 4** para tracking do site. Tambem possui campanhas de **CRM (email marketing)** ativas.

Infelizmente, a camada de dados do site e limitada: o GA4 **nao captura interacoes diretas com o banner** (cliques, impressoes). Para viabilizar a analise, o cliente enviou uma planilha com os produtos que foram divulgados no banner durante Janeiro e Fevereiro de 2025.

---

## Dados Disponíveis

Na pasta `dados/`, voce encontra **5 arquivos CSV**:

| Arquivo | Descricao | Volume |
|---------|-----------|--------|
| `base_produtos.csv` | Catalogo completo de produtos (VTEX) | ~5.000 produtos |
| `planilha_banner_cliente.csv` | Produtos divulgados no banner da home | ~30 produtos |
| `export_ga4_transacoes.csv` | Transacoes exportadas do GA4 (Jan-Fev/2025) | ~15.000 registros |
| `pedidos_vtex.csv` | Pedidos registrados na VTEX (Jan-Fev/2025) | ~16.000 registros |
| `crm_campanhas.csv` | Dados de campanhas de email marketing | ~150 registros |

**Observacoes importantes:**
- A planilha do banner foi preenchida manualmente pelo cliente e **nao contem o ID do produto**
- O catalogo completo do cliente tem os IDs, mas sao **mais de 5.000 produtos**
- Os dados vem de fontes diferentes e podem apresentar **inconsistencias entre si**

---

## Desafio

O cliente quer respostas para duas perguntas:

1. **"O investimento no banner da home esta valendo a pena?"**
2. **"O que esta acontecendo com as nossas vendas por categoria e o que podemos fazer para melhorar?"**

Voce tem 5 CSVs de fontes diferentes. Analise.

---

## Entregaveis

1. **Documento de analise** (formato livre: PDF, Google Slides, Notion, Jupyter Notebook, etc.)
   - Metodologia utilizada para o cruzamento de dados
   - Principais findings e insights
   - Recomendacoes praticas para o cliente (priorizadas)

2. **Evidencia do processo** (queries SQL, scripts Python/R, planilhas, etc.)
   - Queremos ver **como** voce chegou nos resultados, nao so os resultados

3. **Estimativa de prazo**
   - Antes de comecar, nos diga quanto tempo voce estima para entregar
   - Nao existe prazo certo ou errado. Queremos avaliar sua capacidade de estimar

---

## Regras

- **Use as ferramentas que preferir**: Excel, Google Sheets, SQL, Python, R, BI tools, etc.
- **IA e bem-vinda**: se usar ChatGPT, Claude, Copilot ou qualquer outra IA, mencione como usou e o que ajustou no output. Transparencia > tudo.
- **Nao existe resposta unica certa**: estamos avaliando o processo, o raciocinio e a capacidade de gerar insight acionavel.
- **Qualidade > Quantidade**: prefira 3 insights profundos a 10 superficiais.
- **Priorize**: se o cliente so pudesse implementar 2 recomendacoes, quais seriam e por que?

---

## Como Entregar

1. Faca um **fork** deste repositorio
2. Adicione seus arquivos de analise na pasta `entrega/`
3. Abra um **Pull Request** para este repositorio com o titulo: `Entrega - [Seu Nome]`

Ou, se preferir, envie o link do seu trabalho por email.

---

**Boa sorte!** Estamos ansiosos para ver como voce pensa.
