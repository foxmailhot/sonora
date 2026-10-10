# 本地模型、标签和推理依赖来源

1.2.2 按用户明确要求，在 Windows 安装包中提供 MN04/MN10 ONNX 转换权重与 CPU 运行组件。上游仓库展示 MIT 许可并发布预训练模型；未找到另外单列的权重许可。本次保留上游许可和来源，不把用户授权打包等同于额外商用/再分发授权确认。1.2.1 历史安装包不含权重。

|组件|来源/作者|版本/许可与处理|
|---|---|---|
|EfficientAT代码|Florian Schmid，https://github.com/fschmid56/EfficientAT|固定a425fdce92572e602a1d5634799bd9f1f2efa806；MIT；原LICENSE保留在vendor|
|MN04/MN10官方权重|同仓库v0.0.1 release|SHA/URL/大小见manifest.json；未找到单独权重许可说明，原 .pt 不打入安装包|
|本机ONNX转换文件|由上述权重及官方预处理转换|opset17、FP32、未量化；转换报告与SHA见onnx-manifest.json；1.2.2 Windows 随包内置，仍有原权重许可边界|
|AudioSet527类别索引|上游metadata/class_labels_indices.csv；AudioSet：https://research.google.com/audioset/|保持原索引、ID和英文；1.2.2 全量中文映射仅为显示层；未分发AudioSet音频数据；不把整个AudioSet本体授权范围作未经核验的承诺|
|ONNX Runtime|Microsoft，https://github.com/microsoft/onnxruntime|1.20.1，MIT；组件保留包内LICENSE/ThirdPartyNotices|
|Python|Python Software Foundation，https://www.python.org/|3.12.10 Windows嵌入版，PSF许可与第三方说明，保留LICENSE.txt|
|NumPy|NumPy Developers，https://numpy.org/|2.5.2，保留dist-info/licenses（含其二进制依赖通知）|
|辅助Python包|各组件dist-info/METADATA|protobuf5.29.5、flatbuffers24.12.23、coloredlogs15.0.1、humanfriendly10.0、sympy1.13.1、mpmath1.3.0；原许可与作者信息保留|
|官方参考/转换环境|PyTorch Foundation/相关作者，https://pytorch.org/；https://github.com/onnx/onnx|torch2.5.1+cpu/vision0.20.1/audio2.5.1、ONNX1.17；开发环境使用，不随精简组件分发；来源和依赖固定在requirements|

PythonZIP：4acbed6dd1c744b0376e3b1cf57ce906f9dc9e95e68824584c8099a63025a3c3。

MN04 .pt：899a8c6217063f6941793102a2780b3dd788ab11fce468d9cf5f0577c453321c。

MN10 .pt：0bd7dc2443af498c289a2e739f02ebb515d6aa3fd3ab9db539c86123ae368a4e。

本地模型推理无下载器、遥测和外部日志上传。只有用户明确点“获取模型”调用官方URL；音频和识别结果不上传。未知/损坏模型拒绝加载，不能绕过校验。

