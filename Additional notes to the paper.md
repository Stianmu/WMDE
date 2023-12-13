# WMDE
## Details about the dataset  

We have applied WMDE in real-world cellular networks in China Mobile. Based on WMDE, integrating the Transformer-Informed Adjustment Decision Net (TADNet) and the Causal Adjustment Effect Evaluation Net (CAENet), we can support the operation staff in decision-making for RAN parameter adjustment.

Our dataset, collected by China Mobile in the Shanxi region, consists of genuine historical RAN parameter adjustments and network performance metrics. This dataset encompasses a period of two weeks, with data sampled at 15-minute intervals. It includes 42 types of features in the state attributes S, such as 
coverage scenarios’. The configuration parameters C in the dataset contain variables like ‘reference signal power’. The goal metrics G include critical performance indicators such as ‘uplink traffic’ and ‘downlink traffic’. Details are as follows.

| Indicator name | Indicator Chinese name | Indicator type |
|----------------|------------------------|----------------|
| Intra-Frequency Handover Out Success Between eNodeB | 同频切换出成功次数 | S |
| Inter-Frequency Handover Out Success Between eNodeB | 异频切换出成功次数 | S |
| Inter-eNodeB Handover Out Success | eNB间切换出成功次数 | S |
| Inter-eNodeB Handover Out Request | eNB间切换出请求次数 | S |
| Intra-eNodeB Handover Out Success | eNB内切换出成功次数 | S |
| Inter-eNodeB S1 Handover Out Request | eNB间S1切换出请求次数 | S |
| Inter-eNodeB S1 Handover Out Success | eNB间S1切换出成功次数 | S |
| Inter-eNodeB X2 Handover Out Request | eNB间X2切换出请求次数 | S |
| Inter-eNodeB X2 Handover Out Success | eNB间X2切换出成功次数 | S |
| Total Handover Out | 切换出总次数 | S |
| Handover Success QCI=1 | 切换成功次数(QCI=1) | S |
| Average RRC Connection | RRC连接平均数 | S |
| Maximum RRC Connection | RRC连接最大数 | S |
| Uplink PRB Average Utilization | 上行PRB平均利用率 | S |
| Downlink PRB Average Utilization | 下行PRB平均利用率 | S |
| PDCCH Channel CCE Utilization | PDCCH信道CCE占用率 | S |
| Wireless Connection Rate | 无线接通率 | S |
| E-RAB Establishment Success Rate | E-RAB建立成功率 | S |
| E-RAB Establishment Failure Count | E-RAB建立失败次数 | S |
| E-RAB Establishment Success Count | E-RAB建立成功数 | S |
| E-RAB Establishment Request Count | E-RAB建立请求数 | S |
| E-RAB Establishment Success Count QCI=1 | E-RAB建立成功数(QCI=1) | S |
| E-RAB Establishment Request Count QCI=1 | E-RAB建立请求数(QCI=1) | S |
| RRC Connection Establishment Request Count | RRC连接建立请求次数 | S |
| RRC Connection Re-establishment Request Count | RRC连接重建请求次数 | S |
| Initial Context Establishment Success Count | 初始上下文建立成功次数 | S |
| eNB Requested E-RAB Release Count | eNB请求释放的E-RAB数 | S |
| Wireless Interface Failure Caused E-RAB Establishment Failure Count | 无线接口进程失败原因导致的E-RAB建立失败数 | S |
| Handover Failed E-RAB Count | 切出失败的E-RAB数 | S |
| eNB Requested Context Release Count | eNB请求释放上下文数 | S |
| E-RAB Drop Rate QCI=1 Numerator | E-RAB掉线率(QCI=1)分子 | S |
| Small Cell ID | 小单元ID | S |
| Network System | 网络制式 | S |
| Center Frequency Channel Number | 中心载频信道号 | S |
| Coverage scenarios | 覆盖场景 | S |
| Antenna Height | 天线挂高 | S |
| Antenna Azimuth | 天线方位角 | S |
| Total Tilt Angle | 总下倾角 | S |
| PCI | PCI | S |
| Longitude | 经度 | S |
| Latitude | 纬度 | S |
| Is D Frequency | 是否D频 | S |
| Reference Signal Power | 参考信号功率 | C |
| Uplink Traffic MB | 上行流量(MB) | G |
| Downlink Traffic MB | 下行流量(MB) | G |

## Details about the experimental settings

In this configuration, the model uses an embedding dimension (embed_dim) of 128, three layers (n_layer), 16 attention head (n_head), and ReLU as the activation function (activation_function). A dropout rate of 0.1 (dropout) is applied to prevent overfitting. The batch size is set to 8 (batch_size). These settings are tailored for performance on the Nvidia RTX 4090 GPU, working with the Adam optimizer at a learning rate of 0.0001.
