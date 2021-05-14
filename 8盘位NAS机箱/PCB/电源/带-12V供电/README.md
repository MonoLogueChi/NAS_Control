# DC2ATX

基于 [KCORES-CSPS-to-ATX-Converter](https://github.com/KCORES/KCORES-CSPS-to-ATX-Converter) 修改的一个适合 NAS 使用的 DC-ATX 转接板。

相比原版，拥有以下特点

1. 重新定义了硬盘供电线序，并且拥有更多的硬盘供电接口
2. 增强 5V 输出能力
3. 增加 -12V 输出

## 说明

- 如用在其他项目，推荐使用双板电源，体积更小
- ATX 模组线与双板电源不通用
- 如不用 -12V 供电，-12V 部分可不焊接
- ~~如不需要修改，直接下载`Gerber`文件，直接下单 PCB 打样即可~~。

## 注意事项

- 注意事项参见 [KCORES-CSPS-to-ATX-Converter](https://github.com/KCORES/KCORES-CSPS-to-ATX-Converter)

## 预览

非实时，详情请以实际为准。

### 原理图

![原理图](IMG/Schematic_MyNAS-DC2ATX_2_2021-05-14.svg)

### 主电源板

![主电源板顶面](IMG/PCB顶面.svg) ![主电源板底面](IMG/PCB底面.svg)

## BOM

非标准 BOM 表，方便购买

- `CSPS_64P_2.54MM` 某宝可搜 `FCI 64P 2.54MM`(质量较好，价格较高) 或 `SLOT 64P` `WingTAT 64P`(较便宜，低功率电源适用，注意看好间距)
- `5566连接器` 规格：`2*10P`(ATX 供电) `2*4P`(CPU/PCIE 供电) `2*2P`(硬盘供电)
- `IC座` DIP8
- `接线端子` 5.08MM 3P
- `排针` 2.54mm 3P 4P 配跳帽
- `电阻` 封装 1206，阻值 `22K` `3.3K` `2.67K`(高精度)
- `电容` 封装 1206，50V 100nF
- `钽电容` 封装 3528(B 型)，10V 47uF 或更高 3 个
- `二极管` 封装 DO-41，1N4001 或 1N4004
- `PW22ASAB` 海鲜市场拆机货，接 2.67K 输出 5V
- `Mini560` 5V 和 3.3V
- `M3螺丝` M3\*5 或 M3\*6
- `纸垫片` 纸垫片，M3 螺丝兼容
- `铜丝` 紫铜 1.5mm - 2.5mm，可直接买紫铜，也可将铜线剥开使用，使用前注意除锈。
- `DM25` 或 `B1212S-1W`(需焊接外围电路，50V 2.2uF 电容\*2，1.5-3KΩ 电阻 \*1)，二选一

## LICENSE

[kcores-license](../LICENSE)
