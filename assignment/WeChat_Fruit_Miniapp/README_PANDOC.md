# 使用 pandoc 将 pan.md 转为 pan.docx（说明）

步骤（在你的本地电脑执行）：

1. 安装 pandoc：
   - 官方下载页：https://pandoc.org/installing.html
   - 或使用包管理器（Windows: choco, macOS: brew, Linux: apt/yum）

2. 克隆或下载本仓库到本地，并切换到文件夹 assignment/WeChat_Fruit_Miniapp/：
   git clone https://github.com/Ex-Machinery/uuu.git
   cd uuu/assignment/WeChat_Fruit_Miniapp

3. 如果你希望把占位图直接嵌入到 Word，请把你的 PNG 图像命名为 fig1.png、fig2.png、fig3.png、fig4.png 放在同一目录下，或者修改 pan.md 中的占位为 Markdown 图片语法：

   ![图1 用例图](fig1.png)

   pandoc 会把这些本地图片嵌入到生成的 docx 文件中。

4. 生成 Word 的基本命令：

   pandoc pan.md -o pan.docx --resource-path=. 

   这会把 pan.md（以及当前目录下的图片）转换为 pan.docx。若你想使用自定义 Word 样式模板（reference docx），可以用：

   pandoc pan.md -o pan.docx --resource-path=. --reference-doc=reference.docx

   其中 reference.docx 是你准备的 Word 模板文件（样式、字体、段落样式等）。

5. 打开生成的 pan.docx：
   - 直接用 Microsoft Word 或 LibreOffice 打开并检查图片位置与排版。
   - 如需调整图片大小或位置，可在 Word 中修改。

6. 如果你不希望使用 pandoc，也可以直接在 Word 中新建文档，把 pan.md 的文本复制进去，然后手动插入图片并保存为 pan.docx。

---

请在仓库查看并按需替换占位图文件（fig1.png~fig4.png）。如果你需要，我也可以把当前的 mermaid 源渲染成真实的 PNG 并上传替换（但你已经选择自己处理图表）。
