# 我的书架
Windows 本地 PDF 管理与 DeepSeek 阅读问答工具。

## 使用
下载 my-bookshelf-windows-x64.zip，完整解压后运行「我的书架.exe」。首次启动为个人空书架。
支持批量添加 PDF、全文页码检索、分类与阅读笔记、移除恢复、文件重新定位、整书问答、按书聊天记录和连续追问。
DeepSeek 需要使用者自己的 API Key。可通过 Windows 当前用户加密保存。请求会发送所选范围内的原文和问题。
扫描型 PDF 需要先进行 OCR。PDF 原文件保持在使用者选择的路径。

## 数据
应用数据位于 %LOCALAPPDATA%\LocalPdfShelf\v1。仓库和分享包不包含作者的 PDF、私人索引、笔记、聊天历史或密钥。

## 源码与构建
Shelf.cs 为 C# WinForms 界面，ReadingQuestion.cs 处理 AI 问答，build.py 用 pypdfium2 提取 PDF 正文。
目录已按构建要求组织，build.py 位于根目录，界面源码和打包脚本位于 desktop 子目录。
使用 Windows x64、.NET Framework 4.x C# 编译器和包含 pypdfium2 的完整 Python 3.12 环境。
运行 python desktop/package.py --share my-bookshelf-windows-x64.zip。
在线回答效果依赖 DeepSeek；离线核心功能和模拟 API 调用已在开发机测试。

