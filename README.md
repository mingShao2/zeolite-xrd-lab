# Zeolite XRD Lab

一个完全在浏览器端运行的分子筛粉末 XRD 结构筛查工具。支持上传 TXT、XY、XYE、CSV、DAT 数据，进行整谱相似度、特征峰覆盖、杂峰提示和候选框架排序，并显示配套 CIF 骨架示意。

## 在线使用

[打开 GitHub Pages 公共网站](https://mingshao2.github.io/zeolite-xrd-lab/)。实验谱不会上传到服务器，解析和匹配都在访问者浏览器中完成。

## 本地运行

```bash
npm install
npm run dev
```

## 构建 GitHub Pages

```bash
npm run build:github
```

静态站点输出到 `docs/`。如需通过 GitHub 网页上传发布，可继续运行：

```bash
python scripts/build-github-singlefile.py
```

脚本会把参考谱、CIF、样例、样式和程序封装成 `github-upload/index.html`。本仓库当前使用 `main` 分支根目录发布，完整可编辑源码另附于 `zeolite-xrd-lab-source.zip`。

## 科学解释边界

匹配评分用于候选结构排序，不是概率、相含量或自动确认。XRD 不能单独证明 Si/Al、杂原子进入骨架、酸性或孔道性能；相对结晶度需要组成、状态和测量条件匹配的实体标准样。
