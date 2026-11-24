# Ficha da base — Macroeconomia dos Estados Unidos, 1959–2009

**Arquivo:** `macrodata.csv`  
**Tipo:** dados reais, séries temporais trimestrais

## Conteúdo

Indicadores macroeconômicos trimestrais dos Estados Unidos, de 1959T1 a 2009T3: 203 trimestres consecutivos, uma linha por trimestre.

| Variável | Descrição, segundo a documentação do statsmodels |
|---|---|
| `year`, `quarter` | ano e trimestre (1 a 4) |
| `cpi` | índice de preços ao consumidor de todos os consumidores urbanos, todos os itens, no fim do trimestre (1982–84 = 100), com ajuste sazonal |
| `infl` | inflação anualizada, em %: `400 · ln(cpi_t / cpi_{t-1})` |
| `unemp` | taxa de desemprego, em %, com ajuste sazonal |
| `realgdp`, `realcons`, `realinv`, `realgovt`, `realdpi` | PIB, consumo das famílias, investimento privado, gastos federais e renda disponível, em bilhões de dólares encadeados de 2005, com ajuste sazonal e em taxa anual |
| `m1` | estoque nominal de moeda M1 no fim do trimestre, com ajuste sazonal |
| `tbilrate` | taxa média trimestral dos títulos do Tesouro de 3 meses no mercado secundário |
| `pop` | população total no fim do trimestre |
| `realint` | taxa de juros real: `tbilrate − infl` |

A Aula 15 usa `cpi`, `infl` e `unemp`.

## Fonte

- Compilada por Skipper Seabold e incluída no statsmodels como `statsmodels.datasets.macrodata`.
- Dados do FRED (Federal Reserve Economic Data), Federal Reserve Bank of St. Louis, acessados em 15/12/2009, exceto a taxa de desemprego, obtida do Bureau of Labor Statistics, U.S. Department of Labor, na mesma data.

## Condição de uso

Domínio público, segundo a documentação do statsmodels (`COPYRIGHT = "This is public domain."`).

## Proveniência e integridade

- Snapshot: cópia byte a byte de `statsmodels/datasets/macrodata/macrodata.csv`, statsmodels 0.14.5, em 05/11/2026.
- Tamanho: 18.033 bytes.
- SHA-256: `7853fcc0d92a9b89b627cb6eb2d27faf4a00c7515e3b37a9a24001ef597ca8f0`.
- Os notebooks leem este CSV, não o pacote, para que a base não dependa da versão instalada do statsmodels.

## Limites

- **Primeiro trimestre da inflação:** em 1959T1, `infl` e `realint` aparecem como 0. Sem o índice de preços do trimestre anterior, a inflação desse trimestre não pode ser calculada; o zero é um valor ausente registrado como número e deve ser descartado. De 1959T2 em diante, `infl` coincide com `400 · ln(cpi_t / cpi_{t-1})` até o arredondamento a duas casas.
- **Safra dos dados:** os valores são os disponíveis em dezembro de 2009. Séries macroeconômicas são revisadas, e os valores publicados hoje para os mesmos trimestres podem ser diferentes.
- **Desemprego trimestral:** a documentação não informa se a taxa trimestral é a média dos três meses ou o valor de um mês do trimestre.
- **Uma economia e um período:** Estados Unidos, 1959–2009, com mudanças de regime de política econômica ao longo do período — em especial, a inflação alta dos anos 1970 e a política monetária mais restritiva a partir do início dos anos 1980.
