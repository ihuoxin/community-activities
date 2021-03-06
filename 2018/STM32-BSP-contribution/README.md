# STM32 BSP 贡献挑战活动

## 活动简介

首先，非常感谢各位开发者参与STM32 BSP 贡献挑战活动， 为 RT-Thread 尽一份力。参与活动需要先看此文档了解活动规则和流程。挑战活动完成即可获得相应奖励！

## 活动目标

参与 STM32 BSP 贡献挑战活动需要完成下面  2 个阶段的目标：

* 第一阶段：完成基础 BSP， 包括串口驱动和 GPIO 驱动，能运行 FinSH 控制台。完成 MDK4、MDK5 、IAR 和 GCC 编译器支持，如果芯片不支持某款编译器（比如MDK4）可以不用做。 BSP 的 README.md 文件需要填写第二阶段要完成的驱动。

* 第二阶段：完成板载外设驱动支持，所有板载外设使用 menuconfig 配置后就能直接使用。若开发板没有板载外设，则此阶段可以不用完成。

## 活动规则

STM32 BSP 贡献挑战活动规则如下：

* 贡献的 BSP 不能和其他人重复，且 RT-Thread 仓库还没有支持此 BSP。

* 参与活动必须填写跟踪表，方便跟踪每个人的进度。

* 第一阶段目标完成截止日期为二个周，逾期视为挑战失败。

* 第二阶段目标完成截止日期为一个月，逾期视为挑战失败。

* 第一阶段和第二阶段全部完成才算挑战成功！

* 鉴于第二阶段时间跨度比较长，开发者可以完成一些驱动后就提 PR，可以根据此 PR 了解完成状态，全部驱动完成后 PR 才会被合并。

## 活动奖励

挑战成功的小伙伴可以获得如下奖励：

* 可观看 RT-Thread 内部技术公开课（代码贡献专享）

* 可尝鲜获得 STM32 新品板卡，如 STM32G0、STM32WB

* 年底可参与 RT-Thread 年度杰出贡献奖评选

* RT-Thread 公司不定期福利

* 个人账号会被展示在 Github RT-Thread contributors

## 活动流程

活动的主要流程如下图所示：

![STM32 BSP 贡献挑战活动流程](figures/bspflow.png)

### 选择未支持的开发板

* 查看 STM32 BSP 的 [README.md 文件 (STM32 BSP 说明文档)](https://github.com/RT-Thread/rt-thread/tree/master/bsp/stm32)，确认一下要做的 BSP 是否已经支持，若已经支持，则不需要重复造轮子。

* 确认跟踪表里是否有此BSP，若已经有其他开发者在参与此 BSP 的制作，那么只有在其他开发者挑战失败的情况下才可以参与此 BSP 贡献挑战。

### 填写 BSP 提交跟踪表

在本文跟踪表统计小节填写新增 BSP 信息。可在 GitHub 仓库在线修改 README.md 文档。修改及提交步骤如下所示：

* 按下图所示点击编辑按钮修改文档。

![新增跟踪信息](figures/edit.png)

* 然后在跟踪表章节新增自己的信息，填写完成可以点击 `Preview changes`查看预览效果，确认格式是否填写正确。

![新增跟踪信息](figures/add.png)

* 信息添加完成后填写提交信息并提交，比如“增加 ST 官方 stm32f091-nucleo 开发板”等。

![新增跟踪信息](figures/pr.png)

### fork RT-Thread 源代码仓库

参考文档《向 RT-Thread 贡献代码》，fork RT-Thread 源代码仓库，clone 自己的仓库到本地，并新建分支开发 BSP。

### 根据指导文档制作 BSP

参考 STM32 BSP 的 [README.md 文件 (STM32 BSP 说明文档)](https://github.com/RT-Thread/rt-thread/tree/master/bsp/stm32) 的 BSP 制作教程小节，根据此文件的详细步骤制作新的 BSP。

### BSP 完成提 Pull Request

BSP 按照规范制作完成后推送到自己的 GitHub 仓库并提 PR，参考文档《向 RT-Thread 贡献代码》。

### 根据 review 意见更新 BSP

GitHub 提 PR 后需要关注 PR 状态，相关的评审意见会在这里更新，根据评审意见及时修改 BSP。

### PR merged

BSP 修改完成，评审通过后才会被 merge。

## 跟踪表模板

下面表格为 BSP 提交跟踪表模板：

|**GitHub ID**| **RT-Thread 论坛 ID** |        **开发板名称**        |    **BSP 文件夹名称**  | **第一阶段目标** |**第二阶段目标** |**开始日期**|  **完成状态**|
| ------------| ---------------------|------------------------------| ----------------------| --------------  |--------------- | -------- | --------------- |
|       yyyq  |         yyyq         |ST 官方 stm32f091-nucleo 开发板 |  stm32f091-st-nucleo  |      待完成      | 待完成         |  2019/1/8 | 已提 PR  |
|       xxxxa |         xxxxa        |正点原子 F103 NANO 开发板       |   stm32f103-atk-nano  |      已完成      | 待完成         | 2019/1/10 |  待完成   |

表格各项目填写说明如下面表格所示：

|**表格项目**|  **说明**         |
| ------------- | --------------------------- |
|   GitHub ID     |  开发者 GitHub ID    |
|   RT-Thread 论坛 ID |  开发者 RT-Thread 论坛 ID    |
|   开发板名称     |   开发板官方名称，参考 STM32 BSP 的 [README.md 文件 (STM32 BSP 说明文档)](https://github.com/RT-Thread/rt-thread/tree/master/bsp/stm32)里面其他开发板的命名         |
|   BSP 文件夹名称 |   命名规则为：芯片型号  +  厂家名称 + 板子名称 ，参考 [STM32 BSP](https://github.com/RT-Thread/rt-thread/tree/master/bsp/stm32) 其他开发板的命名   |
|   第一阶段目标   | 第一阶段目标完成情况：待完成 或者 已完成    |
|   第二阶段目标   | 第二阶段目标完成情况：待完成 或者 已完成  |
|   开始日期      | 开始日期                      |
|   完成状态      |   开发者可以不用填写     |

## 跟踪表统计

要提交 BSP 需要填写提交跟踪表，根据上面小节的描述在这份表格里面填上自己的信息，注意不要修改其他开发者填写的内容。

|**GitHub ID**|**RTT论坛 ID**|**开发板名称**|**BSP 文件夹名称**|**第一阶段目标**|**第二阶段目标**|**开始日期**|**完成状态**|
| ------------| ----------|------------ | ----------------| -------------- |---------------| ---------|-----------|
| XiaojieFan  | 小住住     |  硬十ibox    | stm32f103-hw100k-ibox|已完成      |   待完成LoRa    |  2019/1/8| 已完成 W5500,ESP8266,RS485,I2C,RTC,ADC,IWG.  |
| e31207077  | e31207077  | NUCLEO-F767ZI | stm32f767-st-nucleo|已完成      | 待完成        |  2019/1/9|   |
| jinsheng20  | jinsheng  |  stm32f746-disco | stm32f746-st-disco|已完成    | 待完成       |  2019/1/9|    |
| sunshine0824| sun_shine |  Nucleo-L432KC | stm32l432-st-nucleo|已完成    |  |  2019/1/31| 已完成 rtc,iwdg,onchip flash  |
| andeyqi     | andeyqi   |  NUCLEO-F446ZE | stm32F446-st-nucleo|已完成    | 待完成          |  2019/1/9|   |
| FindYGL     | Glen_Young| LY-STM32F103C8V1.2 |stm32f103-dofly-lyc8|已完成 | 待完成       |  2019/1/9|  |
| whj4674672 |  无        | 麦克泰 F107 μc_Eval开发板 |stm32f107-uc-eval|已完成 | 待完成     |  2019/1/9|  |
| Vincent-VG | wzw66      | NUCLEO-L476RG | stm32l476-st-nucleo | 已完成    | 待完成       | 2019-1-17 |  |
| gztss      |            | NUCLEO-G072RB  | stm32/stm32g071-nucleo | 已完成 | 待完成       | 2019-1-17 |  |
| Jackistang | Jacksi     | 野火 F103 指南者开发板 | stm32f103-fire-guide | 待完成 | 待完成  | 2020-4-29 |  |
