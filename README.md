本示例相关代码见github：
https://github.com/lzhenboy/Speech2Text.git
#### 1、视频抽取语音
**目标**：从视频文件中抽取语音<br>
**工具**：ffmpeg<br>
**安装**：
```
brew install ffmpeg
```
**示例**：
```
ffmpeg -i video-demo.mp4 -f wav -ar 16000 audio-demo.wav
```
**参数解释**：
```
-i video-demo.mp4 # 输入文件路径
-f wav # 输出语音文件格式为wav
-ar 16000 # 采样率为16000
speech-demo.wav # 输出文件路径
```

#### 2、语音识别
**目标**：从语音中识别文本<br>
**开源实现**：[SpeechRecognition](https://pypi.org/project/SpeechRecognition/)<br>
**安装**：
```
pip install SpeechRecognition
```
**示例**：
```
python speech2text.py

```

**效果评估**：<br>
对语音连续的音频文件，google的语音识别接口识别效果较好，但对于中间有长时间停顿的音频文件，语音识别效果一般，往往会将后半部分漏掉。


#### 参考文献
1、[使用Python进行语音识别---将音频转为文字](https://zhuanlan.zhihu.com/p/26121974)<br>
2、[Python使用Speech_Recognition实现普通话识别](https://www.cnblogs.com/lishangzhi/p/12089981.html)<br>
3、[ffmpeg 从视频中提取WAV格式的音频](https://blog.csdn.net/huplion/article/details/80839944)<br>
