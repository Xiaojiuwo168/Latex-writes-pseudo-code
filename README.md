# Latex-writes-pseudo-code

##Pro-tested to be effective

##1. Import the dependency package.

\usepackage[ruled]{algorithm2e}

```
\begin{algorithm}[]  %其中这里面不能有H不然会报错，不过不影响结果
	\caption{algorithm caption}%算法名字
	\LinesNumbered %要求显示行号
	\KwIn{input parameters A, B, C}%输入参数
	\KwOut{output result}%输出
	some description\; %\;用于换行
	\For{condition}{
		only if\;
		\If{condition}{
			1\;
		}
	}
	\While{not at end of this document}{
		if and else\;
		\eIf{condition}{
			1\;
		}{
			2\;
		}
	}
	\ForEach{condition}{
		\If{condition}{
			1\;
		}
	}
\end{algorithm}

![image](https://user-images.githubusercontent.com/85736050/206119391-b4fae995-6b70-4094-a08f-b9362ed68d78.png)

```

##2. Import the dependency package.
\usepackage[noend]{algpseudocode}
\usepackage{algorithmicx,algorithm}

```
\begin{algorithm}[t]
\caption{algorithm caption} %算法的名字
\hspace*{0.02in} {\bf Input:} %算法的输入， \hspace*{0.02in}用来控制位置，同时利用 \\ 进行换行
input parameters A, B, C\\
\hspace*{0.02in} {\bf Output:} %算法的结果输出
output result
\begin{algorithmic}[1]
\State some description % \State 后写一般语句
\For{condition} % For 语句，需要和EndFor对应
　　\State ...
　　\If{condition} % If 语句，需要和EndIf对应
　　　　\State ...
　　\Else
　　　　\State ...
　　\EndIf
\EndFor
\While{condition} % While语句，需要和EndWhile对应
　　\State ...
\EndWhile
\State \Return result
\end{algorithmic}
\end{algorithm}

![image](https://user-images.githubusercontent.com/85736050/206119891-bbd79868-fa80-4ec1-97cd-ca48494304b1.png)

```

##3. Import the dependency package.
%\usepackage{algorithm}
%\usepackage{algorithmicx}
%\usepackage{algpseudocode}  % 如果不想在算法伪代码模块中显示 end for 和 end while，则使用  %\usepackage[noend]{algpseudocode}


```
\begin{algorithm}[h] 
	\renewcommand{\algorithmicrequire}{\textbf{Input:}}
	\renewcommand{\algorithmicensure}{\textbf{Output:}}
	\caption{Environmental Selection} 
	\label{alg::conjugateGradient} 
	\begin{algorithmic}[1] 
		\Require 
		The population $ P_t $,the probabity for crossover operation
		$ p_c $, the probability for mutation operation $ p_m $,
		the mutation operation list $ l_m $,the probabilities
		of selecting different mutation operations $ p_l $.  
		\Ensure 
		The offspring population $ Q_t $;
		\State $ Q_t $ ← $\phi$;
		\Repeat 
		\State $ p_1 $ ← Randomly select two individuals from $ P_t $,
		and from the two then select the one with the better fitness;
		\State $ p_2 $ ← Repeat Line 4;
		\Repeat
		\State Repeat Line 5;
		\Until{($ p_1 $ == $ p_2 $)}
		%\whiledo{$ p_1 $ == $ p_2 $}{\State Repeat Line 5;} 
		\State $ r $ ← Randomly generate a number from (0,1);  
		\Until{($\lvert Q_t \rvert < \lvert P_t \rvert$)}
		\State Return the individual having the best fitness in $P_t$;
	\end{algorithmic} 
\end{algorithm}

![image](https://user-images.githubusercontent.com/85736050/206119986-48606756-5612-4715-bcf0-55651f3c4582.png)


```






