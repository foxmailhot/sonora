# Sonora 音效库 · 1.2.6

面向剪辑师、配乐师及媒体从业者的本地音频素材工作站：查找、试听、打标、变调，并将素材拖入剪辑软件。

![Uploading image.png…]()


## 下载与升级

[下载最新正式版](https://github.com/foxmailhot/sonora/releases/latest) · [所有版本与更新记录](https://github.com/foxmailhot/sonora/releases) · [反馈 BUG](https://github.com/foxmailhot/sonora/issues)

首次安装或从旧版升级，请运行发布页的 **升级安装包 EXE**。从 1.2.4 开始，Windows 安装版在启动后自动检查并下载正式版更新；保存工作后确认安装，不会无提示关闭软件。设置内可关闭自动检查，或手动检查更新。便携版和 Mac 请手动下载，不宣称支持自动替换安装。

资料库保存于用户“文档 / Sonora 音效库数据”，不在安装目录中；升级不会主动清除分析记录、人工标签、锁定和收藏。重要资料建议在升级前导出备份。1.2.6 当前发布包为 Windows x64；没有本次已验证的 Mac 安装包。

## 基本使用

1. 打开资料库，选择音频目录；路径页也可浏览尚未分析的素材。
2. 单击曲目试听，点击顶部波形可定位；资料分类、标签、收藏和搜索帮助查找。
3. 需要识别时确认开始，可叠加本地声音事件模型；停止后保留已完成结果。
4. 音效工作台和剪辑工作台提供筛选、试听和变调。将素材直接拖入剪辑软件；加工文件须生成完成后才可外拖。
5. 右键可编辑人工标签、转码、查看分析信息。人工/AI 锁定标签受保护。

本地声音事件分数不是正确率；情绪与剪辑场景建议仍需试听确认。不同编码文件可能损坏或受保护，支持扩展名不等于能修复损坏的文件。丢失原文件仅隐藏显示，不删除存档；实际存在但不能解码的素材保留在“分析异常”。

## 1.2.6 更新

- 修复调音台素材数量存在但列表不可见的问题；排序、搜索和文件视口不再抢占布局区域。
- 调音台左右路径页真实读取所选文件夹，能显示资料库之外、尚未分析的音频；路径浏览不自动识别，也不写入资料库。
- 主界面和两侧目录采用独立可取消的分页会话，修正隐藏筛选、旧分页及深滚动造成空列表的情况。
- 新增自定义主题点缀色：输入 RGB / #RRGGBB、使用颜色选择器或屏幕吸管（按 Esc 取消）。
- 壁纸设置增加“框体底色不透明度”，只改变背景，不整体降低文字、按钮和波形透明度。
- 229 项测试与打包界面回归通过，覆盖 1280×720、1480×920、2048×1152/125%；吸管真实屏幕像素选择、覆盖安装及 Mac 未自动化实测。

## 1.2.5 更新

- 音效库、音效工作台和剪辑工作台增加排序下拉菜单，默认新加入的音频排在最前面。
- 支持按名称、时长、BPM、文件修改时间和可重编曲性排序；剪辑工作台保留综合推荐、匹配度与项目使用次数。
- 加入时间保存在本地资料库，重新分析、收藏和编辑标签不会刷新。旧记录无法准确追溯加入日期，排在新记录后面。
- 列表与井字视图共享排序；切换排序不清除筛选和选中项。
- 224 项测试、真实打包界面与本地更新下载校验通过；未运行覆盖安装。

## 1.2.4 更新

- 增加 GitHub Releases 正式版自动检查、下载进度和确认升级；断网不阻塞编辑。
- 保留 1.2.3 收藏筛选、丢失文件隐藏、档案保护与工作台试听流程。
- 完善技术来源、本地模型说明及赞赏入口。

## 使用的开源技术

Sonora 本身的版权与第三方组件的许可证分别适用。下面列出工程中直接使用的主要项目及作者/维护者；[完整解析依赖来源清单](THIRD_PARTY_COMPONENTS.md) 包含传递依赖。“参考项目”不等于随安装包分发。

| 项目 | 作者 / 维护者 | 用途 / 源地址 |
| --- | --- | --- |
| Electron | Electron 社区 / OpenJS Foundation | 桌面与原生拖放：[electron/electron](https://github.com/electron/electron) |
| React | Meta 与 React 贡献者 | 界面：[facebook/react](https://github.com/facebook/react) |
| SQLite | SQLite developers | 本地事务存储：[sqlite/sqlite](https://github.com/sqlite/sqlite) |
| stream-json | Eugene Lazutkin | 大档案流式导入：[uhop/stream-json](https://github.com/uhop/stream-json) |
| FFmpeg / ffmpeg-static | FFmpeg developers / eugeneware contributors | 解码、转码：[FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)，[eugeneware/ffmpeg-static](https://github.com/eugeneware/ffmpeg-static) |
| SoundTouchJS / audio-worklet | Steve “Cutter” Blades 与贡献者 | 保持时长变调：[cutterbl/SoundTouchJS](https://github.com/cutterbl/SoundTouchJS) |
| lamejs / BreezyStack 分支 | Alex Zhukov / shijinyu | MP3 编码：[zhuker/lamejs](https://github.com/zhuker/lamejs)，[shijinyu/lamejs](https://github.com/shijinyu/lamejs) |
| Lucide | Eric Fennis 与贡献者 | 图标：[lucide-icons/lucide](https://github.com/lucide-icons/lucide) |
| Vite / React 插件 | Evan You 与 Vite 贡献者 | 构建：[vitejs/vite](https://github.com/vitejs/vite)，[vitejs/vite-plugin-react](https://github.com/vitejs/vite-plugin-react) |
| TypeScript | Microsoft 与贡献者 | 类型检查：[microsoft/TypeScript](https://github.com/microsoft/TypeScript) |
| electron-builder / electron-updater | Vladimir Krivosheev 与贡献者 | 安装包与更新：[electron-userland/electron-builder](https://github.com/electron-userland/electron-builder) |
| Vitest | Vitest 贡献者 | 回归测试：[vitest-dev/vitest](https://github.com/vitest-dev/vitest) |
| concurrently | Open CLI Tools 贡献者 | 开发任务：[open-cli-tools/concurrently](https://github.com/open-cli-tools/concurrently) |
| cross-env / wait-on | Kent C. Dodds 与贡献者 / Jeff Barczewski | 构建辅助：[kentcdodds/cross-env](https://github.com/kentcdodds/cross-env)，[jeffbski/wait-on](https://github.com/jeffbski/wait-on) |

## 使用的模型与本地运行组件

- **EfficientAT MN04 / MN10**：Florian Schmid 等；[官方代码与权重](https://github.com/fschmid56/EfficientAT)，[原始发布页 v0.0.1](https://github.com/fschmid56/EfficientAT/releases/tag/v0.0.1)。Windows 包内使用 FP32 ONNX 转换模型，对 AudioSet 527 类声音事件进行推理。代码 MIT；原始权重没有在本次核验中找到单独明确的授权条款，不能将代码 MIT 当作权重再分发许可。
- **ONNX Runtime**：Microsoft 与贡献者；[microsoft/onnxruntime](https://github.com/microsoft/onnxruntime)，内置轻量 CPU 推理运行组件。
- **Python**：Python Software Foundation；[python/cpython](https://github.com/python/cpython)，用于独立模型进程。
- **NumPy**：NumPy 贡献者；[numpy/numpy](https://github.com/numpy/numpy)。运行组件还包含 [protobuf](https://github.com/protocolbuffers/protobuf)、[FlatBuffers](https://github.com/google/flatbuffers)、[coloredlogs](https://github.com/xolox/python-coloredlogs)、[humanfriendly](https://github.com/xolox/python-humanfriendly)、[SymPy](https://github.com/sympy/sympy)、[mpmath](https://github.com/mpmath/mpmath)；作者和许可证以各项目与随附组件文件为准。
- **AudioSet**：Google Research；[数据集与类别说明](https://research.google.com/audioset/)。只使用类别索引/映射，不分发 AudioSet 原始音频。
- **PyTorch / ONNX**：模型转换与开发验证使用，[pytorch/pytorch](https://github.com/pytorch/pytorch)，[onnx/onnx](https://github.com/onnx/onnx)；不是轻量安装包内的推理后端。
- **Essentia / YAMNet**：算法研究参考，[MTG/essentia](https://github.com/MTG/essentia)，[tensorflow/models YAMNet](https://github.com/tensorflow/models/tree/master/research/audioset/yamnet)；未内置其模型。

模型识别在本机运行。可选云端 AI 需要用户填写自己的接口密钥并确认调用，不随安装包提供密钥；模型名称与可用性由对应服务提供商决定。

## 版权与赞赏

软件版权归 **xixiwenjia@qq.com** 所有，软件免费。如果通过收费途径获取，请申请退款，可将售卖渠道信息发送到上述邮箱。第三方组件保留各自作者版权和许可证；本页面不是将整个 Sonora 工程授权为 MIT 的声明。

**如果觉得这个软件不错，也赞赏一下作者吧！**

感谢每一位支持 Sonora 的同行，愿你今天灵感常在、好音常伴。

<img src="assets/sonora-tip-code.jpg" alt="作者赞赏码" width="360" />

