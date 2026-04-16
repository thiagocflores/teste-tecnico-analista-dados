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

### Parte 1: Cruzamento e Tratamento de Dados

A planilha do banner (`planilha_banner_cliente.csv`) nao tem o campo `item_id`, que e necessario para cruzar com os dados de venda do GA4.

O cliente enviou o catalogo completo (`base_produtos.csv`) para voce identificar os IDs dos produtos divulgados.

**Perguntas:**
- Como voce faria o cruzamento entre a planilha do banner e o catalogo?
- Quais problemas voce encontrou nos dados? Como tratou?
- Algum produto do banner nao foi encontrado no catalogo? O que isso pode significar?

### Parte 2: Analise de Performance

Com os dados cruzados, analise a performance dos produtos do banner e das categorias do marketplace.

**Pontos para explorar (nao limitado a estes):**
- Quais categorias tem maior representacao de venda? E melhor taxa de conversao?
- Existe algum padrao temporal nas compras? (dia do mes, dia da semana)
- Como as marcas performam dentro de cada categoria?
- Os produtos divulgados no banner tiveram performance superior aos demais?
- O CRM esta contribuindo para as vendas? Existe potencial inexplorado?

### Parte 3: Reconciliacao de Dados

Os dados do GA4 e da VTEX cobrem o mesmo periodo, mas vem de fontes diferentes.

**Perguntas:**
- Os numeros batem entre GA4 e VTEX? Se nao, quais as possiveis causas?
- Que impacto essas divergencias tem na confiabilidade da analise?
- Como voce recomendaria tratar essas discrepancias no dia a dia?

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

## Criterios de Avaliacao

| Criterio | Peso |
|----------|------|
| Tratamento e qualidade dos dados | 25% |
| Profundidade da analise | 25% |
| Insights acionaveis e priorizados | 25% |
| Clareza na comunicacao dos resultados | 15% |
| Processo e documentacao | 10% |

---

## Como Entregar

1. Faca um **fork** deste repositorio
2. Adicione seus arquivos de analise na pasta `entrega/`
3. Abra um **Pull Request** para este repositorio com o titulo: `Entrega - [Seu Nome]`

Ou, se preferir, envie o link do seu trabalho por email.

---

**Boa sorte!** Estamos ansiosos para ver como voce pensa.
