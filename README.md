# Diagrama de Sankey para Mudanças de Uso e Cobertura da Terra

Este projeto cria um diagrama de Sankey que representa a substituição e variação de uso e cobertura da terra em diferentes classes e anos. Ele foi desenvolvido utilizando o framework [Dash](https://dash.plotly.com/) e o módulo [plotly](https://plotly.com/python/), que permite a criação de gráficos interativos em Python. O diagrama de Sankey facilita a visualização das transições entre diferentes classes de uso da terra ao longo do tempo, sendo uma ferramenta útil para análise de mudanças de cobertura e uso do solo.

## Descrição do Projeto

O código presente no projeto lê dados de um arquivo TSV contendo as colunas `from`, `to` e `Weight`, que representam, respectivamente, a origem, o destino e o peso das transições. Essas informações são então processadas para construir o diagrama de Sankey, onde cada nó representa uma classe de uso do solo em um ano específico.

## Pré-requisitos

Para rodar o projeto, você precisará das seguintes bibliotecas:

- Dash
- Plotly
- Pandas

Essas bibliotecas podem ser instaladas executando:

```bash
!pip install Dash
!pip install plotly
!pip install pandas
```

## Como Rodar o Projeto

1. Carregue o código no Google Colab ou em outro ambiente de execução que suporte Dash e Plotly.
2. Faça o upload do arquivo de dados no formato TSV.
3. Execute o código sankeylulc.ipynb fornecido neste repositório.

### Estrutura do Arquivo TSV

O arquivo TSV deve conter três colunas:

- `from`: Classe de origem #letras minusculas
- `to`: Classe de destino #letras minusculas
- `Weight`: Peso (quantidade ou valor) da transição entre as classes #apenas primeira letra maiúscula

Exemplo de estrutura do arquivo TSV:

```tsv
from    to    Weight
Floresta Natural|1985   Pastagem|1989   50
Pastagem|1989   Agricultura|1992   30
```
