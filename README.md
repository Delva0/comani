# Comani

Comani 是面向 ACGN 生产问题的高层 Python 工具包，范围覆盖动画、漫画、游戏、轻小说等领域。项目从真实行业痛点和未解问题出发，通过调研和具体实践逐步形成可复用能力。

目前版本为 `0.1.0.dev0`，仅建立工程起点，尚无稳定的领域 API。具体能力与架构将随问题调研和实现逐步确定。

## 与 Comfier 的关系

| 项目 | 职责 |
| --- | --- |
| [Comfier](https://github.com/Delva0/comfier) | 低层执行库：连接远端 ComfyUI，组合节点与 Python 代码，管理远端 Python 对象及计算结果。 |
| Comani | 高层工具包：围绕 ACGN 领域问题组织能力，并在需要远端执行时使用 Comfier。 |

两者是独立的 Python 包，可以安装在同一个环境中。当前 Comani 尚无调用 Comfier 的功能，因此暂未声明运行依赖。

## 本地开发

需要 Python 3.11 或更新版本。在本仓库中安装：

```sh
python -m venv .venv
. .venv/bin/activate
python -m pip install -e .
```

安装后可导入 `comani`。若同时开发远端执行层，可将两个仓库放在同级目录，再运行 `python -m pip install -e ../comfier`；Comfier 的部署和调用方式见其 [README](https://github.com/Delva0/comfier#readme)。
