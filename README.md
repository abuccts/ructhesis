RUCTHESIS
=========

RucThesis is a LaTeX thesis template package for Renmin University of China supporting from bachelor, master to doctor dissertations. Since the users of this package are supposed to be Chinese or those understand Chinese, the following of this file and all other documents are written in Chinese only. This project is forked from [ThuThesis](https://github.com/xueruini/thuthesis).


RucThesis 是什么？
-----------------

RucThesis 为 <b>R</b>enmin <b>U</b>niversity of <b>C</b>hina <b>Thesis</b> LaTeX Template 之缩写。

此宏包修改自 [ThuThesis](https://github.com/xueruini/thuthesis)，旨在建立一个简单易用的中国人民大学学位论文 LaTeX 模板，包括本科毕业论文、硕士论文以及博士论文。目前支持本科毕业论文，对其它论文的支持会陆续加入。


文档
----

请[下载](https://github.com/abuccts/ructhesis/releases)发行版，里面包括具体使用说明以及示例文档：

* 模板使用说明 (ructhesis.pdf)
* 示例文档 (main.pdf)


下载
----

* 发行版：[Release](https://github.com/abuccts/ructhesis/releases)
* 开发版：[GitHub](https://github.com/abuccts/ructhesis)

升级
----

* `git pull`
* 下载最新的 [release](https://github.com/abuccts/ructhesis/releases) 版本，将 `ructhesis.ins`，`ructhesis.dtx` 和 `ructhesis.bst` 拷贝至工作目录覆盖相应的文件，然后运行 `latex ructhesis.ins`，生成新的类文件 `ructhesis.cls` 和配置文件 `ructhesis.cfg` 即可。


提问
----

* [Github Issues](http://github.com/abuccts/ructhesis/issues)


Makefile 的用法
---------------

``` sh
make [{all|thesis|doc|count|clean|cleanall|distclean}] \
     [METHOD={latexmk|xelatex|pdflatex}]
```

### 目标

| 命令             | 说明                                         |
| ---------------- | -------------------------------------------- |
| `make all`       | 等于 `make thesis && make shuji && make doc` |
| `make cls`       | 生成模板文件                                 |
| `make thesis`    | 生成论文 main.pdf                            |
| `make doc`       | 生成使用说明书 ructhesis.pdf                 |
| `make count`     | 计算论文 main.pdf 字数                       |
| `make clean`     | 删除示例文件的中间文件（不含 main.pdf）      |
| `make cleanall`  | 删除示例文件的中间文件和 main.pdf            |
| `make distclean` | 删除示例文件和模板的所有中间文件和 PDF       |

### 参数


**METHOD**：指定生成 pdf 的方式，缺省采用 latexmk。

| METHOD   | 说明                                        |
| -------- | ------------------------------------------- |
| latexmk  | 使用 latexmk 的方式生成 pdf（使用 xelatex） |
| xelatex  | 使用 xelatex 引擎编译生成 pdf               |
| pdflatex | 使用 pdflatex 引擎编译生成 pdf              |


开源许可证
----------

* 本项目 fork 自 (ThuThesis)[https://github.com/xueruini/thuthesis/tree/4deba6c6bf2adda781c10018eae6162e57c4b4dc]，遵守原项目的相关开源许可；
* 中国人民大学中英文标志 `figures/ruc-*` 的版权归中国人民大学教务处所有；
* (texcount.pl)[texcount.pl] 的版权归原作者所有，采用 (The LaTeX Project Public License)[https://www.latex-project.org/lppl.txt] 发布；
* 其余部分使用 (LaTeX Project Public License v1.3)[LICENSE] (LPPL) 授权。