# Template do Trabalho de Conclusão de Curso do DEP
Template criado em Latex para o trabalho final de curso de Engenharia de Produção. O template é uma adequação da biblioteca Abntex ao modelo de trabalho de conclusão do curso.

## Modo de Uso

### Divisão das pastas

#### Bibliografia

Aqui são colocadas as referências estruturadas do trabalho. Para efetuar a citação adequada é necessário adicionar a referência no arquivo bibliografia.bib. É possível compreender melhor o uso no [link](https://pt.overleaf.com/learn/latex/Bibliography_management_with_bibtex).

#### Externos

Aqui são colocadas as informações anteriores ao texto, para preencher a capa e contra-capa é necessário ajustar o arquivo info-autor.tex. O arquivo capa.tex não necessita ser alterado.

#### Internos

A pasta internos, contempla todos os demais elementos do texto. No template, ela é dividida em 3 pastas, pré-textuais, textuais e pos-textuais.

##### Pré-textuais
Nos elementos pré-textuais estão as listas (lista de abreviaturas, figuras, quadros, tabelas e simbolos, sumário), também compreende elementos de escrita como resumo e abstract, agradecimentos, dedicatória, epigrafe, errata, folha de aprovação e folha de rosto.

A folha de aprovação e ficha catalográfica, incluem um arquivo em pdf no texto. Esses arquivos estão no diretório raiz do texto, nomeados "ata.pdf" para a folha de aprovação e "ficha.pdf" para a ficha catalográfica.


##### Textuais
Nos elementos textuais estão os capítulos do trabalho. Aqui são apresentados também alguns exemplos de utilização do código para elementos de figura, tabela, quadro e citações

###### Exemplo quadro
```latex
\begin{quadro}[H]
\tiny
% Please add the following required packages to your document preamble:
% \usepackage{multirow}
\legenda{Exemplo de quadro 1}
\label{Quadro:exemplo1}
\begin{tabular}{|r|l|l|l|l|l|}
\hline
Exemplo 1 & Exemplo 2 & Exemplo 3 & Exemplo 4 \\ \hline
1         & 1         & 1         & 2         \\ \hline
2         & 3         & 4         & 5         \\ \hline
44        & 2         & 1         & 2         \\ \hline
\end{tabular}
\source{Exemplo}
\end{quadro}
```

###### Exemplo tabela
```latex
\begin{table}[H]
\IBGEtab{%
  \tiny%
  \legenda{Exemplo tabela 1}%
  \label{Tab:tabela-e1}
}{%
  \begin{tabular}{m{0.3\textwidth}m{0.2\textwidth}m{0.2\textwidth}}

  \toprule
  Exemplo 1 & Exemplo 2 & Exemplo 3 & Exemplo 4 \\
  \midrule \midrule
    1         & 1         & 1         & 2         \\
    2         & 3         & 4         & 5         \\
    44        & 2         & 1         & 2         \\
  \bottomrule
\end{tabular}%
}{%
  \fonte{Autor}%
  }
\end{table}
```

###### Exemplo Figura
```latex
 \begin{figure}[H]
    \begin{center}
      % fbox faz uma borda ao redor do seu argumento
		\legenda{Exemplo de Imagem com Latex}
		\fbox{\includegraphics[width=0.95\linewidth]{internos/textuais/capitulo1-introducao/figuras/ctec.jpg}}
		\source{Internet}
		\label{Fig:exemplo1}
	\end{center}
\end{figure}

```

###### Exemplo citação durante
```latex
 \citeonline{referencia}
```

###### Exemplo citação após
```latex
 \citeo{referencia}
```

###### Exemplo paragrafo
```latex
\paragrafo{}
Texto Texto Texto Texto Texto Texto Texto Texto Texto Texto
Texto Texto Texto Texto Texto Texto Texto Texto Texto Texto
Texto Texto Texto Texto Texto Texto Texto Texto Texto Texto
Texto Texto Texto Texto Texto Texto Texto Texto Texto Texto
Texto Texto.
```

###### Exemplo de adição de outro arquivo tex
```latex
\input{caminho do arquivo}
```

##### Pós-textuais

Os elementos pós-textuais são anexos, apêndices e a bibliografia. De maneira simples os apêndices e anexos podem ser inclusos no como capítulos no arquivo e automaticamente já serão integrados ao texto. A bibliografia apenas adiciona as referências aos trabalhos citados, então dessa forma é necessário apenas adicionar a referência estruturada e realizar a citação adequada.