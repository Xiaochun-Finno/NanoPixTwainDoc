## ADF 传输模型的特点和适用软件

| 传输模型       |       适用软件        |
|----------------|----------------------|
| [B]Simplified  | Archy，OpenDental，XDR，TigerView（单张不关闭源，可实现边采边传）；|
|                | Apteryx(XV)，Curve（单张关闭源，支持伪ADF，支持暂存区批量多张传输）|
| [C]Classic     | 大多数支持ADF的软件使用该版本会出现“延迟一张传输”问题，|
|                | Vixwin，LynxVision和EzDent除外（边采边传，不会延迟一张），   
|                | B版本中的app单张采集传输也可支持，但可能没有B版本稳定；|
| [D]Advanced    | EzDent-i, CareStream, Dexis，B版本中的app也可支持，但可能没有B版本稳定。|
|                | 大多数支持ADF的软件使用该版本不会出现“延迟一张传输”问题|

如果上位软件没有默认的传输模型时，需要尝试这三种传输模型，应按照【B】->【C】->【D】的顺序进行测试，直至“连续传输”功能正常，适配成功。比如，测试发现【B】传输模型能适配成功，则停止测试，否则按照顺序测试剩下的【C】和【D】传输模型。如果测试发现所有的传输模型都不能适配成功，则需要进一步调查上位软件，并分析原因（比如分析售后提供截屏或视频），解决问题；如果问题仍然不能解决，力争拿到上位软件的试用程序，进行本地测试和调试Twain程序,看能不能解决问题。

## 已测试的上位软件支持列表
### Dental 软件
|序号| 上位软件             |   传输模型   |
|--|-----------------------|--------------|
|1 | CS Imaging            |     D        |
|2 | Apteryx XrayVision    |     B        |
|3 | Dexis                 |     D        |
|4 | VixWin                |     C        |
|5 | OpenDental            |     B        |
|6 | EzDent                |     D        |
|7 | Archy                 |     B        |
|8 | Archy(In-Process)     |     B        |
|9 | TigerView             |     B        |
|10| Curve                 |     B        |
|11| XDR                   |     B        |
|12| XDR                   |     B        |
|13| Core Practice         |     B        |
|14| Oryx                  |     D        |
|15| DentiView             |     B        |
|16| Sidexis               |     D        |
|17| Dentrix Ascend        |     B        |
|18| Eaglesoft             |     B        |
|19| LynxVision            |     C        |
|20| Sota                  |     B        |
### 通用软件
|序号| 上位软件             |   传输模型   |
|--|-----------------------|--------------|
|1 | PhotoShop             |     B        |
|2 | DynamSoft             |     B        |
|3 | XnView                |     B        |
|4 | IrfanView             |     B        |
|5 | NAPS2                 |     B        |


上位软件调用Twain界面的操作视频可参考[NanoPix Twain兼容软件视频](https://www.youtube.com/playlist?list=PLRMqU9ylVrDxeebvkFFowd46Yiq_o8vny)。

还可参考[Apex Dental Sensor兼容软件视频](https://www.youtube.com/playlist?list=PL7BcoCsLx7VtyhFXZhbAoOsKxCuj_69Ye)。

## 上位软件需要做的设置

### 1. XDR
Close After Transfer不要勾选！！！

![Setting Image](./resource/host_app/XDR.png)

### 2. OpenDental
Show Twain UI 要勾选！！！

![Setting Image](./resource/host_app/OpenDental.png)

### 3. Sidexis
Automatic document feed 要勾选！！！

![Setting Image](./resource/host_app/Sidexis.png)

### 4. Archy
测试发现 Run In-Process 需要勾选，要不然有些时候会出现曝光了之后不能出图的现象

![Setting Image](./resource/host_app/Archy.png)
