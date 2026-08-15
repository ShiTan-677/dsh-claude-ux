# 截图占位说明

把截图放到本目录，**文件名必须与下表一致**（README 中的引用路径）。

| 文件名 | 截图内容 | 拍摄要点 |
|---|---|---|
| `settings-page.png` | 「Claude 风控」标签页全貌 | 打开设置 → 左侧栏点「Claude 风控」，整页截图：右上总开关、检测状态卡、区域风控面板、自主性面板、文案面板 |
| `settings-sidebar.png` | 设置页左侧标签栏 | 显示左侧标签列表，「Claude 风控」标签可见（与「视觉工具」等插件标签并列），窄图即可 |
| `status-card.png` | 检测状态卡特写 | 放大「检测状态」面板：风控目标 / 主机判定 / 命中 / 信号分 / 公网 IP / 命中信号明细 / 本机浏览器信号 |
| `refusal-chat.png` | 对话中的区域拒绝回复 | 启用插件且目标命中时发一条消息，截取对话：用户消息 + 拒绝文案（含「第 N/M 次尝试——继续将结束本次对话」） |
| `chat-ended.png` | Chat ended 面板 | 触发会话结束（区域拒绝达到 `refusalEndsAfter` 次数，或辱骂达到 `endThreshold`）后，截取输入区：Chat ended / 原因说明 / Start a new chat 按钮 |
| `classify-panel.png` | 分类 LLM 面板 + 自测 | 「Claude 风控」标签里的「分类 LLM」面板：判定模式下拉、分类模型下拉（展开状态，能看到 DSH 已配置模型列表）、超时；下方「消息分类自测」输入一句话并点测试，显示词表/LLM/最终判定与使用的模型 |

## 拍摄提示

- 截 `settings-page.png` / `status-card.png` 前：建议把「区域策略」设为 block、总开关打开（截完记得关回）；**把 `ipCheck` 保持关闭**，避免公网 IP 出现在公开截图里。
- 截 `refusal-chat.png`：总开关打开 + 目标命中（本机时区/语言通常已命中），发任意一条消息即可看到拒绝文案。
- 截 `chat-ended.png`：可临时把「区域拒绝后结束（次数）」调成 1，发一条消息即触发；截完调回。
- 格式 PNG，宽度建议 ≥ 800px；截全页可用浏览器自带的全页截图（如 Edge/Chrome 的 Capture full page）。
