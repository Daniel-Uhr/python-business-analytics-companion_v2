# Roteiro do Projeto Final — Supermercados Cisne



## Propósito



Este roteiro organiza o trabalho sem determinar os modelos, os comandos ou os resultados. As decisões são suas: registre cada uma, com a justificativa, de forma que outra pessoa consiga reproduzi-la e avaliá-la.



## As perguntas



- **P1 — Aplicativo e gasto:** os clientes que usam o aplicativo gastam mais do que clientes semelhantes que não usam? Quanto? O que esse resultado permite — e não permite — concluir sobre levar mais clientes ao aplicativo?

- **P2 — Piloto de cupons:** os cupons personalizados aumentaram as visitas, o gasto e a renovação do programa? Vale a pena estendê-los a todos os clientes?

- **Extensão opcional — Receita da rede:** a receita mensal cresce por uma tendência ou acumula choques? Quanto cresce ao ano?



## Entrega



- arquivo: `projeto_final_nome_sobrenome.ipynb`, feito a partir do `template.ipynb`;

- **prazo:** [definido pelo professor];

- um único notebook, com caminhos relativos para `dados/`;

- executar **Restart Kernel and Run All** antes da entrega.



## 1. Compreensão da base



### Orientação



Antes de qualquer modelo, entenda o que cada linha e cada coluna representam.



### Dica



Qual é a unidade de observação? Qual é o período? Quais variáveis descrevem o cliente e quais registram resultados de 2025? Qual informação foi sorteada e qual foi escolhida pelo cliente?



### Alerta



**A forma como os dados foram gerados — por escolha, por sorteio ou por registro — define o que eles podem responder.**



## 2. Qualidade dos dados



### Orientação



Investigue ausências, zeros, valores extremos e a coerência entre variáveis antes de modelar.



### Dica



Quem não informou a renda se parece com quem informou? O que significa um cliente com zero visitas? As variáveis são coerentes entre si? Há clientes muito diferentes dos demais? Quem são eles, à luz do dicionário?



### Alerta



**Uma observação extrema não é necessariamente um erro. Não exclua nem impute sem investigar e sem registrar o efeito da decisão.**



## 3. Perguntas e variáveis resposta



### Orientação



Para cada pergunta, defina a variável resposta e identifique sua natureza.



### Dica



A resposta é contínua, uma contagem ou binária? É assimétrica? Tem zeros? Qual escala de interpretação faz sentido para a decisão — reais, percentuais ou pontos percentuais?



### Alerta



**Zeros não podem entrar em um logaritmo sem uma decisão explícita.**



## 4. P1 — Especificação e estimação



### Orientação



Escolha e justifique uma especificação de referência e estime-a com a inferência adequada.



### Dica



Quem usa o aplicativo se parece com quem não usa? Quais diferenças entre esses grupos também se relacionam com o gasto? Que forma funcional faz sentido para cada variável? Que erros-padrão os dados pedem?



### Alerta



**Controlar uma consequência da variável de interesse muda a pergunta. Pense no papel de cada variável antes de incluí-la.**



## 5. P1 — Diagnóstico e robustez



### Orientação



Examine os resíduos e as observações influentes e verifique se a conclusão principal depende de escolhas razoáveis.



### Dica



O que acontece com o resultado quando você muda a forma funcional, a amostra ou o tratamento das ausências? Quais observações mais influenciam a estimativa? Apresente as alternativas em uma tabela comparativa.



### Alerta



**Robustez não é procurar a especificação com o resultado preferido. Escolha a especificação por argumentos, não pelo p-valor.**



## 6. P2 — O sorteio



### Orientação



Examine a comparabilidade realizada entre os grupos, sem usar testes de balanceamento como certificação e explique o que o sorteio permite concluir.



### Dica



Compare os dois grupos nas características registradas antes do piloto. Uma diferença entre grupos sorteados significa que o sorteio falhou? O que fazer se surgir alguma?



### Alerta



**O sorteio sustenta a leitura causal da atribuição do cupom, sob as hipóteses do desenho; não identifica automaticamente uso do app ou resgate.**



## 7. P2 — Efeitos sobre visitas, gasto e renovação



### Orientação



Estime o efeito do cupom sobre cada resultado com um modelo coerente com sua natureza e com a inferência adequada.



### Dica



Qual escala de efeito é mais útil para cada resultado? A variância das visitas é compatível com o que o modelo supõe? Incluir controles muda a estimativa ou só a precisão — e por quê?



### Alerta



**Coeficientes de modelos não lineares não são lidos diretamente como unidades ou probabilidades.**



## 8. P2 — Heterogeneidade e decisão econômica



### Orientação



Avalie se o efeito é parecido entre grupos de clientes e traduza os resultados em uma decisão para a diretoria.



### Dica



O cupom paga seu custo? Use o custo e a margem do dicionário e considere a incerteza da estimativa. A renovação acrescenta valor? Se você examinar grupos, quantas comparações fez, e quão firme é cada uma?



### Alerta



**Um efeito pode ser estatisticamente significativo e economicamente pequeno — ou economicamente relevante e impreciso.**



## 9. Extensão opcional — Receita da rede



### Orientação



Caracterize a tendência e a persistência da receita mensal e meça seu crescimento.



### Dica



O gráfico sugere uma média estável, uma tendência regular ou uma trajetória que vagueia? Que termos determinísticos o teste de raiz unitária deve incluir? Como expressar o crescimento ao ano?



### Alerta



**“Não rejeitar” a raiz unitária não é prova de raiz unitária, e o teste não substitui o gráfico.**



## 10. Conclusões, recomendações e limites



### Orientação



Responda às perguntas da diretoria em linguagem de decisão, separando evidência, interpretação e recomendação.



### Dica



Para cada pergunta: o que os dados mostram, com que incerteza, o que isso significa para a Cisne e o que fazer. Quais são os limites de cada conclusão — desenho, dados sintéticos, ausências, extremos, um único ano?



### Alerta



**Associação não demonstra causalidade, e recomendação sem evidência não é conclusão analítica.**



## Checklist antes da entrega



- [ ] A unidade de observação e a origem de cada variável foram descritas.

- [ ] Ausências, zeros e extremos foram investigados, e as decisões foram registradas.

- [ ] A natureza de cada variável resposta orientou a escolha do modelo.

- [ ] A especificação de referência foi justificada antes de olhar os p-valores.

- [ ] Os erros-padrão são adequados aos dados.

- [ ] Os efeitos foram interpretados com unidade — reais, percentuais ou pontos percentuais.

- [ ] Há diagnóstico e uma tabela de robustez.

- [ ] Significância estatística e relevância econômica foram distinguidas.

- [ ] A leitura causal de cada pergunta é coerente com o desenho dos dados.

- [ ] Há recomendações e limites.

- [ ] O notebook executa do início ao fim em kernel limpo.



## Convenção empresarial



Margem de 20% e custo incremental anual de R\$ 120 por atribuição são premissas do briefing. O custo ainda não foi deduzido da margem usada na conta. Distinga contribuição líquida corrente de cenário futuro de renovação. Não conte descontos duas vezes. Registre lacunas de estoque, capacidade e atendimento; não estime contratações sem horas, produtividade e salários.

