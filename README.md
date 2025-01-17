# Análise dos dados do RENAEST

## Introdução

O RENAEST (Registro Nacional de Acidentes e Estatísticas de Trânsito)
foi criado em 2006, a partir da resolução nº 208 do CONTRAN (Conselho
Nacional de Trânsito). O Registro conta com dados sobre data, local e
tipo de sinistro de trânsito, além de informações sobre as
características das vítimas, como sexo, faixa etária e quantidade de
envolvidos. O RENAEST é uma base de dados pública, que pode ser acessado
em
<https://www.gov.br/infraestrutura/pt-br/assuntos/transito/conteudo-Senatran/registro-nacional-de-acidentes-e-estatisticas-de-transito>

## Objetivo

O objetivo do código incluído neste repositório é analisar a qualidade
dos dados que estão sendo fornecidos pelo RENAEST de forma aberta.

## Estrutura

Este repositório contém os seguintes arquivos:

| Diretório   | Arquivo                          | Descrição                                                                                      |
|-------------|----------------------------------|------------------------------------------------------------------------------------------------|
| `data/`     |                                  | Contêm os dados processados do RENAEST                                                         |
|             | `vitimas.rda`                    | Base de dados das vítimas, em formato `rda`                                                    |
|             | `acidentes.rda`                  | Base de dados dos acidentes, em formato `rda`                                                  |
| `data-raw/` |                                  | Contêm os scripts de importação dos dados brutos do RENAEST                                    |
|             | `vitimas.R`                      | Script de importação dos dados de vítimas                                                      |
|             | `acidentes.R`                    | Script de importação dos dados de acidentes                                                    |
| `plot/`     |                                  | Contêm todos os gráficos de análise exportados.                                                |
| `R/`        |                                  | Diretório com todos os scripts que aplicam os métodos deste trabalho                           |
|             | `00_main.R`                      | Script principal que executa o projeto. Pode ser executado com o comando `Rscript R/00_main.R` |
|             | `01_organizacao_dados.R`         | Limpa e organiza os dados de entrada                                                           |
|             | `02_tabelas_perc_nas.R`          | Contabiliza a quantidade de vazios em cada coluna                                              |
|             | `03_graficos_pna_sinistros_cv.R` | Calcula outras variáveis: covariação, sinistros, etc.                                          |
|             | `04_export.R`                    | Exporta todos os gráficos                                                                      |
