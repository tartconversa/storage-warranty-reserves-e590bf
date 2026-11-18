# 储能质保的迟报风险与资金准备分析

现有内容是合成业务资料及通用资料检查器，尚无业务分析或决策能力。字段、单位和业务记录的含义见 docs/资料口径.md，完整性目录为 data/catalog.json。不得把文件自检成功解释成业务结论成立。

## 环境

Python 3.11.2；分析依赖已在 requirements.txt 固定版本。

    python3 -m pip install -r requirements.txt
    python3 -m sourcepack

检查入口读取资料目录，核对文件摘要、字段类型、记录键、引用与行数，不进行估计、推荐、批准或结算。新增业务资料可使用相同字段契约，目录摘要只对应当前保存的输入文件。

## 已有检查与语法构建

    python3 -m unittest discover -s tests -v
    python3 -m compileall -q sourcepack tests

现有测试只覆盖资料容器和输入诊断。产品入口、业务状态、结果解释及业务测试尚待开发；开发完成后需补充实际使用方式。运行资料检查不需要访问外部业务系统。
