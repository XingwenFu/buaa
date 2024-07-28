# 北京航空航天大学硕博学位论文LaTeX模板3.2.1

本项目为北京航空航天大学学位硕士博士论文模板BUAAThesis，包含Word模板和LaTeX模板。模板按照《研究生手册》制定，适用于博士、硕士学位论文（中文）。

#版本修改
相比于3.2版本，3.2.1版本解决了之前英文无法加粗的问题、博士论文中页眉为硕士学位论文的问题，以及之前论文题目为25字时，标题页排版错误的问题。
在3.2.1版本中，在取得的学位成果板块，加入了书写的样例。

3.2.2相比于3.2.1版本，该3.2.2版本解决了部分学院名称对不上的问题，本版本按照北航官网的学院名称进行了对应。
3.2.3相比于3.2.2版本，该3.2.3版本重新调整了公式和上下文之间的页间距，使其不会出现过大的问题，同时标注了参考文献不显示的操作方法，具体可看写作提示部分。
3.2.4相比于3.2.3版本，调整了4级，5级和6级标题前后的间距,修改了副教授的标识，由Prof.修改为A.P., 第一页栏的培养院系修改为培养学院。首页中图分类号和论文编号已经根据格式要求加粗，作者姓名、专业名称、指导教师、培养学院等改为了4号黑体字。
## 项目结构
```
- BUAAThesis
|-- def
|   |-- GBT7714-2015.bst      // 国标参考文献BibTeX样式文件
|   |-- GBT7714-2015-NoWarning.bst // 国标参考文献BibTeX样式文件,取消了对于关键信息缺失的警示消息
|   |-- buaa.cls                  // LaTeX宏模板文件
|   |-- simsun.ttc                // 宋体字
|   |-- head-doctor.eps       // 论文封皮学术博士学位论文标题
|   |-- head-prodoctor.eps    // 论文封皮专业博士学位论文标题
|   |-- head-master.eps       // 论文封皮学术硕士学位论文标题
|   |-- head-professional.eps // 论文封皮专业硕士学位论文标题
|   |-- logo-buaa.eps         // 论文封皮北航字样
|-- pic
|   |-- logo-buaa.eps         // 论文封皮北航字样
|   |-- question_survey.jpg   // 论文出现问题后可参与的问卷二维码
|-- tex/*.tex                 // LaTeX模板样例中的独立章节
|-- main.tex              // LaTeX模板
|-- README.md                 // 本文件
|-- ref.bib                   // LaTeX模板中的参考文献Bib文件
```

## 模板使用
1. 参考下方 `环境配置` 部分配置 `LaTeX` 写作环境
2. 参考下方 `写作提示` 部分撰写论文

## 环境配置

常见的 `LaTeX` 写作环境有两种，一种是使用 Overleaf 的在线环境，另一种是使用 `TexLive` 的本地环境。两种写作环境各有优劣：
- 在线环境基本无需配置，本地环境需要较复杂的配置
- 在线环境的免费账户有着**严苛**的编译时长限制，类似毕业论文这样的长篇文章**基本不可能**通过编译，需要开通订阅才能解锁编译时长限制

### 1. Overleaf 环境

将项目压缩包上传至 [Overleaf](https://cn.overleaf.com/) 后，修改编译选项为 `XeLaTeX` 即可开始写作。


### 2. 本地编译环境

编译环境请选择 'TexLive' + ‘Texstdio' 方案

#### 2.1 TexLive安装

- MacOS用户点击 [MacTeX](https://mirror.ctan.org/systems/mac/mactex/MacTeX.pkg) 下载并安装 `MacTex` 即可（这是一个包含了`TexLive` 环境的程序）
- Windows 和 Linux 用户需要参考以下步骤安装 `TexLive+TexStdio`

1. 前往 [TexLive Images - 清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/) 下载 `texlive.iso` 安装包
2. 装载 `texlive.iso` 后，Windows 用户点击 `install-tl-windows.exe` 启动安装程序，Linux 用户请使用`sudo install-pl`启动安装
3. 修改安装路径（否则默认安装在系统盘，会占据巨大的系统空间！）
4. 点击 `安装`，等待漫长的安装过程（可能会持续几十分钟）
5. 安装结束后，使用终端输入 `tex`，出现下方结果即表示安装成功

具体详细的安装步骤可前往 https://blog.csdn.net/qq_43431934/article/details/124079142
注意！！！！
在安装之后，需要在计算机的环境变量Path中加入bin的路径。

## 写作提示

-  参看示例模板 `Template.tex` 及其中插入的各章节 `tex/*.tex` 熟悉模板结构和 $LaTeX$ 语法，撰写论文正文。
-  在写公式时，请不要在公式之后加入额外的空行，避免空行所导致的公式与下一行距离过大的问题。
-  在编译时，请使用xelatex进行编译，否则会出现页码不是五号宋体的问题。
-  在写参考文献时，可以先选用GBT7714-2015.bst来查看缺少哪些关键内容，进行补全，如果存在某些内容找不到的问题，则可以使用GBT7714-2015-NoWarning.bst来不表示这些缺乏信息。
-  在写表时，如果存在上下两个线加粗的需求，可以使用\toprule[], \midrule[] 和 \bottomrule[] 来加粗三线表的三条线。
-  在写论文时，可根据tex文件里的注释信息来修改本文的密级，专硕学硕等内容。
-  在编译时，可能会出现参考文献无法出现的现象，此时，可以先运行texstudio界面上方工具栏的参考文献，然后进行重新的构建和编译，即可出现参考文献内容。
-  在编译时，有可能会出现两行间距过小的情况，这是由于本页的图的大小导致的，当遇到这种情况时，可在间距较小的第二行之前加入\newpage使其进入下一页，可解决这个问题。

## 学院名称对应
材料科学与工程学院                          School of Materials Science and Engineering
电子信息工程学院                            School of Electronic and Information Engineering
自动化科学与电气工程学院                    School of Automation Science and Electronic Engineering
能源与动力工程学院                          School of Energy and Power Engineering
航空科学与工程学院                          School of Aeronautic Science and Engineering
计算机学院                                  School of Computer Science and Engineering
机械工程及自动化学院                        School of Mechanical Engineering and Automation
经济管理学院                                School of Economics and Management
数学科学学院                                School of Mathematics Sciences
生物与医学工程学院                          School of Biological Science and Medical Engineering
人文社会科学学院                            School of Biological Science and Medical Engineering
公共管理学院                                School of Public Administration
人文社会科学学院（公共管理学院）            School of Humanities and Social Sciences (School of Public Administration)
外国语学院                                  School of Foreign Languages
交通科学与工程学院                          School of Transportation Science and Engineering
可靠性与系统工程学院						School of Reliability and Systems Engineerin
宇航学院                                    School of Astronautics
飞行学院                                    School of Astronautics
仪器科学与光电工程学院                      School of Instrumentation Science and Optoelectronics Engineering
物理学院									School of Physics
法学院             							School of Law
软件学院									School of Software
继续教育学院								College of Continuing Education
沈元学院									ShenYuan Honors College
高等理工学院                                ShenYuan Honors College
未来空天技术学院							School of Future Aerospace Technology
国家卓越工程师学院							National Superior College for Engineers
中法工程师学院								Sino-French Engineer School
国际通用工程学院							School of General Engineering
国际学院									International School
新媒体艺术与设计学院						School of New Media Art and Design
化学学院									School of Chemistry
马克思主义学院								School of Marxism
人文与社会科学高等研究院					Institue for Advanced Studies in Humanities and Social Science
空间与环境学院								School of Space and Environment
无人系统研究院								Institute of Unmanned System
航空发动机研究院							Research Institute of Aero-Engine
体育部										Department of Sports
国际交叉科学研究院							International Research Institue for Multidisciplinary Science
北航学院									Beihang School
医工科学与工程学院							School of Medical Science and Engineering
医工交叉创新研究院							School of Medical Science and Engineering
网络空间安全学院							School of Cyber Science and Technology
集成电路科学于工程学院						School of Integrated Circuit Science and Engineering
人工智能研究院								Institue of Artificial Intelligence
前沿科学技术创新研究院						Research Institute for Frontier Science
北京学院									School of Beijing
中法航空学院								Sino-French Aviation Institute



## 更多建议

-  使用 Git 进行版本管理
