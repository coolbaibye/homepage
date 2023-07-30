---
author: "Bye"
title: "有用的工具列表"
date: "2023-01-23"
description: ""
tags: ["资源"]
ShowToc: false
ShowBreadCrumbs: true
---
### 数据库
* 兼容MySQL的**免费**的云数据库 
	* PlanetScale：免费账号有5G的容量
	* Prisma：配合JavaSript特别方便
	* PingCap的TiDB

### 图像
* [rembg](https://github.com/danielgatis/rembg) 用Python给**图片移除背景** 
	* 有命令行工具
* [reccap.it](https://reccap.it/)：**把Youtube视频转换为自动生成key points图文**，方便浏览检索和分享  
* [table-reader](https://www.table-reader.com/image-to-excel)：OCR图片表格 => CSV/Excel 表格 
* [Upscayl](https://www.upscayl.org/)：图像放大工具 
* [carbon](https://carbon.now.sh/)：代码截图 
* [Detexify](https://detexify.kirelabs.org/classify.html)：手工画出“大致的样子”就能查询对应的Latex写法！ 
* [vectorizer.ai](https://vectorizer.ai/)：在线**将jpg、png等位图矢量化**，转为svg格式保存。 
* [BarberGPT.ai](https://www.barbergpt.ai)：不用Photoshop也能换发型 
	* pixian.ai
	* hairstyleai.com：贵
* [_Cloudcraft_ – Draw AWS diagrams](https://www.cloudcraft.co/)：创建一个基于云的基础设施,并使用3D工具和技术以更好的方式将其**可视化**
* [WechatMomentScreenshot](https://github.com/TransparentLC/WechatMomentScreenshot)：朋友圈转发截图生成工具 
	* [git.io/WMS](https://git.io/WMS "https://git.io/WMS")
* [Queryable](https://github.com/mazzzystar/Queryable) ：「寻隐/Queryable」是一个离线的自然语言相册搜索工具
	* Run OpenAI's CLIP model on iPhone to search photos.
	* 开发学习

### 语音
* [whisper](https://github.com/openai/whisper)：OpenAI的**语音识别**模型 
	* [C/C++实现](https://github.com/ggerganov/whisper.cpp)
		- 表现
			- 准确率高
			- 没有标点
			- 中文会有些同音，但不对的字
			- 能产生srt，vtt字幕
			- large 的 model，1 小时的 talk 大约要 30 分钟、medium 约 16 分钟，但 medium 错误就蛮明显
			- 翻译功能（中=>英）
		- 部署
			- 没有外部依赖  
			- 不需要联网  
			- 内存使用率低  
		- 支持几乎所有的主流平台：  
			* Mac OS (Intel and Arm)  
			* iOS  
			* Android  
			* Linux / FreeBSD  
			* WebAssembly  
			* Windows (MSVC and MinGW]  
			* Raspberry Pi
		* 使用SwiftUI的Demo需注意
			* 先要下载好Model，如何下载模型在它的models目录下有说明： github.com/ggerganov/whisper.cpp/blob/master/models/README.md  
			* 然后放到SwiftUI项目的Resources/models目录下  
			* WhisperState类下的模型文件名要修改成对应的模型文件  
			* LibWhisper类中的”en”改成”zh”才能输出成中文结果
* [snipd](https://www.snipd.com/)：**整合AI的播客产品** 
	1. **能帮你生成文字版的摘要**  
	2. **自动生成字幕和翻译**  
	3. **自动提取高亮内容**，让你可以聚焦在关键的信息上  
	4. **自动生成笔记**，点一下就可以生成某个段落的摘要
* [NaturalReaders](https://www.naturalreaders.com/online/)：文字2语音工具 
	* <mark style="background: #FF5582A6;">免费版无法导出位mp3格式</mark>
* [bark](https://github.com/suno-ai/bark)：**文本->语音模型** 
	* **英语质量目前是最好的**
	* **会自动从输入文本中识别语言**，因此可以使用带有英语文本的德语历史提示。这通常会导致带有德国口音的英语音频。
	* **可选择将文本生成为音乐**，但您可以通过在歌词周围添加音符来帮助它。`♪ [TXT] ♪`
	* 支持100多种语言的扬声器预设
* [cheetah](https://github.com/leetcode-mafia/cheetah)：用Whisper和ChatGPT来**面试作弊** 
	* 利用Whisper进行实时音频转录，利用GPT-4/GPT-3.5生成提示和解决方案
* [audiopen.ai](https://audiopen.ai/)：这是一个集成ChatGPT的**音频笔记软件**，不止是是会录声音，还能转成文字，并且借助ChatGPT生成摘要。 
* Call Annie（[callsam.ai](https://callsam.ai)）：**练英语口语**，完全语音沉浸、无文字，适合提高口语对答。中国号码应该也能注册。 
* [HeyPi](http://heypi.com/) ：公认很会聊天的AI，不用担心把天聊死了，并且它支持文字和语音。语音输入需要借助苹果系统自带的输入。
* [pyannote-audio](https://github.com/pyannote/pyannote-audio)：声纹识别工具包 
* [audiocraft](https://github.com/facebookresearch/audiocraft)：直接用 AI 生成音乐 
* [WhisperX](http://github.com/m-bain/whisperX)：语音识别，按照单词对齐时间戳（生成的字幕都是完整的句子） 
	* 生成结果除了SRT还有JSON文件，里面有每一行里面单词的时间戳
	* 识别发言人
	* 似乎不支持 MAC，而且需要NVIDIA的显卡，好在Google Colab可以运行（需要启用GPU）
	* 根据YouTube Url识别YouTube字幕的[Jupyter Notebook](http://github.com/JimLiu/whisper-subtitles/blob/main/whisperx_youtube_subtitle.ipynb)
* [free-music-demixer](https://github.com/sevagh/free-music-demixer)：音源分离 
	* https://sevag.xyz/free-music-demixer/ 

### 文本
* [csv-to-markdwon](https://tableconvert.com/csv-to-markdown)：CSV 转 Markdown 
* [Mathcha - Online Math Editor](https://www.mathcha.io/)：在线数学编辑器 
* [火山写作✍️](https://writingo.net/home)：AI辅助写作工具，网页链接，支持中英文，可以纠正语法、拼写、格式等错误，还能智能改写、润色优化 
* [bilingual_book_maker](https://github.com/yihong0618/bilingual_book_maker)：文件/图书翻译，使用ChatGPT 
* [law-cn-ai](https://github.com/lvwzhen/law-cn-ai)：AI 法律助手 
* [AMYmind.com](https://amymind.com/) ：借助AI帮助你自动生成思维导图的在线思维导图和白板工具 
* [synk.io](https://snyk.io/)：给程序找Bug的AI 
* [ai-code-translator](https://github.com/mckaywrigley/ai-code-translator)：代码翻译 
	* https://ai-code-translator.vercel.app/
* [gpt_academic](https://github.com/binary-husky/gpt_academic)：GPT 学术优化 
* [ChatPaper](https://github.com/kaixindelele/ChatPaper)：论文阅读+润色+优缺点分析与改进建议+审稿回复 
* [ask2end](https://ask2end.com/)：AI把问题问到底
* [ChatDBG](https://github.com/plasma-umass/ChatDBG)：基于GPT的程序调试建议工具，将大型语言模型集成到标准调试器(pdb、 lldb 和 gdb)中，以帮助调试代码 
* [ebook-GPT-translator](https://github.com/jesselau76/ebook-GPT-translator)：借助ChatGPT帮助翻译电子书，支持PDF、Word、Mobi和Epub等格式。 
* [gpt4all](https://github.com/nomic-ai/gpt4all)：一个基于聊天机器人，接受了大量干净的助手数据的训练，包括代码、故事和对话。可以在M1 Mac 上流畅运行。也是基于 LLaMa + GPT-3.5-Turbo训练的。 
* [MathTranslate](https://github.com/SUSYUSTC/MathTranslate)：LaTex翻译工具，支持谷歌翻译引擎和腾讯翻译引擎，能一键翻译 arxiv 上的大部分（有LaTex源文件的）论文 
* [donut](https://github.com/clovaai/donut)：基于神经网络的OCR代码，支持表格识别 
* OCRmyPDF：实现在扫描版 PDF 中检索文字  
	* `brew install ocrmypdf`
	* `ocrmypdf input.pdf output.pdf -l chi_sim+eng`
* [ChatLaw](https://github.com/PKU-YuanGroup/ChatLaw)：ChatLaw-法律大模型 
	* [chatlaw.cloud/lawchat/](https://chatlaw.cloud/lawchat/ "https://chatlaw.cloud/lawchat/")

### 视频
* [open-chat-video-editor](https://github.com/SCUTlihaoyu/open-chat-video-editor)：短视频生成和编辑工具 
* [VideoCrafter](https://github.com/VideoCrafter/VideoCrafter)：一个用于文本到视频生成和编辑的工具包 
* [rask.ai](https://www.rask.ai/)：**自动将视频内容翻译并进行自动配音**的AI工具 
	* 免费版可以翻译2个视频，付费版可以翻译25分钟和100分钟的视频，额外的1美元1分钟。而且支持将视频翻译和配音为 60 多种可用语言。

### ChatGPT
* [chatbot-ui](https://github.com/mckaywrigley/chatbot-ui)：类似于ChatGPT的web聊天程序 
* [OpenPrompt](https://openprompt.co/#)：开放的共享Prompt社区 
* [SnackPrompt](https://snackprompt.com/)：ChatGPT Prompt提示分享社区 
* [ChatGPT-Next-Web](https://github.com/Yidadaa/ChatGPT-Next-Web)：一键免费部署你的私人 ChatGPT 网页应用 
* [ChatGPT 学习手册](https://nujuo8y1qx.feishu.cn/docx/AdqEdlT52oBiawx6Vv2cc89DnLb) 
* [Welcome | Learn Prompt](https://www.learnprompt.pro/docs/intro) ：学习 Prompt 
* [《ChatGPT 中文调教指南》](https://chatguide.plexpt.com/?continueFlag=91c65c17ba3b6d83808143f06a0d8abc)：一些 Prompt 
* [AI-Products-All-In-One](https://github.com/TheExplainthis/AI-Products-All-In-One)：這個 Repository 整理了當前將 ChatGPT 產品化的服務 
* [ChatGPT Shortcut](https://www.aishort.top/)：简单易用的 ChatGPT 快捷命令表
* [liftoff](https://github.com/Tameyer41/liftoff)： AI 对你进行技术面试，并给出能力评估 
* [Gamma.app](https://gamma.app/)：PPT 制作工具，支持中文与多人协作 
* [gpt-migrate](https://github.com/0xpayne/gpt-migrate)：让 AI 重写整个项目代码，实现所有代码框架、编程语言的迁移。 
	* 你可以将原有的 Python 项目，用 JavaScript 重写为新项目，AI 会自动帮你生成新的目录结构、文件命名、项目依赖包。
* [manga-image-translator](https://github.com/zyddnys/manga-image-translator)：一键翻译各类图片内文字 
	* 日漫图片翻译
* [Data-Copilot](https://github.com/zwq2018/Data-Copilot)：Bridging Billions of Data and Humans with Autonomous Workflow

### 键盘
* [Karabiner](https://sspai.com/link?target=https%3A%2F%2Fpqrs.org%2Fosx%2Fkarabiner%2F)：开源的改键工具 
