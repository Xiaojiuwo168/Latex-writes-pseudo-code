# Latex-writes-pseudo-code

##亲测有效

##1、导入依赖包：

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

```
![image](https://user-images.githubusercontent.com/85736050/206119391-b4fae995-6b70-4094-a08f-b9362ed68d78.png)



