# BasicLatex
\documentclass[14pt,a4paper,onecolumn]{article}
\usepackage[brazil]{babel}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{spverbatim}
\author{João Caetano}
\title{Anotações Sobre o Estudo de Latex}
\begin{document}
\maketitle
\tableofcontents
\pagebreak

\section{Código Básico Para se Iniciar a Escrita de Um Texto}
\begin{spverbatim}
%Define as características do texto como Modelo Básico(article),tamanho da letra(14pt),tamanho do papel(a4paper), número de colunas por página.
\documentclass[14pt,a4paper,onecolumn]{article}
%Define os pacotes necessários para se escrever o texto dependendo da língua e dos recursos necessários.(Os textos apresentados são as versões que tem funcionado melhor até o momento pelas minhas pesquisas
\usepackage[brazil]{babel}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
%O seguinte pacote serve para utilizar a funcionalidade de escrita de linhas de comando verbatim permitindo que tenhamos linhas quebradas
\usepackage{spverbatim}
%Insere o autor do trabalho
\author{João Caetano}
%Insere o título do trabalho
\title{Anotações Sobre o Estudo de Latex}
%Inicia o documento
\begin{document}
%Adiciona o título do trabalho
\maketitle
%Adiciona o índice definido pelas seções que foram criadas
\tableofcontents
%Gosto de deixar o índice separado. Então insiro aqui uma quebra de página
\pagebreak
%Cria seções enumeradas
\section{}
\subsection{}
\subsubsection{}
%Permite que se adicione enumerações
\begin{itemize}
\item
\item
\end{itemize}
%Como realizar citações simples. Devemos citar entre chaves o código definito para citação.
\cite{referencia}
%Inserir a bibliografia
\begin{thebibliography}
%Cria a referência de um artigo específico. Um ponto importante é que os comandos \bibitem e \emph devem estar um abaixo do outro
\bibitem{TesteDeCitacao} Oetiker:
\emph{The Not So Short Introduction to \TeX},(2018)
%Finaliza a Bibliografia
\end{thebibliography}
%Finaliza o documento
\end{document}

%Se for necessário realizar a inserção de linhas de comando deve-se criar uma um ambiente específico verbatim
\begin{spverbatim}
%end{spverbatim}

\end{spverbatim}

\section{Como executar esse código básico utilizando linhas de programação}
Quando vamos executar um código no cmd pontos importantes para consideramos são:

\begin{itemize}
\item Abrir o console ou o cmd e direcionar o mesmo para o diretório onde esta o arquivo com o código base para a geração do texto utilizando o comando "cd".

\begin{spverbatim}
cd /Users/jcaetano/Dropbox/Anotações/latex

\end{spverbatim}

\item Utilizar o comando "pdflatex" seguido do nome do arquivo na pasta com a sua respectiva extinção.

\begin{spverbatim}
pdflatex latex.txt

\end{spverbatim}

\item Depois de executado irá aparecer na mesma pasta em que está o arquivo um arquivo pdf com o texto já compilado.

\end{itemize}

\section{Dicas importantes para quem está escrevendo um texto em latex}

\begin{itemize}
\item Ao escrever um parágrafo um ponto importante é a considerado de que parágrafos separados devem ter uma linha de espaçamento para que o programa consiga renderizar o arquivo como parágrafos separados. Oetiker\cite{TesteDeCitacao}
\end{itemize}

\section{Orientação Básica para se criar uma bibliografia \cite{ShareLatex}}
\begin{spverbatim}
Para se criar uma bibliografia básica devemos iniciar pela criação de um ambiente de criação de bibliografia
\begin{theblibliography}{99}% A terminologia apresentada nas chaves em separado especifica a quantidade de itens que serão inseridos na bibliografia. É importante que esteja especificado para que apareçam os números correpondentes antes da referencia.
O próximo passo para se criar uma citação de maneira eviciente é estabelecer o indexador para que possamos realizar a citação da referencia ao longo do texto utilizando o comando "\cite{indexador}". Essa ação pode ser realizada utilizando-se o seguinte comando:
\bibitem{indexador}
Autor do trabalho
%Título do Trabalho
\textit{Coyote behavior: Implications for manegement}
%Data da publicação
(1976).

Depois que realizamos todas as citações Fechamos o ambiente que gera a citação bibliográfica utilizando o seguinte termo:
\end{thebibliography}

\end{spverbatim}

%Bibliografia
\begin{thebibliography}{99}
\bibitem{TesteDeCitacao} 
Oetiker:
\textit{The Not So Short Introduction to \TeX},(2018)

\bibitem{ShareLatex}
ShareLatex
\textit{Bibliography management with bibtex}
(2018). Website:https://www.sharelatex.com/learn/Bibliography_management_with_bibtex

\end{thebibliography}

\end{document}
