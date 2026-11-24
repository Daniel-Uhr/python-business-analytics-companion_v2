# Dicionário de dados — Supermercados Cisne



## Contexto



A Cisne é uma rede fictícia de supermercados com cinco lojas em uma mesma cidade. Seu programa de fidelidade, o **Cisne+**, registra as compras dos clientes cadastrados. As bases são **sintéticas** e foram preparadas para fins educacionais; nomes, valores e relações não descrevem nenhuma empresa real.



## `clientes_cisne.csv`



Uma linha representa um cliente do Cisne+. A base é uma amostra aleatória de 3.000 clientes cadastrados antes de 2025, observados de janeiro a dezembro de 2025.



| Coluna | Significado | Unidade ou codificação |

|---|---|---|

| `cliente_id` | identificador do cliente | texto, `M0001` a `M3000` |

| `loja` | loja de referência no cadastro | Centro, Norte, Sul, Leste ou Oeste |

| `idade` | idade em 2025 | anos |

| `renda_familiar` | renda familiar mensal declarada no cadastro | R\$ mil por mês; **vazio** quando o cliente não informou |

| `distancia_km` | distância em linha reta entre o endereço do cadastro e a loja de referência | km |

| `canal_adesao` | canal em que o cliente aderiu ao programa | loja, aplicativo ou site |

| `usa_app` | uso do aplicativo da Cisne em 2025 | 1 se usou ao menos uma vez; 0 caso contrário |

| `cupom` | participação no piloto de cupons personalizados | 1 se recebeu os cupons em 2025; 0 caso contrário |

| `visitas` | compras registradas no programa em 2025 | número de compras |

| `gasto_anual` | soma das compras registradas no programa em 2025 | R$ |

| `renovou` | renovação do programa para 2026 | 1 se renovou; 0 caso contrário |



### Regras e informações do negócio



- **Piloto de cupons:** em dezembro de 2024, a Cisne atribuiu independentemente a cada cliente a possibilidade de receber cupons personalizados mensais durante 2025, com probabilidade 1/2 para cada cliente, sem impor grupos de tamanho idêntico. Os demais não receberam cupons. Cada cliente com cupom custou à rede cerca de **R\$ 120 no ano**, entre descontos concedidos e envio.

- **Margem:** a margem bruta média da rede é de **20% do valor vendido**.

- **Aplicativo:** o uso do aplicativo é escolha do cliente; ninguém foi sorteado para usá-lo.

- **Compras sem cartão:** compras feitas sem identificar o cartão do programa não são registradas. Um cliente pode ter zero visitas registradas no ano.

- **Quem pode participar:** o programa é aberto a qualquer pessoa física, inclusive donos de pequenos negócios que compram para revenda.

- **Renda:** declarada no cadastro, sem verificação; o preenchimento é opcional.



## `receita_mensal_cisne.csv` — Extensão opcional



Uma linha representa um mês, de janeiro de 2016 a dezembro de 2025.



| Coluna | Significado | Unidade |

|---|---|---|

| `mes` | mês de referência | texto `AAAA-MM` |

| `receita_mil` | receita total da rede no mês, com ajuste sazonal feito pela equipe de planejamento | R\$ mil |



## Integridade



Confira os arquivos antes de começar:



| Arquivo | SHA-256 |

|---|---|

| `clientes_cisne.csv` | `3e5951beb681ab52023168e2dce4fc83558d57ba48d63c59a7ed19509379947e` |

| `receita_mensal_cisne.csv` | `3e3cdebb67ca123ce953a96e489726e5a0789c2a5d83da7dc854216ad5bf3d86` |



Não altere os arquivos originais. Faça as transformações no seu notebook.



## Convenção de custo e margem



Para a conta didática, R\$ 120 é custo incremental por cliente atribuído ao cupom, ainda não deduzido da margem de 20%. Confirmar registro antes/depois de descontos em aplicação real. Não interpretar renovação como receita futura observada. Dados não contêm quadro de pessoal, horas ou salários.

