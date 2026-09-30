Em parceria com a DIO e sob orientação de Felipe Aguiar o Felipão apresento.

# Simulador de Investimentos em Fundos Imobiliários — Excel

## Sobre o projeto

Este projeto consiste no desenvolvimento de uma ferramenta de simulação de investimentos em Fundos de Investimento Imobiliário (FIIs), utilizando Excel.

A solução permite que o usuário informe diferentes parâmetros de investimento e visualize projeções de patrimônio acumulado, dividendos mensais e distribuição sugerida da carteira de acordo com diferentes perfis de investimento.

O projeto foi desenvolvido como exercício prático de aplicação de Excel em um problema financeiro, utilizando fórmulas, funções financeiras, consultas, validação de dados, parametrização, cenários e visualização.

---

## Objetivo

Desenvolver uma ferramenta simples e interativa que permita simular a evolução de investimentos ao longo do tempo a partir de diferentes parâmetros definidos pelo usuário.

A ferramenta busca facilitar a compreensão da relação entre:

* valor investido mensalmente;
* prazo do investimento;
* taxa de rendimento;
* patrimônio acumulado;
* dividendos mensais projetados;
* perfil de investimento;
* distribuição dos aportes entre diferentes tipos de FIIs.

---

## Problema

Para um investidor iniciante, pode ser difícil visualizar como o valor dos aportes mensais e o prazo de investimento podem influenciar a formação de patrimônio ao longo do tempo.

A planilha procura transformar esses parâmetros em informações de fácil interpretação, permitindo testar diferentes cenários sem a necessidade de realizar os cálculos manualmente.

---

## Ferramentas utilizadas

* Microsoft Excel
* Fórmulas financeiras
* Funções de busca
* Validação de dados
* Referências absolutas e relativas
* Nomes definidos
* Tabelas de parametrização
* Gráficos
* Simulação de cenários

---

## Funcionalidades

A ferramenta permite:

* informar o salário;
* definir uma taxa de rendimento da carteira;
* informar o valor do investimento mensal;
* definir o período do investimento;
* informar uma taxa de rendimento mensal;
* calcular o patrimônio acumulado projetado;
* estimar dividendos mensais;
* comparar diferentes horizontes de investimento;
* selecionar um perfil de investimento;
* consultar automaticamente a distribuição sugerida para cada perfil;
* calcular os valores destinados a cada tipo de FII;
* visualizar a composição da carteira por meio de gráfico.

---

## Dados de entrada

Os principais parâmetros que podem ser alterados pelo usuário são:

| Parâmetro                 | Descrição                                     |
| ------------------------- | --------------------------------------------- |
| Salário                   | Renda mensal utilizada como referência        |
| Rendimento da carteira    | Taxa utilizada para estimar os dividendos     |
| Investimento mensal       | Valor destinado mensalmente aos investimentos |
| Prazo                     | Período do investimento em anos               |
| Taxa de rendimento mensal | Taxa utilizada na projeção do patrimônio      |
| Perfil                    | Conservador, Moderado ou Agressivo            |

A parametrização permite alterar os valores de entrada e observar automaticamente os impactos nos resultados.

---

## Cálculos realizados

### Patrimônio acumulado

O patrimônio projetado é calculado utilizando a função financeira `FV` (Future Value / Valor Futuro), considerando:

* valor do aporte mensal;
* número de períodos;
* taxa de rendimento mensal.

Conceitualmente:

```text
Patrimônio futuro =
aportes mensais + efeito da capitalização ao longo do tempo
```

### Dividendos mensais

A estimativa de dividendos é calculada a partir do patrimônio projetado e do rendimento definido para a carteira.

```text
Dividendos mensais =
Patrimônio acumulado × rendimento da carteira
```

### Cenários

A ferramenta apresenta diferentes horizontes de investimento, permitindo comparar projeções para:

* 2 anos;
* 5 anos;
* 10 anos;
* 20 anos;
* 30 anos.

Essa funcionalidade permite observar como alterações no prazo podem impactar o patrimônio projetado.

---

## Distribuição da carteira

A planilha utiliza uma segunda aba como base de parametrização dos perfis de investimento.

São considerados diferentes tipos de FIIs:

* Papel;
* Tijolo;
* Híbridos;
* FOFs;
* Desenvolvimento;
* Hotelarias.

A partir do perfil selecionado pelo usuário, a ferramenta utiliza uma função de busca para recuperar os percentuais correspondentes e calcular os valores destinados a cada categoria.

Essa estrutura permite separar a tabela de parâmetros dos cálculos apresentados ao usuário.

---

## Exemplo de simulação

Considerando os valores inicialmente configurados na planilha:

* Investimento mensal: R$ 500
* Prazo: 10 anos
* Taxa de rendimento mensal: 1,079%

A simulação resulta em um patrimônio projetado de aproximadamente:

**R$ 121.642**

O resultado é uma projeção matemática baseada nos parâmetros informados e não representa garantia de rentabilidade futura.

---

## Estrutura do projeto

```text
📁 simulador-investimentos-fii
│
├── 📊 Planilha Investimento.xlsx
│
└── 📄 README.md
```

### Planilha1

Contém:

* configurações;
* parâmetros de investimento;
* cálculo do patrimônio;
* estimativa de dividendos;
* cenários;
* seleção do perfil;
* distribuição dos investimentos;
* gráfico da composição da carteira.

### Planilha2

Contém a tabela de parametrização dos diferentes perfis de investimento e respectivos percentuais por tipo de FII.

---

## Principais conhecimentos aplicados

Durante o desenvolvimento foram aplicados conceitos de:

* organização e estruturação de informações;
* modelagem de uma solução em Excel;
* criação de parâmetros de entrada;
* fórmulas financeiras;
* funções de busca;
* validação de dados;
* criação de cenários;
* referências de células;
* nomes definidos;
* visualização de informações;
* raciocínio lógico e financeiro.

---

## Aprendizados

O desenvolvimento do projeto permitiu praticar a transformação de um problema financeiro em uma ferramenta estruturada de simulação.

Entre os principais aprendizados estão:

* utilização de fórmulas financeiras para projeções;
* criação de uma estrutura parametrizada;
* utilização de tabelas de referência para alimentar cálculos;
* construção de cenários;
* criação de mecanismos para interação com o usuário;
* organização de informações para facilitar a interpretação dos resultados.

---

## Limitações

A ferramenta possui finalidade educacional e de simulação.

Os resultados dependem diretamente dos parâmetros informados pelo usuário e das premissas utilizadas no modelo.

A simulação não considera, entre outros fatores:

* variações reais nos preços dos ativos;
* alterações nos dividendos;
* inflação;
* tributação;
* taxas e custos operacionais;
* mudanças nas condições de mercado;
* reinvestimento variável dos dividendos;
* risco individual de cada fundo.

Portanto, os resultados devem ser interpretados como projeções matemáticas dentro das premissas estabelecidas.

---

## Possíveis melhorias

Como evolução do projeto, podem ser incorporados:

* cálculo explícito do total aportado;
* comparação entre total aportado e patrimônio acumulado;
* gráficos de evolução patrimonial;
* comparação entre diferentes cenários;
* indicadores de rentabilidade;
* simulação com diferentes taxas de rendimento;
* controle de inflação;
* inclusão de aportes extraordinários;
* reinvestimento dos dividendos;
* dashboard interativo;
* migração dos dados e indicadores para Power BI.

---

## Conclusão

O projeto demonstra a aplicação do Excel na construção de uma solução de análise e simulação financeira, combinando entrada de dados, processamento, cálculos, parametrização e visualização de resultados.

A proposta também representa uma etapa prática no desenvolvimento de competências relacionadas à análise de dados e Business Analytics.

---

## Autor

**Rogerio Rodrigues da Costa**

Transição de carreira para Analytics, com experiência profissional em finanças, crédito, relacionamento com empresas, indicadores e análise de negócios.
