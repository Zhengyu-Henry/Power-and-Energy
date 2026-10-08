# Week1

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
