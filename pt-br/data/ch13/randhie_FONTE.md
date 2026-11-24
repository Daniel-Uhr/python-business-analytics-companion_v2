# Ficha da base — RAND Health Insurance Experiment

**Arquivo:** `randhie.csv`  
**Tipo:** dados reais de um experimento com sorteio

## Conteúdo

Consultas médicas ambulatoriais por pessoa e por ano no Health Insurance Experiment da RAND Corporation, realizado nos Estados Unidos entre as décadas de 1970 e 1980. As famílias participantes foram sorteadas entre planos de seguro-saúde com diferentes coparticipações — a parcela da despesa paga pelo segurado.

| Item | Registro |
|---|---|
| Unidade de observação | pessoa-ano |
| Número de observações | 20.190 |
| `mdvis` | número de consultas ambulatoriais com médico no ano |
| `lncoins` | `ln(coparticipação + 1)`, com a coparticipação em % (0 a 100) |
| `idp` | 1 se o plano tem franquia individual, 0 caso contrário |
| `lpi` | `ln(max(1, pagamento anual de incentivo à participação))` |
| `fmde` | 0 se `idp = 1`; caso contrário, `ln(max(1, MDE / (0,01 · coparticipação)))`, em que MDE é o teto de despesa do segurado |
| `physlm` | 1 se a pessoa tem limitação física |
| `disea` | número de doenças crônicas |
| `hlthg`, `hlthf`, `hlthp` | 1 se a saúde autoavaliada é boa, regular ou ruim (a categoria omitida é excelente) |

A coparticipação de cada plano é obtida por `round(exp(lncoins) − 1)`: 0%, 25%, 50% e 95% nos planos sem franquia individual (`idp = 0`, 14.941 pessoas-ano); 0% e 100% nos planos com franquia individual (`idp = 1`).

## Fonte

- RAND Corporation, Health Insurance Experiment (HIE).
- Resultados principais: Manning, W. G.; Newhouse, J. P.; Duan, N.; Keeler, E. B.; Leibowitz, A.; Marquis, M. S. (1987). Health Insurance and the Demand for Medical Care: Evidence from a Randomized Experiment. *American Economic Review*, 77(3), 251–277.
- Subconjunto usado em Cameron, A. C.; Trivedi, P. K. (2005). *Microeconometrics: Methods and Applications*. Cambridge University Press; incluído no statsmodels como `statsmodels.datasets.randhie`. Segundo a documentação do statsmodels, os dados diferem ligeiramente dos reportados por Cameron e Trivedi.

## Condição de uso

Domínio público, segundo a documentação do statsmodels (`COPYRIGHT = "This is in the public domain."`).

## Proveniência e integridade

- Snapshot: cópia byte a byte de `statsmodels/datasets/randhie/randhie.csv`, statsmodels 0.14.5, em 04/11/2026.
- SHA-256: `7ee0d2dea0ca8ecfcfbb02c31d63a88abe632318f5a110d638d6a035f4827f91`.
- Os notebooks leem este CSV, não o pacote, para que a base não dependa da versão instalada do statsmodels.

## Limites

- A base não traz identificadores de pessoa nem de família, e as mesmas pessoas aparecem em vários anos. Como observações da mesma pessoa e da mesma família não são independentes, os erros-padrão — mesmo os robustos — tendem a subestimar a incerteza; erros-padrão agrupados não podem ser calculados.
- O sorteio foi feito entre famílias, e não entre pessoas-ano, e houve abandono do experimento ao longo do tempo; a leitura causal das diferenças entre planos é a do estudo original, com essas ressalvas.
- Estados Unidos, décadas de 1970 e 1980: preços, oferta de serviços e práticas médicas diferem dos atuais e dos de outros países.
- `mdvis` conta apenas consultas ambulatoriais com médico; não inclui internações, exames ou despesas.
