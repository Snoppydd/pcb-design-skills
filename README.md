# PCB 布局布线技能

用于 Codex 的 `pcb-layout-design` 技能：从已完成的原理图和封装出发，执行 PCB 布局、走线、铺铜、评审与交付检查。支持通过嘉立创 EDA 专业版客户端命令行工作，默认禁止自动走线和自动寻路器。

## 安装

在 GitHub 打开本仓库内的 `pcb-layout-design` 文件夹，复制浏览器地址，向 Codex 发送：

```text
请使用 skill-installer 安装这个技能：【粘贴 pcb-layout-design 文件夹的 GitHub 地址】
```

链接一般形如 `https://github.com/用户名/pcb-design-skills/tree/main/pcb-layout-design`，也可以使用对应版本标签的目录链接。安装目标若已有同名技能，先让 Codex 比较并备份本地改动，再明确要求更新。

## 使用

使用者需自行安装嘉立创 EDA 专业版、准备可用的 `lceda-pro`，并打开客户端。技能安装不会安装 EDA 软件，也不会附带器件库或原理图。

1. 准备原理图工程及关联封装。
2. 将技能中的 [PCB需求.md](pcb-layout-design/assets/PCB需求.md) 复制到工程根目录，填写已知要求。也可以让 Codex 帮你复制，不覆盖已有文件。
3. 发送：

```text
使用 pcb-layout-design，按本工程的 PCB需求.md，通过嘉立创客户端命令行完成 PCB。禁止自动走线，交付原生工程、顶底层预览和验证结果。工程路径：【填写路径】。
```

关键输入不足时先查工程再询问；普通可逆选择连续推进。设计过程包含电源供回路径、去耦、散热、装配、通道、参考铜及原生规则检查。零 DRC 不代表整机性能已验证，最终设计仍需硬件工程师审核及适用样机测试。

## 内容

- `pcb-layout-design/SKILL.md`：任务范围、工作流程与专题导航。
- `pcb-layout-design/references/`：布局、走线、电源、接口、制造、评审及工程案例。
- `pcb-layout-design/assets/PCB需求.md`：简版项目输入模板。

案例中的尺寸与统计只用于学习，不是新项目的默认参数。外部资料的权利归原作者；本仓库未统一授予第三方内容的再许可。
