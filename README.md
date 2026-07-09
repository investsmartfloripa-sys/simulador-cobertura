# Simulador de Decisão — Compra da Cobertura (25%)

Página interativa para apoiar a decisão de funding de uma operação de compra,
reforma e revenda de imóvel (flip), com participação de 25%.

**Acesse:** https://investsmartfloripa-sys.github.io/simulador-cobertura/

## O que a página compara

1. **Sacar as aplicações** — o retorno total que deixa de ser ganho (renda +
   valorização: recomprar as cotas mais caras depois faz parte do custo) entra
   como custo de oportunidade, mais um custo de resgate configurável (padrão 1%
   do valor sacado — spread de saída e marcação a mercado).
2. **Crédito colateralizado** — as aplicações continuam rendendo; os juros do
   crédito (CDI + spread mensal + IOF, ou taxa prefixada mensal) entram como custo.
3. **O efeito do prazo de venda** — como o preço de venda não corrige com o
   tempo, cada mês a mais dilui a rentabilidade anualizada da operação. O tooltip
   do gráfico, o cartão do flip e a tabela mostram a taxa anualizada em cada
   prazo, lado a lado com o que a aplicação renderia.

## Como usar

Todos os campos são editáveis diretamente na página — valores do imóvel,
participação, faixa de retorno das aplicações, condições do crédito e
impostos. O slider de prazo atualiza os cartões de resultado, o gráfico, a
abertura dos números e a tabela.

São **dois gráficos**, um para cada leitura:

- **vs. manter aplicado** — resultado de cada caminho além de simplesmente
  deixar o capital rendendo (a faixa amarela de incerteza fica no saque, cujo
  custo de oportunidade depende do retorno dos FIIs).
- **Lucro absoluto** — colunas empilhadas nos prazos-chave (6 a 36 meses, mais
  o prazo do slider, destacado): acima do zero o que entra (lucro do flip; no
  crédito, também o retorno dos FIIs mantidos), abaixo do zero o que sai
  (resgate; juros e IOF). O traço escuro marca o resultado líquido de cada
  coluna, o fio vertical mostra o resultado do crédito com FIIs do mínimo ao
  máximo, e a linha tracejada é a referência de não fazer a operação.

A incerteza representada é sempre a mesma — o retorno dos FIIs entre o mínimo
e o máximo (faixa amarela no primeiro gráfico, fio vertical no segundo) — e a
diferença entre crédito e saque é idêntica nas duas leituras; o que muda é o
ponto de referência.

Há ainda um seletor de **cenário de retorno (mínimo / médio / máximo)** que
define qual ponto da faixa alimenta os cartões, a tabela e a abertura dos
números, e a **tabela alterna** entre as leituras relativa e absoluta.

## Premissas do modelo

- Aporte integral no mês zero.
- Crédito pago integralmente na venda (bullet), com juros compostos mensais.
- IOF (modalidade CDI + spread): 0,38% fixo + 0,0082% ao dia, limitado a 365 dias.
- Aplicações isentas de IR por padrão (LCI, LCA, CRI, CRA, debêntures
  incentivadas); opcionalmente aplica-se a tabela regressiva (22,5% → 15%).
- IR de 15% sobre o ganho de capital do imóvel (editável).

## Aviso

Simulação educacional para apoio à decisão — **não constitui recomendação de
investimento**. Custos de transação (ITBI, cartório, corretagem, condomínio e
IPTU durante a obra) não estão incluídos e devem ser considerados nos campos de
custo ou descontados do valor de venda.
