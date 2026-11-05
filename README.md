# 拉马努金数学公式 · Ramanujan Formulas

拉马努金（Srinivasa Ramanujan, 1887–1920）全部已知公式的整理仓库：以三本早期笔记、失落笔记与正式发表论文为三大来源，按主题模块组织。

> **内容口径，请先读这段**：本仓库目前是**目录、导读与代表公式骨架**，不是 3,254 条公式的全文收录。逐条全文收录须对照 Berndt 五卷与 Andrews–Berndt 五卷逐条整理，且现代整理本的正文与证明受版权保护，本仓库只收录公式陈述与自写导读，不照抄整理本。每个模块文件末尾都标了「待补充」的具体内容。

## 数字总览

| 项目 | 数量 | 来源 |
|---|---|---|
| 三本早期笔记的结果条目 | 约 3,254 条 | Bruce C. Berndt 整理统计；Berndt 在 Springer 五卷本《Ramanujan's Notebooks》Parts I–V（1985–1998）中为全部 3,254 条给出证明或引出文献证明 |
| 失落笔记中的公式 | 600+ 条（约 650 条） | 约 138 面手稿，1919–1920 年最后一年所写；1976 年由 George E. Andrews 在剑桥三一学院 Wren 图书馆 Watson 遗物中发现 |
| 正式发表论文 | 37 篇 | 生前发表于专业期刊的论文，收录于《Collected Papers of Srinivasa Ramanujan》（剑桥大学出版社 1927 年初版，AMS Chelsea 再版，ISBN 978-0-8218-2076-6）；另有向《Journal of the Indian Mathematical Society》提交的 58 个问题 |
| 失落笔记的学术整理成果 | 5 卷 | George E. Andrews 与 Bruce C. Berndt《Ramanujan's Lost Notebook》Parts I–V（Springer，2005、2009、2012、2013、2018） |

补充说明：

- 3,254 条中有相当一部分（Berndt 指出约半数）可能是对已有结果的重新发现；拉马努金只记结果、不记证明，据 Berndt 的解释，这与当时印度学生用石板演算、纸张昂贵有关。
- 失落笔记不是一本装订好的书，而是散页；Rankin（1989）概述其内容：多数关于 q-级数与 mock theta 函数，约三分之一关于模方程与奇异模，其余主要是积分、Dirichlet 级数、同余与渐近分析。
- 全集另有说法「一生独立得出近 3,900 个结果」，那是把笔记、失落笔记与论文合在一起的约数；本仓库各处数字以分来源的统计为准，不混用。

## 仓库结构

```
ramanujan-formulas/
├── README.md                  # 本文件：总览与数字
├── notebooks.md               # 三本早期笔记：3,254 条的来源与整理史
├── lost-notebook.md           # 失落笔记：138 面、600+ 公式、五卷整理
├── papers.md                  # 37 篇正式发表论文目录
├── modules/
│   ├── M07-q-series.md        # q-级数：q-级数恒等式
│   ├── M08-mock-theta.md     # Mock Theta Functions：模拟 theta 函数
│   ├── M09-integrals.md      # 积分：定积分、特殊积分
│   ├── M10-gamma.md          # Gamma 函数：阶乘推广、特殊函数
│   ├── M11-elliptic.md       # 椭圆函数：椭圆积分、椭圆模数
│   ├── M12-asymptotics.md    # 渐近分析：近似公式、渐近展开
│   ├── M13-combinatorics.md  # 组合数学：组合恒等式
│   └── M14-algebraic-equations.md  # 代数方程：丢番图方程、代数关系
├── data/
│   └── modules.json           # 模块目录（机器可读）
└── index.html                 # 静态导览页（GitHub Pages）
```

## 模块一览（M07–M14）

| 模块 | 主题 | 内容 |
|---|---|---|
| M07 | q-级数 | q-级数恒等式 |
| M08 | Mock Theta Functions | 模拟 theta 函数 |
| M09 | 积分 | 定积分、特殊积分 |
| M10 | Gamma 函数 | 阶乘推广、特殊函数 |
| M11 | 椭圆函数 | 椭圆积分、椭圆模数 |
| M12 | 渐近分析 | 近似公式、渐近展开 |
| M13 | 组合数学 | 组合恒等式 |
| M14 | 代数方程 | 丢番图方程、代数关系 |

注：编号 M07–M14 为本仓库的模块编号；M01–M06 不在本批范围内，如后续补齐再按同一体例加入。

## 相关仓库

- 《数学全景图》：[curzydj8/mathematics-panorama](https://github.com/curzydj8/mathematics-panorama)（在线阅读：https://curzydj8.github.io/mathematics-panorama/），其中拉马努金卷（r1 生平、r2 笔记、r3 失落笔记、r4 π 公式）是本仓库的入门导读。

## 主要参考文献

- Bruce C. Berndt, *Ramanujan's Notebooks*, Parts I–V, Springer, 1985–1998.
- George E. Andrews & Bruce C. Berndt, *Ramanujan's Lost Notebook*, Parts I–V, Springer, 2005–2018.
- Srinivasa Ramanujan, *Collected Papers of Srinivasa Ramanujan*, eds. G. H. Hardy, P. V. Seshu Aiyar, B. M. Wilson, Cambridge University Press, 1927；AMS Chelsea 再版 2000，ISBN 978-0-8218-2076-6.
- G. H. Hardy, *Ramanujan: Twelve Lectures on Subjects Suggested by His Life and Work*, Cambridge University Press, 1940.
- Robert Kanigel, *The Man Who Knew Infinity*, 1991（传记，非数学文献）。

## 贡献方式

按模块认领：每条公式注明出处（笔记卷 / 失落笔记 / 论文编号）、给出陈述、附自写证明思路或文献指引，不直接复制整理本的证明原文。先开 issue 说明要补的模块与条目范围，再提交。
