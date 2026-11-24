# Rubrica — Projeto Final de Estatística e Econometria Aplicada



## Uso



A rubrica avalia decisões analíticas, coerência, inferência, interpretação e reprodutibilidade. Código que executa sem erros é necessário, mas não suficiente. Total: **100%**.



| Dimensão | Peso | Excelente | Adequado | Parcial | Insuficiente |

|---|---:|---|---|---|---|

| Compreensão da base e das perguntas | 10% | Descreve unidade, período, origem de cada variável e o que cada pergunta exige; distingue escolha, sorteio e registro. | Descreve os elementos centrais, com pequenas omissões sem impacto. | Confunde parte da estrutura ou das perguntas. | Analisa sem compreender a base ou as perguntas. |

| Qualidade e preparação dos dados | 10% | Investiga ausências, zeros, extremos e coerência; registra decisões, alternativas e efeitos. | Trata os principais problemas e justifica a maior parte das decisões. | Diagnóstico incompleto ou decisões pouco justificadas. | Ignora a qualidade ou altera dados arbitrariamente. |

| Natureza de `Y` e especificação justificada | 15% | Escolhe modelos coerentes com cada resposta; justifica controles e forma funcional antes de olhar os p-valores; reconhece variáveis que mudam a pergunta. | Especificações adequadas, com justificativas suficientes. | Especificações parcialmente adequadas ou pouco justificadas. | Modelo incompatível com a resposta ou escolhido pelo p-valor. |

| Estimação e inferência | 15% | Estima corretamente e usa inferência adequada e identifica a covariância e suas hipóteses; apresenta intervalos de confiança e os lê corretamente. | Estimação e inferência corretas, com pequenas falhas de apresentação. | Inferência parcialmente inadequada ou mal interpretada. | Erros-padrão inadequados ou inferência incorreta. |

| Interpretação | 10% | Interpreta cada efeito com unidade e escala — reais, percentuais, pontos percentuais —, no ponto ou na média, conforme o caso. | Interpretações corretas, com pequenas imprecisões. | Interpretações vagas ou com unidades ausentes. | Lê coeficientes de índice como unidades ou probabilidades. |

| Diagnóstico | 10% | Examina resíduos, sobredispersão e observações influentes e conecta o diagnóstico às decisões. | Diagnóstico adequado e interpretado. | Diagnóstico mecânico ou desconectado das decisões. | Ausência de diagnóstico. |

| Robustez | 10% | Tabela comparativa com alternativas razoáveis (forma funcional, amostra, ausências, extremos, controles), interpretada. | Algumas alternativas relevantes, bem interpretadas. | Alternativas pouco relevantes ou não interpretadas. | Ausência de robustez ou busca pela especificação preferida. |

| Significância × relevância e decisão econômica | 8% | Separa significância de relevância; traduz o cupom em custo e margem, com a incerteza; recomendação proporcional à evidência. | Decisão econômica correta, com tratamento parcial da incerteza. | Conta econômica incompleta ou recomendação desproporcional. | Decisão pelo p-valor ou sem conta econômica. |

| Limites causais e coerência com o desenho | 7% | Lê a atribuição do cupom como efeito causal sob as hipóteses do sorteio, e o aplicativo como associação condicional, explicando por quê; discute confundimento não observado. | Distinção correta, com explicação breve. | Distinção incompleta ou inconsistente. | Afirma efeito causal do aplicativo ou ignora o desenho. |

| Reprodutibilidade e comunicação | 5% | Restart + Run All funciona; caminhos relativos; conferência dos arquivos; texto claro, com conclusões e recomendações separadas das evidências. | Notebook reproduzível e comunicação adequada. | Reprodução exige ajustes ou comunicação confusa. | Notebook não reproduzível. |



## Extensão opcional



A extensão de séries temporais não é obrigatória, e sua ausência não reduz a nota. Uma extensão correta — gráfico, termos determinísticos justificados, teste de raiz unitária lido com cautela, crescimento anual e interpretação — pode receber bônus de até cinco pontos, a critério do professor, com nota final limitada a 100.



## Erros conceituais graves



Podem reduzir substancialmente a avaliação da dimensão correspondente:



- aplicar logaritmo a zeros sem decisão explícita, ou descartar zeros sem registrar a mudança de pergunta;

- ler a associação entre aplicativo e gasto como efeito causal;

- controlar as visitas no modelo do gasto sem reconhecer que a pergunta mudou;

- ler coeficientes de Logit ou de Poisson diretamente como probabilidades ou unidades;

- usar erros-padrão usuais com heterocedasticidade ou sobredispersão relevantes;

- excluir observações extremas sem investigar e sem mostrar o efeito da exclusão;

- escolher a especificação pelo p-valor ou relatar apenas a especificação mais favorável;

- recomendar a extensão do cupom sem comparar benefício e custo;

- entregar notebook que não executa integralmente.



## Regra de soluções alternativas



Uma decisão diferente da solução de referência pode receber pontuação integral quando for substantivamente justificável, documentada, aplicada de forma consistente e acompanhada de seus efeitos sobre os resultados.

