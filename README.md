# Analog Graphic Equalizer | 模拟图示均衡器

[English](#english) · [简体中文](#简体中文) · [Simulation guide / 仿真指南](docs/simulation.md)

## English

Three- and seven-band graphic equalizers built from op-amp and active RC stages. Parallel low-pass, band-pass and high-pass paths separate the input spectrum. Individual gain stages adjust the contribution of each branch before the signals are summed.

## 简体中文

基于运放与有源 RC 滤波器搭建三段及七段图示均衡器。并联低通、带通和高通支路分离输入信号的频段，各支路经独立增益控制后再求和。

| Design / 设计 | Editable circuit / 可编辑电路 | Saved evidence / 已存结果 |
| --- | --- | --- |
| Three-band / 三段 | [Multisim 14](Simu_File/Equalizer_3band.ms14) · [BOM / 元件清单](3band_equalizer_parts_list.csv) · [Reference schematic / 参考原理图](3band_equalizer_reference_schematic.svg) · [SPICE netlist / 网表](3band_equalizer_multisim_netlist.cir) | [AC sweep / 交流扫频](Img/3Band_AC_SWEEP/3Band_AC_SWEEP_New.png) · [Breadboard prototype / 面包板原型](docs/three-band-breadboard.jpg) |
| Seven-band / 七段 | [Multisim 14](Simu_File/Equalizer_7band.ms14) | [AC sweep / 交流扫频](Img/7Band_AC_SWEEP/7Band_AC_SWEEP.png) |

![Saved three-band Multisim AC sweep / 三段均衡器 Multisim 交流扫频存档](Img/3Band_AC_SWEEP/3Band_AC_SWEEP_New.png)

LTspice completed the AC sweep of the separate ideal-op-amp reference netlist. The screenshot above is from the archived Multisim run. See the [simulation guide](docs/simulation.md) for test settings and expected branch behaviour.

独立的理想运放参考网表已在 LTspice 中跑通交流扫频。上图来自原有 Multisim 仿真存档。测试设置及各支路的预期响应见[仿真指南](docs/simulation.md)。
