# Diagrama de Sankey para Mudanças de Uso e Cobertura da Terra

Este arquivo trabalha a manipulação dados geoespaciais através de um gráfico de transição chaamado Sankey. O diagrama de Sankey facilita a visualização de dados entre diferentes classes de uso da terra ao longo do tempo, sendo uma ferramenta útil para análise de dados de mudanças de uso e cobertura. Além da visualização em softwares de SIGs, a análise espacial por gráficos em linguagem de programação fornece apoio fundamental para o desenvolvimento de projetos geoinformacionais. 

O atual projeto foi desenvolvido utilizando o framework [Dash](https://dash.plotly.com/) e o módulo [plotly](https://plotly.com/python/), que permite a criação de gráficos interativos em Python. 

## Descrição do Projeto

O código presente no projeto lê dados de um arquivo TSV contendo as colunas `from`, `to` e `Weight`, que representam, respectivamente, a origem, o destino e o peso das transições. Essas informações são então processadas para construir o diagrama de Sankey, onde cada nó representa uma classe de uso e cobertura   da terra em um ano específico.

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

- `from`: Classe de origem      #letras minusculas
- `to`: Classe de destino       #letras minusculas
- `Weight`: Peso (quantidade ou valor) da transição entre as classes      #apenas primeira letra maiúscula

Exemplo de estrutura do arquivo TSV (conforme arquivo "teste1.tsv" presente no repositório):

```tsv
from;    to;    Weight;
Floresta Natural|1985;   Pastagem|2000;   50;
Floresta Natural|1985;   Agricultura|2000;   30;
Floresta Natural|1985;   Área Urbana|2000;   20;
Pastagem|2000;   Pastagem|2015;   15;
Pastagem|2000;   Agricultura|2015;   30;
Pastagem|2000;   Área Urbana|2015;   5;
Agricultura|2000;   Pastagem|2015;   0;
Agricultura|2000;   Agricultura|2015;   30;
Agricultura|2000;   Área Urbana|2015;   0;
Área Urbana|2000;   Pastagem|2015;   0;
Área Urbana|2000;   Agricultura|2015;   0;
Área Urbana|2000;   Área Urbana|2015;   20;
```
Outro exemplo mais complexo que pode ser trabalhado está dentro do arquivo "teste2.tsv" onde podem ser vizualizados os dados do Cobertura do Mapbiomas Brasil (Coleção - 5) sobre a Amazônia Legal. O diagrama de Sankey gerado foi utilizado no capítulo "EVOLUÇÃO RECENTE DO DESFLORESTAMENTO NA AMAZÔNIA LEGAL: SUPRESSÃO, TRAJETÓRIAS E SEUS PADRÕES" do livro "CARTOGRAFIAS DO ONTEM, HOJE E AMANHÃ"¹

```
¹AMARAL, F. G.; MAGALHAES, D. M. ; AMBROSIO, B. G. ; PAOLINO, C. C. ; SANTANA, B. S. F. ; CRUZ, C. B. M. . EVOLUÇÃO RECENTE DO
DESFLORESTAMENTO NA AMAZÔNIA LEGAL: SUPRESSÃO, TRAJETÓRIAS E SEUS PADRÕES. In: Paulo Márcio Leal de Menezes, Manoel do Couto Fernandes, Carla Bernadete Madureira Cruz. (Org.). Cartografias do Ontem, Hoje e Amanhã. 1ed.Curitiba: Appris, 2022, v. 1, p. 239-266.
```
## Contribuição
Sinta-se à vontade para abrir issues e pull requests para adicionar novas funcionalidades, corrigir bugs ou melhorar a documentação.

## Licença
Este projeto está licenciado sob Apache Licence 2.0
