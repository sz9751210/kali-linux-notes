# wireshark

- 用途：收取網路流向，網路分析工具，可將網路封包攔截記錄下來並進行分析，主要用於網路故障排除，通信協議開發，數據包分析

## 安裝
* 環境：CentOS 7
```shell
sudo yum install libpcap

sudo yum install tcpdump

sudo yum install wireshark

sudo usermod -a -G wireshark $(whoami) 
```

## 語法

```shell
tshark [OPTIONS]
```
## 格式

| Packet number | Time| Source | Destination | Protocol | Info |
| ---- | ---- | ---- | ---- | ---- | ---- |
|      |      |      |      |      |      |


## 參數

| 參數 | 說明 |
| ---- | ---- |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
|      |      |
## 基本操作

1. 列出網卡
```shell
tshark -D
```

2. 指定網卡收封包，並存到檔案(test.pcap)
```shell
tshark -i 3 -w test.pcap
```

3. 指定網卡收封包，並存成log檔
```shell
tshark -i 3 > test.log
```

4. 指定port收封包
```shell
tshark -i 3 -f "port 443"
```
5. 指定網卡收封包，時間為10分鐘
```shell
tshark -i 3 -a duration:600
```

6. 指定網卡收10000個封包
```shell
tshark -c 10000 -i 3
```

7. 指定網卡收指定協議的封包
```shell
tshark -i 3 -f "tcp"
```

## 參考資料
https://www.wireshark.org/docs/man-pages/tshark.html

https://www.wireshark.org/docs/dfref/

## 相關指令(可選)
