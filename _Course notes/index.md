---
layout: page # 这个布局应该指向你 _layouts 文件夹中用于普通页面的布局文件，比如 page.html 或 default.html
title: "我的书籍与代码精选" # 这个标题会显示在你的网站页面上，作为“书籍与代码”模块的名称
permalink: /Books&codes/ # 核心：这个设置将让该文件成为你网站上 /Books&codes/ 路径的入口页面
---

## 欢迎来到我的书籍与代码页面

这里汇总了我的学习笔记、代码示例和相关资源，按主题分类整理。点击下面的链接，探索更多内容！

### 电子工程

* [**模电学习笔记**](/Books&codes/Analog-Electronics/)
    * **概述：** 这部分包含了我在模拟电路设计与分析方面的学习资料。
* [**数电实验代码**](/Books&codes/Digital-Electronics/)
    * **概述：** 这里分享了数字电路实验中的代码实现和项目记录。
* ### 编程语言与算法

* [**Python 基础与应用**](/Books&codes/Python-Basics/)
    * **概述：** 从基础语法到实际项目，Python 学习的整理。
* [**C++ 高级编程**](/Books&codes/Cpp-Advanced/)
    * **概述：** 深入探讨 C++ 的高级特性和实践。
* ---


### 代码解释和下一步操作：

1.  **`layout: page`**:
    * 确保你的 `_layouts` 文件夹中有一个 `page.html` 或者 `default.html` 文件。Jekyll 会使用这个布局来包裹你的 Markdown 内容，生成最终的 HTML 页面。
2.  **`title: "我的书籍与代码精选"`**:
    * 这是这个目录页面的标题，会显示在浏览器标签页和页面内容本身。
3.  **`permalink: /Books&codes/`**:
    * **这是最核心的部分。** 它告诉 Jekyll，当用户访问 `https://hugswangyu.github.io/Books&codes/` 这个 URL 时，就应该显示 `index.md` 的内容。这样就解决了之前 `Page Not Found` 的问题。
4.  **内部链接 (`[模电学习笔记](/Books&codes/Analog-Electronics/)`)**:
    * 这些链接是你目录页面的“按钮”。当用户点击“模电学习笔记”时，他们会被导航到 `https://hugswangyu.github.io/Books&codes/Analog-Electronics/` 这个 URL。
    * **重要：** 你现在需要为这些链接**创建对应的 `.md` 文件**。

### 下一步关键操作：创建子分类的具体内容文件

为了让 `[模电学习笔记](/Books&codes/Analog-Electronics/)` 这样的链接能够正常工作，你需要：

1.  **在 `_Books&codes` 文件夹内，创建对应的 Markdown 文件。**
    * 例如，创建一个名为 `Analog-Electronics.md` 的文件。
    * 创建一个名为 `Digital-Electronics.md` 的文件。
    * 等等，对应你在 `index.md` 中列出的所有子分类链接。

2.  **编辑这些子分类文件的内容和前置元数据。**
    以 `_Books&codes/Analog-Electronics.md` 为例：
    ```markdown
    ---
    layout: page # 同样，指向合适的布局文件
    title: "模电学习笔记" # 这个标题会显示在模电页面的顶部
    permalink: /Books&codes/Analog-Electronics/ # 核心：必须和 index.md 中链接的 URL 完全匹配！
    ---

    ## 模电学习笔记：我的探索之路

    欢迎来到模电的学习空间。这里你可以找到我关于以下主题的笔记：

    ### 运算放大器
    * [运算放大器基础原理及应用](/Books&codes/Analog-Electronics/Op-Amp-Basics/)
    * [用运放设计滤波器](/Books&codes/Analog-Electronics/Filter-Design/)

    ### 功率电子
    * [开关电源设计](power-supply-design.md)

    ```
    * **`permalink`**: 确保这个 `permalink` 的值，**与你在 `_Books&codes/index.md` 中为“模电学习笔记”设置的链接 `/Books&codes/Analog-Electronics/` 完全一致**。
    * 你可以继续在 `Analog-Electronics.md` 内部添加更细分的链接（如 `Op-Amp-Basics.md`），这同样需要你在 `_Books&codes/Analog-Electronics/` 下创建这些文件，并给它们设置对应的 `permalink`。

### 最后：提交并推送更改

1.  在你完成 `index.md` 和所有子分类的 `.md` 文件的创建和编辑后，保存所有文件。
2.  在终端中，进入你的项目根目录 (`hugswangyu.github.io`)。
3.  执行 Git 命令来提交和推送这些更改：
    ```bash
    git add .
    git commit -m "Add Books&codes index page and sub-category content"
    git push origin master # 再次确认你的主分支名是 master
    ```

完成这些步骤后，GitHub Pages 会重新构建你的网站。稍等几分钟，然后清除浏览器缓存并访问你的网站。点击导航栏的 "Books&codes"，你应该能看到 `index.md` 的内容和分类链接，再点击分类链接，就能跳转到对应的具体学习笔记页面了。
