## 文件说明

| 文件 | 说明 | 特征数 |
|---|---|---|
| `network_flow_features_single_flow.csv` | 单条流可提取的特征 | 507 |
| `network_flow_features_multi_flow.csv` | 多流汇聚特征 | 27 |

## single_flow 配置参数

### total_packets/... 根据前N包计算，默认5000, 模拟整个流，同packet_length_seq 序列长度L，同l2l3l4pl_iat
### active_time/idle_time 时间间隔t，默认1ms
### first_n_packets_length_mean/std/... 的前n包的n，默认10
### window_packet_count_mean/std/... 的window时间值t，默认1s
### instant_bitrate_mean/std/... 时间间隔t，默认100ms
### avg_burst_duration burst的判断阈值，包时间间隔，默认1ms
### small_packet_ratio 阈值，默认64B，同 top_1_bigram_SS_freq/... S M L 阈值，64B/1200B
### large_packet_ratio 阈值，默认1200B
### fft 的 TOP K 
### ar_prediction_mse AR模型阶数（可配置）？
### dl_chunk_seq/uplink_rate_seq 到流结束

## multi_flow 配置参数 
### short_connection_ratio