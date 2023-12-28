


# Echo

在AR中探索肢体交互、图像视觉和声音合成的关系

***“Echo”（暂用名）是由中国美术学院创新设计学院媒介与交互研究所学生进行并在Github同步更新进度的数字媒体艺术项目***

***详细技术解决方案见branch[“技术解决方案记录”](https://github.com/RipVanWinkle3939/Echo/tree/%E6%8A%80%E6%9C%AF%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88%E8%AE%B0%E5%BD%95)***

## 我们要做什么
我们希望做出一套系统，使得戴上AR眼镜的你/你们可以共同看见你们之间的微妙联系，听见你们之间的空间所发出的声音，你的动作会实时改变AR中的视觉元素，当你用你的动作改变这一微妙联系之时，空间所发出的声音也会因此改变。
这意味着，我们需要实时读取使用者的肢体信息，利用其创作出AR空间中的视觉元素并随着肢体信息改变而改变，同时利用肢体信息进行声音设计以及实时的声音合成，再将这些赋予使用者的设备。

###### ——————2023/12/8——————
我们试图

 1. 探究单人、双人以至多人间，在AR语境下的交互形式，并将所有的**点子**记录下来。这个被记录的**点子**将详细记录该交互动作的过程以及点子诞生时随之而生的思考。并且这个**点子**将被存储为一个视频文件、肢体动作追踪的osc信号数据包以及对其进行描述的文本文件。
 2. 对被记录的点子进行详细的语义解读，再进行初步的**视觉设计**——该点子中所记录的动作在AR中可以对应什么样的视觉，动作数据的变化对视觉又会有什么样的影响。
 3. 对被记录的点子进行**声音设计**——该点子中所记录的动作可以对应到什么样的声音，动作数据的变化对声音又会有什么样的影响。

我将在此对这样的行为进行记录，囿于过程可读性，暂且仅将过程“1”以及其中产出的文件进行记录。
技术流如下：Unity——AR Foundation——UniOSC/oscJAck——Maxmsp
***详细技术解决方案见branch[“技术解决方案记录”](https://github.com/RipVanWinkle3939/Echo/tree/%E6%8A%80%E6%9C%AF%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88%E8%AE%B0%E5%BD%95)***


| “点子”代称 | 日期 | 描述 | 视频 | osc数据包 | 备注 |
|--|--|--|--|--|--|
| “雷达” | 2023/12/9 | 多人“朝向”方向之间的关系 |  |  | 捕捉肩部数据 |
| “挤压” | 2023/12/14 | “贴近与撞击” |  |  | 身上套着壳子 |
| “撕扯” | 2023/12/14 | 多人“距离”之间的关系 |  |  | 肢体拉丝 |
| “和弦” | 2023/12/15 | 单人双手和躯干位置关系 | ![和弦](https://github.com/RipVanWinkle3939/Echo/blob/0281a8c365a91f11c0d47fe60bd78374b1188b76/%E8%A7%86%E9%A2%91/%E2%80%9C%E7%82%B9%E5%AD%90%E2%80%9D/hexian1.mp4) |  | 单人身体形态 |

###### ——————2023/12/17——————
接下来我们需要将所有功能集成，这需要实时的AR画面和声音合成。
在视觉上，我们使用HoloKit的AR解决方案
在声音上，我们使用Csound进行声音的合成和编排

###### ——————2023/12/23——————
已实现效果：双手距离控制音高，身体高度控制音量的正弦合成器。有频率随音高改变的正弦波图形视觉。具体见GIF（声音无法录制）。

![soundless](%E8%A7%86%E9%A2%91/%E6%95%88%E6%9E%9C/waveline.gif)

###### ——————2023/12/27——————
动作与视觉的关系向舞蹈动作匹配。
新增拍手和甩手的功能
![line3](%E8%A7%86%E9%A2%91/%E6%95%88%E6%9E%9C/line3.gif)
