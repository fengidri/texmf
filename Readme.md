## usage:

```
export export TEXINPUTS=.:/path/to/this:$TEXINPUTS
```




## 字体设置
要在 begin document 之后, 在 \input 之前无用.

## 在 frame 中使用 lstlisting
使用
```
\begin{frame}[fragile]
```


## lstset 设置关键词
```
\lstset{
  morekeywords={upssh,brew},  % if you want to add more keywords to the set
}
```


## 文章默认字体

可以在 document 之后先设置英文字体再设置中文字体.
```
\begin{document}
\ttfamily
\kaishu

{\songti 宋体} \quad {\heiti 黑体} \quad {\fangsong 仿宋} \quad {\kaishu 楷书}

中文字体的 \textbf{粗体} 和 \textit{斜体} 。

%字体大小,根据normalsize的大小确定，normalsize 在文档类的参数决定
{\tiny           Hello}\\
{\scriptsize     Hello}\\
{\footnotesize   Hello}\\
{\small          Hello}\\
{\normalsize      Hello}\\
{\large          Hello}\\
{\Large          Hello}\\
{\LARGE          Hello}\\
{\huge           Hello}\\
{\Huge           Hello}\\
```
ctex 中文字体的设置会保存英文字体的配置信息. 只对中文生效.


## titlepage
设置
```
\title{}
\author{}
\date{} 可以不设置, 自动生成
\institute{} 机构
\subtitle()
```

beamer 下如下生成 title page
```
\frame{\titlepage}
```

## beamer 色彩

```
\setbeamercolor{background canvas}{bg=colorbcd}
\setbeamercolor{frametitle}{bg=colortitlebg,fg=colortitlefg}
```
setbeamercolor 可以修改 beamer 指定的结构的色彩.

* frametitle: 第一个 frame 里的 title 的色彩
* background canvas: frame 背景色


## beamer 字体

```
\setbeamerfont{frametitle}{size = \large}
```
修改指定 beamer 的字体的格式

## tcolorbox 基本用法
```
\begin{tcolorbox}[title={title}]
。。。。。
\tcblower
。。。。。
\end{tcolorbox}
```


## beamer 多列

```
  \begin{columns}[t]
    \begin{column}{0.25\textwidth}
      \begin{tcolorbox}[title = {}]
            ....
      \end{tcolorbox}
    \end{column}

    \begin{column}{0.42\textwidth}
      \begin{tcolorbox}[title = {}]
            ....
      \end{tcolorbox}
    \end{column}

    \begin{column}{0.3\textwidth}
      \begin{tcolorbox}[title = {}]
            ....
      \end{tcolorbox}
    \end{column}
  \end{columns}
```


## 学习资源
[Beamer](https://cn.sharelatex.com/learn/Beamer)
[tcolorbox](https://liam0205.me/2016/07/22/using-the-tcolorbox-package-to-create-a-new-theorem-environment/)
[盒子](https://liam0205.me/2018/05/21/TeX-by-Topic-boxes/)
