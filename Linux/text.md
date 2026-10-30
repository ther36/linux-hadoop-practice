# 问题：使用 grep 搜索文件时提示“没有那个文件或目录”

- **环境**：CentOS 7 / FinalShell
- **现象**：文件明明就在当前目录下，执行 `grep "to" /yao1/yao1.txt` 却报错找不到文件。
- **解决过程**：去掉最前面的斜杠，改为相对路径 `grep "to" yao1/yao1.txt`，成功搜出结果。
- **根因**：在 Linux 中，以 `/` 开头代表从系统的“根目录”开始找（绝对路径）；而文件实际在当前用户目录下，不加 `/` 代表从当前位置找（相对路径）。
- **一句话总结**：写路径前先确认自己在哪（用 `pwd`），不要无脑加 `/`。
- <img width="1393" height="749" alt="fc16e5b6565e169b041485957e35c261" src="https://github.com/user-attachments/assets/c196fff4-e07f-4c5b-91d6-1a486ee761ce" />
