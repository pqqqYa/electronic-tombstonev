# 源文件

## 1. 导言区

### 1.1 定义文章类型

### 1.2 定义标题、作者以及日期

### 1.3 调用一些需要的宏包

* 使用`\usepackage`加载宏包

1. **必备**
	* amsmath
	* graphicx
	* hyperref
2. 样式
	* caption
	* enumitem
	* fancyhdr
	* footmisc
	* geometry
	* titlesec
3. 数学
	* bm
	* mathtools
	* physics
	* unicode-math
4. 表格
	* array
	* booktabs
	* longtable
	* tabularx
5. 插图、绘图
	* float
	* pdfpages
	* standalone
	* subfig
	* pgf/tikz
	* pgfplots
6. 字体
	* newpX
	* pifont
	* fontspec
7. 各种功能
	* algorithm2e
	* beamer
	* biblatex
	* listings
	* mhchem
	* microtype
	* minted
	* natbib
	* siunitx
	* xcolor
8. 多语言
	* babel
	* polyglossia
	* ctex
	* xeCJK


## 2. 正文区

## 2.1 LaTex的基本语法

章节结构

* `\chapter`章
* `\section`节
* `\subsection`小节
* `\paragraph`带题头段落

文本格式

* `\centering`居中对齐
* `\emph`强调
* `\verb`原样输出
* `\url`超链接
* `\footnote`脚注

列表与应用

* `\item`列表条目
* `\caption`标题
* `\includegraphics`插入图片
* `\label`标号
* `\cite`引用参考文献
* `\ref`引用图表公式等

常用环境

* table表格
* figure图片
* equation公式
* itemize无编号列表
* enumerate编号列表
* description描述


## 2.2 分页

1. `\newpage` 插入一个新页。
2. `\null\thispagestyle{empty}` 创建一个空页，但不显示页码。
3. 再次使用 `\newpage` 插入另一个新页，确保目录从新的一页开始。