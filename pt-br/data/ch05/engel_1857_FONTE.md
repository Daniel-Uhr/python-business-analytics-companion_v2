# Ficha da base — Engel (1857)

**Arquivo:** `engel_1857.csv`  
**Tipo:** dados reais históricos

## Conteúdo

Renda anual e gasto anual com alimentação de 235 famílias de trabalhadores na Bélgica, em 1857.

| Item | Registro |
|---|---|
| Unidade de observação | família |
| Número de observações | 235 |
| `income` | renda anual da família, em francos belgas |
| `foodexp` | gasto anual da família com alimentação, em francos belgas |

## Fonte

- Base usada em Koenker, R.; Bassett, G. (1982). Robust Tests for Heteroscedasticity Based on Regression Quantiles. *Econometrica*, 50(1), 43–61.
- Distribuída com o pacote `quantreg` do R (Koenker, R. *quantreg: Quantile Regression*) e incluída no statsmodels como `statsmodels.datasets.engel`.

## Condição de uso

Domínio público, segundo a documentação do statsmodels (`COPYRIGHT = "This is public domain."`).

## Proveniência e integridade

- Snapshot: cópia byte a byte de `statsmodels/datasets/engel/engel.csv`, statsmodels 0.14.5, em 31/10/2026.
- SHA-256 (arquivo com finais de linha CRLF, como distribuído): `05b60e091325bc170cb6803ce78f80c029bfe2ae072891ec577f1ebe8deefd61`.
- Os notebooks leem este CSV, não o pacote, para que a base não dependa da versão instalada do statsmodels.

## Limites

- Famílias de trabalhadores belgas de 1857: a base não representa o consumo atual nem outras populações.
- Não há informação sobre tamanho da família, preços ou região; a leitura é descritiva.
- Os valores são armazenados com muitas casas decimais; a aula os arredonda apenas na apresentação.
