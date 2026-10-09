# Introduction

## electric VS electrical VS electronic
1. electric：核心意思是电的、带电的、用电的、产生电的；语感偏具体、直接；常见对象有电流、电场、电荷、电击、电机、电车。
2. electical：核心意思是与电有关的、电气工程的；语感偏抽象、领域、系统；常见对象有电气工程、电气系统、电气设备、电气安全。
3. electronic：电子、弱电、半导体、信息处理。

## power VS energy
1. Power（功率）是能量转换/传输的速率，表示“多快”。the rate of energy transfer or conversion.
2. Energy（能量）是累计的能量总量，表示“多少”。the total amount of energy transferred or converted.

## Nameplate of an electric machine（电机铭牌）
1. HP（Horsepower）：马力，是电机的额定输出功率，1马力约等于745.7瓦特。
2. RPM（Revolutions Per Minute）：额定负载下每分钟转速。
3. VOLTS：额定电压。

## 电力变换（Power Conversation）
1. 定义：将一种形式的电能转换为另一种形式。
2. 核心器件：电力变换器（Power Converter），使用高功率能力的二极管或晶体管（半导体器件）。
3. 变换类型：
- 整流（Rectification）：整流器（Rectifier），AC（交流）转换为 DC（直流），使用整流器。
- 逆变（Inversion）：逆变器（Inverter），DC 转换为 AC，使用逆变器。
- 直流变换（DC-DC）：DC 转换为 DC，使用 DC-DC 变换器（升压 Boost 或降压 Buck）。
4. 电机驱动（Motor Drive）：电力变换器 + 电动机。

## 功率半导体器件（Power Semiconductor Devices）
1. 本质上是一个电子开关，只有断态（off state）和通态（on state）这两个主要状态。断态就是不导通，几乎没电流；通态就是导通，有电流通过，压降很小。
2. 器件有一个专门的控制端，比如 gate 或 base。你给这个控制端一个信号，就能让器件在断态和通态间转换，从而实现控制开通和控制关断。
### 二极管（diode）
1. 不可控（不可控制开通和关断），单向导通。
2. 有两个端，阳极A（Anode），阴极K（Cathode）。
3. 阳极电位高于阴极，且超过正向压降，二极管导通；阳极电位低于阴极，二极管截止。
4. 常用于：整流：AC → DC；续流：给电感电流提供通路；保护：防止反向电压；钳位：限制电压。

# Circuit Elements and Analysis Techniques
## International System of Units（SI单位）
1. 国际单位制。大多数国家接受为唯一法定测量系统。计算时永远使用 SI 单位。
2. 常见基本量与SI单位
```
Physical quantity 物理量	      Quantity Symbol 符号	Basic SI Unit Name 单位名	Unit Symbol 单位符号
长度 Length                    l, d, h, r            米 meter                  m
时间 Time                      t                     秒 second                 s
质量 Mass                      m                     千克 kilogram             kg
电流 Electric current          I                     安培 ampere               A
绝对温度 Absolute temperature   T                     开尔文 Kelvin             K
物质的量 Amount of substance    n                     摩尔 mole                 mol
发光强度 luminous intensity     Iv                    坎德拉 candela            cd
```

## Basic Terms in Electric System
### 基本电力系统的四个主要部分
1. The source 源：给系统提供能量，如电池、发电机。
2. The load 负载：吸收源提供的能量，如灯、加热器。
3. The transmission / distribution system 输配电系统：用绝缘导线/电缆把能量从源传到负载。
4. The control apparatus 控制装置：如开关。

### 电荷与电流
1. 电荷具有双极性（bipolar），自然界基本负电荷载体为电子（electron），正电荷载体为质子（proton）。
2. e = 1.6 * 10^-19，单个电子电荷-e，单个质子电荷+e。
3. 电荷不能被创造或销毁，但可以移动。典型导线或元件中，实际上只有电子能移动。
4. 电流通常是导体中电荷的运动。1A = 1C/s，即当 1 C 电荷在 1 s 内穿过特定面积，就流过 1 A 电流。
5. 电流在一点测量，有方向。
6. 电流密度（Current density）J = I / A（面积）。
7. 持续电流流动需要：Complete circuit 完整电路；Presence of a driving influence 存在驱动影响，如电压源。

### 电动势（Electromotive Force，EMF）
- 单位电荷通过源时消耗的能量。
- 总是主动的：产生电流的驱动影响。

### Potential difference (PD) 电位差 / Voltage 电压
- 单位电荷在电路中两点之间通过时转移的能量。
- 电压跨两点测量，有极性（+ 端电位高，- 端电位低）。
- 可以是主动的（给电荷能量的电压，像电源），也可以是被动的（消耗电荷能量的电压，像电阻）。
- SI 单位：Volt 伏特，V。
- 定义：移动 1 C 电荷从一点到另一点使用 1 J 能量时，两点间的电位差为 1 V。
- 用箭头定义电位差，箭头指向高电位节点；也可以用 + -。
- 用节点标记电压，假设先命名的节点电位更高。

## 参考方向与符号约定
### 关联参考方向 / 被动符号约定（associated reference directions / passive sign convention）
- 电流应进入正电压端。
- 计算 P=IV 的后果：正功率：元件吸收功率，被动。负功率：元件发出功率。

### 非关联参考方向 / 主动符号约定（non-associated reference directions / active sign convention）
- 电流应离开正电压端.
- 计算 P=IV 的后果：正功率：元件发出功率，主动。负功率：元件吸收功率。

## Load 负载：
- 通常指负载电阻中耗散的功率，而不是电阻本身。
- 小心：“no load 无负载”意味着无负载功率，所以：I=0 A,R=∞ Ω,P=0。即开路。

## 实践知识
1. 小规模铜电路：电流容量约 5 到 10 A per mm²。取决于类型、绝缘、环境温度等。
2. 为什么银做导线：银电阻率最低，但成本高、易氧化、机械强度/加工性不如铜，所以常用铜。
3. PCB（印刷电路板）：1 oz 铜厚：35 μm。2 oz 铜厚：70 μm。
4. 线宽单位：mil。1000 mil = 1 inch = 25.4 mm。所以 100 mil = 2.54 mm
5. AWG = American Wire Gauge，美国线规。它是一个导线尺寸标准，用来表示导线的直径或截面积。AWG 数字和导线粗细的关系是：AWG 数字越小，导线越粗，截面积越大，电阻越小，载流能力越大。
