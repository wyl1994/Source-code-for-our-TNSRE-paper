# 项目整理说明

本目录已按“源码 / 数据 / 结果 / 文档 / 图像素材”重新整理，避免代码、数据和论文文件继续混在一起。

## 目录结构

- `src/main_pipeline/`：主分析流程脚本。
- `src/extended_analysis/`：扩展分析与降维实验脚本。
- `data/main_pipeline/`：主流程输入数据。
- `data/extended_analysis/`：扩展分析输入数据。
- `results/main_pipeline/`：主流程产生的结果表和图。
- `results/extended_analysis/`：扩展分析产生的结果表和图。
- `docs/manuscript/`：TNSRE 论文 LaTeX 稿件与插图。
- `docs/references/`：参考文献 PDF。
- `docs/submission/`：投稿校样等文件。
- `docs/slides/`：PPT 文件。
- `figures/workflow/`：流程图和补充示意图素材。

## 已完成的整理

- 给保留的 Python 脚本在文件最前面补了中文说明注释。
- 将脚本中的主要输入输出路径改为指向当前整理后的 `data/` 和 `results/` 目录。
- 删除了明显无效或冗余的文件：
  - 自动保存的 PPT/EMF 文件
  - `Thumbs.db`
  - 解压后无必要保留的 `tnsre.zip`
  - 明显无效的 `plott.py`
  - 旧版脚本 `Leave-one-out_old.py`
  - 训练缓存目录 `catboost_info`

## 说明

- `src/main_pipeline/xxx.py` 虽然文件名很差，但代码本身不是空文件；目前保留为“实验性主流程脚本”。如果后续确认不用，建议直接删除或改成有意义的文件名。
- `results/` 下保留了少量带 `root_copy` 或拼写不规范的历史结果文件，因为它们内容并不完全一致，直接删除风险高。它们不是好资产，只是暂时保留的旧结果。
- 论文目录下的 `martix.png` 与 `matrix.png` 不是同一个文件，因此没有擅自删除。

## 建议运行方式

在项目根目录执行脚本，例如：

```bash
python src/main_pipeline/Leave-one-out.py
python src/extended_analysis/Five-fold_Prediction_PCA.py
```

## TE实验
增加的TE相关实验直接在相应原实验代码修改输入输出文件实现，rst是返修实验保存的结果，除了修改输入输出硬编码的文件名便于实验，没有对原实验代码和数据做任何修改。
