
由國際標準組織 **ISO (International Stardard Organization)** 訂出的開放系統交互連結標準 **OSI (Open System Interconnection)**。把網路的硬體跟軟體訂出七層標準，大家遵守共同標準才能互相溝通。

**網路七層**: 用 outlook 寫一封信給對方
![[網路七層.png|550]]
- TCP: 有保證(加序號、加檢查位元、加 ack、控制資料流)、速度慢
- UDP: 沒保證、速度快
**TCP/IP 模型**: 國際標準組織訂出網路七層的標準之後，TCP/IP 把它簡單化
![[TCPIP.png|550]]
- 應用層: HTTP (傳輸網頁)、FTP (傳檔案)、SMTP (傳送 Email)
- 傳輸層: 應用層用 HTTP ，傳輸層使用 TCP 80 port。應用層用 DNS 名稱解析，傳輸層走 UDP 53 port。
- 網路層: 在前面加上來源 IP 和目的 IP
- 連結層: 在前面加上來源 MAC 和目的 MAC，再交給實體網路線把封包送出去
### 使用固定 IP 或浮動 IP
---
##### 固定 IP
設定 IP 永遠不會變，當電腦需要讓別人可以連時。架一台伺服器如網站、File Server、Database Server 等
##### 浮動 IP
設定自動取得 IP 位址，只是一台員工的電腦，電腦只需要可以上網
### IP 路由
---
- Windows:
```shell
tracert www.pchome.com.tw
```
- Mac:
```shell
brew install mtr
```
```shell
sudo -s # mtr 需要 root 權限才能執行
```
```shell
mtr www.pchome.com.tw
```
- 範例圖: 到 pchome 中間經過了 8 個 Routers
![[tracer.png]]
