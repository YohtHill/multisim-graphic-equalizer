# Equalizer Simulation Guide | 均衡器仿真指南

## Frequency bands | 频段划分

These are design breakpoints for the branch filters. Check the combined response in the actual circuit.

下表为各支路滤波器的设计分频点，合成响应以实际电路的仿真结果为准。

| Design / 设计 | Nominal bands / 标称频段 |
| --- | --- |
| Three-band / 三段 | <340 Hz, 340 Hz–3.4 kHz, >3.4 kHz |
| Seven-band / 七段 | <100 Hz, 100–250 Hz, 250–630 Hz, 630 Hz–1.6 kHz, 1.6–4 kHz, 4–10 kHz, >10 kHz |

## Reproduce | 复现

1. Open the desired .ms14 in NI Multisim 14. Use the configured supply rails and check the input AC magnitude. / 在 NI Multisim 14 中打开对应的 .ms14 工程，使用工程中的电源设置并检查输入源的交流幅值。
2. Run **AC Analysis** with a 1 V AC input, decade sweep from 10 Hz to 100 kHz and 100 points per decade. Select the branch outputs and the final summing-stage output separately. / 将交流输入设为 1 V，按十倍频程从 10 Hz 扫至 100 kHz，每十倍频程 100 点。分别观察各频段输出及最终求和输出。
3. In the three-band circuit, try 100 Hz, 1 kHz and 10 kHz. Bass, mid and treble should dominate respectively. If the waveform clips, reduce the input amplitude. / 三段电路可分别输入 100 Hz、1 kHz 和 10 kHz，预期依次由低、中、高频支路主导。若波形削顶，降低输入幅值。

## SPICE reference | SPICE 参考模型

The [three-band netlist](../3band_equalizer_multisim_netlist.cir) uses ideal controlled-source op-amps. Run its included AC directive in LTspice and probe BASS_OUT, MID_OUT, TREBLE_OUT and AUDIO_OUT. LTspice may warn about the unused rail nodes or the .PRINT directive. The AC output was generated successfully.

[三段参考网表](../3band_equalizer_multisim_netlist.cir)以受控源实现理想运放。可在 LTspice 中运行自带的交流分析指令并查看 BASS_OUT、MID_OUT、TREBLE_OUT 与 AUDIO_OUT。LTspice 可能提示电源节点未参与模型或 .PRINT 指令不适用，交流数据已成功生成。
