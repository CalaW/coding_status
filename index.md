![svg](https://wakatime.com/share/@861a8c47-8fc9-4e74-962b-717a962d6838/5c6f2fd6-b3ee-4e2d-a015-9c673996c290.svg)
![svg](https://wakatime.com/share/@861a8c47-8fc9-4e74-962b-717a962d6838/34949166-4a2f-41b0-8f4e-bc1429216deb.svg)
![svg](https://wakatime.com/share/@861a8c47-8fc9-4e74-962b-717a962d6838/649aaf4f-32e4-441a-adb1-fa15a6b3bbf5.svg)

# 扒谱参考步骤

本文使用Audition及Logic Pro X进行演示。

## 提取音频中各声部

混音时为提升音乐的层次感、降低噪声，将各声部“放置”在空间中的一个虚拟位置上，称作**「声象」**。
可以利用这一特性，提取音频中某一方位的声音，从而提取音频中某声部。

### 人耳如何辨别声音方位？

方位感基于**「双耳效应」**产生：**声压差**（音量）+**相位差**（时间）$\implies$ 立体声

![image-20210403012718179.png](https://i.loli.net/2021/04/03/rTSvNqyQldxHIFJ.png)

### 步骤

使用 **Audition** 内置的**「中置声道提取器」**，按照相位表上的声音方向，提取声道。
该插件通过分析左右声道的共有频率，提取中置声道。[^1]

![截屏2021-04-03 下午12.22.40.png](https://i.loli.net/2021/04/03/BdKXRzSHavsxrWL.png)

> #### 拓展——制作伴奏
>
> 流行歌曲采用人声中置，配器分别安排在两边的混音方法。因此可以通过消除中置声道、保留两边声道来获得歌曲的伴奏。

## 导入宿主软件，同步速度和强拍

### 导入宿主软件

新建音频轨道，将音频拖入；
可以点击轨道页面左上角的加号新建轨道。

![截屏2021-04-03 下午12.31.11.png](https://i.loli.net/2021/04/03/2yQPirxDw3CRtjo.png)

### 标记音频速度与强拍

点击音频块，打开智能速度界面，**祈祷**它能识别出来音频速度。
note: 如果确定原音频是按节奏唱的，最好将速度改为**「恒定」**（不然会忽快忽慢）

![截屏2021-04-03 下午12.34.59.png](https://i.loli.net/2021/04/03/FJx26gzyO4LYUEc.png)

回放音频，检查强拍位置，并通过智能速度窗口设置强拍。

![downbeat](https://support.apple.com/library/content/dam/edam/applecare/images/zh_CN/proapps/logic/macos-logic-pro-x-10-4-2-tempo-set-downbeat.jpg)

更多关于「智能速度」的介绍可以参考 [Logic Pro 智能速度概览](https://support.apple.com/zh-cn/guide/logicpro/lgcp9281e70c/mac)。

### 将音频速度和强拍同步到项目

右键音轨，选择**「将片段速度应用到项目速度」**即可。
可以看到，项目速度与音频速度一致，项目的强拍也与音频一致。

![截屏2021-04-03 下午12.55.58.png](https://i.loli.net/2021/04/03/WvY7Bqd9E3jwNn5.png)

## MIDI录制及量化

MIDI(Musical Instrument Digital Interface)是一种数字音乐的技术标准，其中定义了MIDI文件格式，能够记录音高、时长、速度、运音法（颤音/滑音等）信息。

可以通过建立「软件乐器」轨道录制MIDI。点击轨道控制面板上的 **R** 按钮启用录制。
按键盘上的R键或点击软件上方录制钮开始录制，若没有MIDI键盘，可以使用Command+K调出软键盘。

![截屏2021-04-03 下午3.30.38.png](https://i.loli.net/2021/04/03/TyIrR5BM9AQCf2K.png)

录制完成后，需要进行「时间量化」，使MIDI音符对齐节拍。
选中所有音符，使用左侧的时间量化，按照具体情况选择量化标准（音符时长）即可。

![image-20210403153540466.png](https://i.loli.net/2021/04/03/WF6ieC3jgVGwn8d.png)


## 制谱

点击Command+5即可调出乐谱窗口。

![截屏2021-04-03 下午3.38.05.png](https://i.loli.net/2021/04/03/D38LKnN2BTwkiGj.png)

[^1]: https://helpx.adobe.com/cn/audition/user-guide.html/cn/audition/using/stereo-imagery-effects.ug.html
