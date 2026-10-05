# CCNA Routing and Switching

**Cisco**

*Đặc biệt cảm ơn: Mr. Raj Bhanushali (CCNA Trainer)*

---

## MỤC LỤC

- CƠ BẢN VỀ MẠNG (BASICS OF NETWORKING)  
- ĐỊA CHỈ IP (IP ADDRESSING)  
- CẤU HÌNH ROUTER (ROUTER CONFIGURATION)  
- ĐỊNH TUYẾN IP (IP ROUTING)  
- CHUYỂN MẠCH (SWITCHING)  
- DANH SÁCH ĐIỀU KHIỂN TRUY CẬP (ACCESS CONTROL LIST \- ACL)  
- QUẢN LÝ IOS (IOS MANAGEMENT)  
- MẠNG DIỆN RỘNG (WAN)  
- IPv6

---

## CƠ BẢN VỀ MẠNG (BASICS OF NETWORKING)

### Mạng (Networking) là gì?

Networking là sự kết nối của 2 hay nhiều thiết bị CÓ CÙNG DẢI ĐỊA CHỈ IP DƯỚI MỘT GIAO THỨC (PROTOCOL) CHUNG.

**Các loại mạng:**

- **LAN \[Local Area Network \- Mạng cục bộ\]:** Một mạng máy tính bao phủ một khu vực tương đối nhỏ. Hầu hết LAN được giới hạn trong một căn phòng, tòa nhà hoặc cụm tòa nhà. Tuy nhiên, một LAN có thể kết nối với các LAN khác ở bất kỳ khoảng cách nào thông qua đường dây điện thoại hoặc sóng vô tuyến.  
- **MAN \[Metropolitan Area Network \- Mạng đô thị\]:** Một mạng kết nối người dùng với các tài nguyên máy tính trong một khu vực địa lý lớn hơn LAN nhưng nhỏ hơn WAN (ví dụ: trong phạm vi một thành phố).  
- **WAN \[Wide Area Network \- Mạng diện rộng\]:** Mạng máy tính bao phủ một khu vực địa lý rộng lớn. Thông thường, một WAN bao gồm hai hoặc nhiều LAN. Các máy tính kết nối với WAN thường thông qua mạng công cộng (như hệ thống viễn thông), đường truyền thuê bao (leased lines) hoặc vệ tinh.  
- **GAN \[Global Area Network \- Mạng toàn cầu\]:** Đề cập đến một mạng bao gồm nhiều mạng khác nhau kết nối với nhau, bao phủ một khu vực địa lý không giới hạn. Thuật ngữ này gần đồng nghĩa với Internet.

**CÁC MÔ HÌNH MẠNG (NETWORK TOPOLOGIES):**

- BUS  
- RING (Vòng)  
- STAR (Sao)  
- MESH (Lưới)  
- HYBRID (Lai)

#### Mô hình BUS

Topology dạng BUS là loại mạng mà mọi máy tính và thiết bị mạng đều được kết nối vào một trục cáp duy nhất (single cable).

**Đặc điểm của BUS Topology**

1. Dữ liệu chỉ truyền theo một hướng.  
2. Mọi thiết bị đều kết nối chung vào một cáp.

**Ưu điểm:**

1. Tiết kiệm chi phí.  
2. Cần ít cáp nhất so với các topology khác.  
3. Phù hợp cho các mạng nhỏ.  
4. Dễ hiểu, dễ thiết lập.  
5. Dễ dàng mở rộng bằng cách nối hai cáp lại với nhau.

**Nhược điểm:**

1. Nếu trục cáp chính đứt, toàn bộ mạng sẽ sập.  
2. Khi lưu lượng mạng (network traffic) lớn hoặc có nhiều Node (điểm nút), hiệu suất mạng sẽ giảm.  
3. Chiều dài cáp bị giới hạn.  
4. Tốc độ chậm hơn so với mô hình Ring.

#### Mô hình RING (Vòng)

Được gọi là mạng vòng vì mỗi máy tính được kết nối với một máy tính khác, và máy tính cuối cùng kết nối vòng lại với máy tính đầu tiên, tạo thành một vòng khép kín. Mỗi thiết bị có chính xác hai thiết bị lân cận.

**Đặc điểm:**

1. Sử dụng một số bộ lặp (repeaters) và luồng truyền dữ liệu là một chiều (unidirectional).  
2. Dữ liệu được truyền tuần tự theo từng bit.

**Ưu điểm:**

1. Không bị ảnh hưởng nhiều bởi lưu lượng truy cập cao hay khi thêm Node, vì chỉ Node nào giữ Token (thẻ bài) mới được truyền dữ liệu.  
2. Chi phí lắp đặt và mở rộng rẻ.

**Nhược điểm:**

1. Khắc phục sự cố (Troubleshooting) khó khăn.  
2. Việc thêm hoặc xóa máy tính sẽ làm gián đoạn hoạt động của mạng.  
3. Một máy tính hỏng có thể làm toàn bộ mạng ngừng hoạt động.

#### Mô hình STAR (Sao)

Tất cả các máy tính được kết nối với một thiết bị trung tâm (Hub/Switch) thông qua cáp. Hub đóng vai trò là Node trung tâm.

**Đặc điểm:**

1. Mỗi Node có một kết nối riêng biệt (dedicated connection) tới Hub.  
2. Hub hoạt động như một repeater cho luồng dữ liệu.  
3. Có thể dùng cáp xoắn đôi (twisted pair), cáp quang (Optical Fibre) hoặc cáp đồng trục (coaxial cable).

**Ưu điểm:**

1. Hiệu suất nhanh khi có ít Node và lưu lượng mạng thấp.  
2. Hub dễ dàng được nâng cấp.  
3. Dễ dàng khắc phục sự cố (Troubleshoot).  
4. Dễ dàng thiết lập và thay đổi cấu trúc.  
5. Nếu một Node bị hỏng, chỉ Node đó bị ảnh hưởng, các Node khác vẫn hoạt động bình thường.

**Nhược điểm:**

1. Chi phí lắp đặt cao.  
2. Đắt tiền hơn khi sử dụng (tốn nhiều cáp).  
3. Nếu Hub bị hỏng, toàn bộ mạng sẽ ngừng hoạt động.  
4. Hiệu suất phụ thuộc hoàn toàn vào năng lực của Hub/Switch.

#### Mô hình MESH (Lưới)

Là kiểu kết nối điểm-điểm (point-to-point) giữa các thiết bị. Traffic chỉ được truyền giữa hai thiết bị có kết nối trực tiếp với nhau. Mô hình Mesh đầy đủ có số lượng kết nối vật lý là `n(n-1)/2` đối với `n` thiết bị.

**Các loại Mesh Topology:**

1. **Partial Mesh (Lưới bán phần):** Một số hệ thống kết nối theo kiểu Mesh, nhưng một số thiết bị khác chỉ kết nối với hai hoặc ba thiết bị.  
2. **Full Mesh (Lưới toàn phần):** Tất cả các Node đều được kết nối trực tiếp với nhau.

**Ưu điểm:**

1. Mỗi kết nối có thể chịu tải dữ liệu riêng biệt.  
2. Mạng có độ bền bỉ (robust) rất cao.  
3. Dễ dàng chẩn đoán lỗi.  
4. Cung cấp tính bảo mật và riêng tư cao.

**Nhược điểm:**

1. Cài đặt và cấu hình phức tạp.  
2. Chi phí cáp mạng đắt đỏ.  
3. Cần số lượng dây cáp khổng lồ (Bulk wiring).

#### Mô hình HYBRID (Lai)

Là sự kết hợp của hai hay nhiều loại topologies khác nhau. Ví dụ: một phòng ban dùng Ring, phòng khác dùng Star; khi kết nối hai mạng này lại sẽ tạo thành Hybrid Topology.

**Ưu điểm:**

1. Đáng tin cậy, dễ dàng phát hiện lỗi và khắc phục sự cố.  
2. Hiệu quả cao.  
3. Khả năng mở rộng (Scalable) tốt.  
4. Linh hoạt (Flexible).

**Nhược điểm:**

1. Thiết kế phức tạp (Complex).  
2. Chi phí cao (Costly).

---

### Cáp và Kết nối (Cables and Connections)

#### Cáp xoắn đôi (Twisted Pair Cable)

Là loại cáp trong đó hai dây dẫn của một mạch được xoắn vào nhau nhằm triệt tiêu nhiễu điện từ (EMI) từ các nguồn bên ngoài và hiện tượng nhiễu chéo (crosstalk) giữa các cặp dây lân cận. Có 2 loại phổ biến là STP (Shielded \- có chống nhiễu) và UTP (Unshielded \- không chống nhiễu).

* **UTP:** Phổ biến, rẻ, linh hoạt, dùng nhiều trong văn phòng và gia đình. Nhược điểm là không có lớp bảo vệ chống nhiễu từ môi trường ngoài.  
* **STP:** Có thêm lớp vỏ bọc chống nhiễu. Thường dùng trong các môi trường ngoài trời hoặc công nghiệp yêu cầu băng thông (bandwidth) ổn định cao. Chi phí đắt hơn và cáp cứng hơn UTP.

#### Cáp thẳng (Straight Cable)

Được dùng để kết nối **các thiết bị khác loại**. Cụ thể:

1. Máy tính tới cổng thông thường của Switch/Hub.  
2. Máy tính tới cổng LAN của Modem cáp/DSL.  
3. Cổng WAN của Router tới cổng LAN của Modem.  
4. Cổng LAN của Router tới cổng Uplink của Switch/Hub.  
5. Kết nối 2 Switch/Hub (một đầu cắm cổng Uplink, một đầu cắm cổng thường).

#### Cáp chéo (Crossover Cable)

Được dùng để kết nối **các thiết bị cùng loại**. Cụ thể:

1. Kết nối trực tiếp 2 máy tính.  
2. Cổng LAN của Router kết nối với cổng thông thường của Switch/Hub.  
3. Kết nối 2 Switch/Hub (đều cắm vào cổng thông thường ở cả hai đầu).

#### Cáp Rollover (Cáp Console)

Còn gọi là cáp Cisco console. Đây là loại cáp null-modem thường dùng để kết nối terminal (máy tính) vào cổng Console của Router/Switch để cấu hình. Cáp thường có dạng dẹt và màu xanh nhạt.

| Chuẩn mạng (Specification) | Loại cáp (Cable Type) |
| :---- | :---- |
| 10BaseT | Cáp xoắn đôi không chống nhiễu (UTP) |
| 10Base2 | Cáp đồng trục mỏng (Thin Coaxial) |
| 10Base5 | Cáp đồng trục dày (Thick Coaxial) |
| 100BaseT | UTP |
| 100BaseFX | Cáp quang (Fiber Optic) |
| 100Base BX | Cáp quang đơn mode (Single mode Fiber) |
| 100Base SX | Cáp quang đa mode (Multimode Fiber) |
| 1000BaseT | UTP |
| 1000BaseFX | Cáp quang |

---

### MÔ HÌNH OSI (OSI MODEL)

Mô hình OSI phân chia hệ thống giao tiếp mạng thành 7 tầng (layer) trừu tượng để chuẩn hóa giao thức.

7. **Application (Ứng dụng):** Tầng cao nhất, cung cấp các dịch vụ mạng cho người dùng (Mail, web, thư mục).  
8. **Presentation (Trình diễn):** Dịch, mã hóa và định dạng dữ liệu để tầng Application có thể đọc được.  
9. **Session (Phiên):** Thiết lập, quản lý và đồng bộ hóa các phiên giao tiếp (conversation) giữa hai ứng dụng.  
10. **Transport (Giao vận):** Đảm bảo truyền tải dữ liệu một cách đáng tin cậy. Cắt dữ liệu thành các Segment nhỏ để truyền tải hiệu quả. Xử lý ghép kênh (multiplexing).  
11. **Network (Mạng):** Chịu trách nhiệm định tuyến (Routing). Quyết định đường đi tốt nhất cho dữ liệu (Packets). Đóng vai trò như bộ điều khiển mạng.  
12. **Data Link (Liên kết dữ liệu):** Nhóm các bit thành các Khung (Frames). Kiểm soát lỗi (Error control) trên đường truyền vật lý và phát hiện lỗi.  
13. **Physical (Vật lý):** Kích hoạt, duy trì và ngắt kết nối vật lý. Chuyển đổi các bit kỹ thuật số (0 và 1\) thành tín hiệu điện (hoặc quang/sóng vô tuyến) để truyền trên môi trường vật lý.

| TÊN TẦNG (LAYER) | GIAO THỨC (PROTOCOLS) | THIẾT BỊ ĐIỂN HÌNH (DEVICES) |
| :---- | :---- | :---- |
| Application, Presentation, Session (Layers 5-7) | Telnet, HTTP, FTP, SMTP, POP3, VoIP, SNMP | Firewall, IDS |
| Transport Layer (Layer 4\) | TCP, UDP |  |
| Network Layer (Layer 3\) | IP | ROUTER |
| Data Link Layer (Layer 2\) | Ethernet, HDLC, Frame Relay, PPP | SWITCHES, DSL Modem |
| Physical Layer (Layer 1\) | Ethernet | HUBS, Cáp mạng |

---

### TCP VÀ UDP LÀ GÌ?

Cả hai đều là giao thức Transport Layer, nhưng có mục đích sử dụng khác nhau:

| Transmission Control Protocol (TCP) | User Datagram Protocol (UDP) |
| :---- | :---- |
| **Hướng kết nối (Connection-oriented):** Đảm bảo dữ liệu được gửi đến đích trừ khi mất kết nối. | **Không hướng kết nối (Connectionless):** Gửi dữ liệu mà không cần biết đích có nhận được hay không. |
| **Đáng tin cậy (Reliable).** | **Không đáng tin cậy (Unreliable).** |
| Gửi xác nhận nhận (Acknowledgement). | Không gửi xác nhận (No acknowledgement). |
| Kích thước Header là 20 bytes. | Kích thước Header là 8 bytes. |
| Tốc độ chậm hơn UDP. | Tốc độ nhanh hơn vì không có cơ chế kiểm tra lỗi phức tạp. |
| Phù hợp cho ứng dụng cần tính toàn vẹn dữ liệu (Web, Email, File transfer). | Phù hợp cho ứng dụng cần truyền tải thời gian thực, tốc độ nhanh (Game online, VoIP, Video stream). |
| Có cơ chế kiểm soát luồng (Flow Control) và kiểm soát tắc nghẽn (Congestion control). | Không có kiểm soát luồng. |

* **DNS (Domain Name System):** Hệ thống phân giải tên miền, dịch tên website (dễ nhớ) thành địa chỉ IP (số).  
* **MAC Address (Địa chỉ MAC):** Còn gọi là địa chỉ vật lý, là định danh duy nhất được gán cho card mạng (NIC) để giao tiếp ở tầng Physical.  
* **Node (Điểm nút):** Một thiết bị kết nối vào mạng (máy tính, máy in,...).  
* **Gateway / Router:** Nút kết nối hai hay nhiều mạng lại với nhau, làm nhiệm vụ chuyển tiếp (forward) các gói tin giữa các mạng.

---

## ĐỊA CHỈ IP (IP ADDRESSING)

* **Address:** Địa chỉ IP định danh duy nhất cho một Host hoặc cổng (interface) trên mạng.  
* **Subnet (Mạng con):** Một phần của mạng chia sẻ chung một dải địa chỉ Subnet.  
* **Subnet mask (Mặt nạ mạng):** Một dải 32-bit dùng để xác định phần nào của địa chỉ IP là Mạng (Network) và phần nào là Máy chủ (Host).  
* **Interface:** Một cổng kết nối mạng (VD: cổng Ethernet trên Router).

**Subnet mask mặc định (Natural masks):**

* Lớp A (Class A): 255.0.0.0  
* Lớp B (Class B): 255.255.0.0  
* Lớp C (Class C): 255.255.255.0

| Class | Dải IP (1 Octet đầu) | Network Mask | Prefix | Số lượng mạng | Số lượng Hosts (Máy) |
| :---- | :---- | :---- | :---- | :---- | :---- |
| A | 1\. \- 127\. | 255.0.0.0 | /8 | 126 | 16,777,214 |
| B | 128\. \- 191\. | 255.255.0.0 | /16 | 16,382 | 65,534 |
| C | 192\. \- 223\. | 255.255.255.0 | /24 | 2,097,150 | 254 |
| D | 224\. \- 239\. |  |  | Dành cho Multicast |  |
| E | 240\. \- 254\. |  |  | Dành cho nghiên cứu |  |

**Dải IP Private (Nội bộ/Miễn phí):**

* Class A: 10.0.0.0 \- 10.255.255.255  
* Class B: 172.16.0.0 \- 172.31.255.255  
* Class C: 192.168.0.0 \- 192.168.255.255

### CHIA MẠNG CON (SUBNETTING)

Subnetting cho phép bạn tạo nhiều mạng logic nhỏ lẻ bên trong một dải mạng Class A, B hoặc C. **Ưu điểm:** Giảm traffic mạng (tăng hiệu suất), giới hạn các gói tin Broadcast, dễ quản lý và dễ chẩn đoán lỗi (Troubleshooting).

**Các loại Subnetting:**

* **FLSM \[Fixed Length Subnet Mask\]:** Subnet mask có độ dài cố định.  
* **VLSM \[Variable Length Subnet Mask\]:** "Chia mạng con của mạng con", cho phép chia IP thành các mạng con với nhiều kích thước khác nhau để tối ưu IP.

**Default gateways (Cổng mặc định):** Là địa chỉ IP của Router giúp các thiết bị trong một Subnet có thể giao tiếp với các mạng bên ngoài.

---

## CẤU HÌNH ROUTER (ROUTER CONFIGURATION)

**Router là gì?** Thiết bị kết nối các mạng khác nhau lại với nhau bằng các giao thức định tuyến (Routing protocols). Router giúp chia nhỏ các Broadcast Domain (vùng quảng bá) ở Layer 3\.

**Bộ nhớ của Router:**

* **ROM:** Bộ nhớ chỉ đọc, chứa hướng dẫn để chạy POST (Power-on Self Test).  
* **RAM:** Bộ nhớ tạm thời, mất dữ liệu khi tắt nguồn. Chứa Running-config, Routing tables (Bảng định tuyến).  
* **NVRAM:** Bộ nhớ cố định, chứa cấu hình khởi động (Startup-config).  
* **Flash:** Bộ nhớ cố định lưu trữ hệ điều hành (Cisco IOS image).

**Các chế độ cấu hình (Modes):**

* **Exec Mode (Chế độ người dùng):** Chế độ mặc định (`Router>`).  
* **Enable Mode (Chế độ đặc quyền):** `Router#en`  
* **Configuration Mode (Chế độ cấu hình toàn cục):** `Router#configure terminal` hoặc `conf t`

**Cấu hình cơ bản:**

\#hostname R1  (Đổi tên Router thành R1)

Gán IP cho cổng (Interface) fa0/0:

\#int fa0/0

\#ip add 10.0.0.1 255.0.0.0

\#no shut  (Bật cổng)

**Các lệnh kiểm tra/lưu cấu hình:**

* `# show running-config`: Xem cấu hình đang chạy (trên RAM).  
* `# show startup-config`: Xem cấu hình đã lưu (trên NVRAM).  
* `# copy running-config startup-config` (hoặc `# wr`): Lưu cấu hình.  
* `# show ip interface brief`: Xem tóm tắt thông tin các cổng và IP.  
* `# no ip domain lookup`: Ngăn Router tốn thời gian tìm kiếm DNS khi gõ sai lệnh.

---

## ĐỊNH TUYẾN IP (IP ROUTING)

Có 3 phương pháp định tuyến:

### 1\. Static Routing (Định tuyến tĩnh)

Quản trị viên phải cấu hình đường đi thủ công.

\#ip route 30.0.0.0 255.0.0.0 20.0.0.2

### 2\. Dynamic Routing (Định tuyến động)

Giao thức tự động học hỏi và xây dựng bảng định tuyến.

* **Distance Vector:** RIP, RIPv2, IGRP.  
* **Link State:** OSPF, IS-IS.  
* **Hybrid (Lai):** EIGRP.

**So sánh RIP và RIPv2:**

* **RIPv1:** Classful, Broadcast để cập nhật, không xác thực.  
* **RIPv2:** Classless (hỗ trợ VLSM), Multicast (224.0.0.9) để cập nhật, hỗ trợ xác thực.  
* **Điểm chung:** Metric dựa trên số bước nhảy (Hop count \- tối đa 15). Khoảng cách quản trị (AD) \= 120\.

Cấu hình RIPv2:

R1 (config) \# router rip

R1 (config) \# version 2

R1 (config) \# no auto-summary

R1 (config) \# network 10.0.0.0

### IGRP (INTERIOR GATEWAY ROUTING PROTOCOL)

* **Metric:** Bandwidth (Băng thông) \+ Delay (Độ trễ) \= Cost.  
* Độc quyền của Cisco (Cisco Proprietary). AD \= 100\.

### LINK STATE: OSPF (OPEN SHORTEST PATH FIRST)

* **Metric:** Cost (Phụ thuộc vào Bandwidth).  
* Sử dụng Multicast (224.0.0.5 & 224.0.0.6).  
* Duy trì 3 bảng: Neighbour table, Topology table, Routing table.  
* Giao thức Classless, ngăn lặp vòng (Loop free).  
* Thuật toán: Dijkstra (SPF). AD \= 110\.

Cấu hình OSPF:

R1 (config) \# router ospf 10

R1 (config) \# network 10.0.0.0 0.255.255.255 area 1

### HYBRID: EIGRP

* **Metric:** Bandwidth \+ Delay (+MTU+Reliability+Load).  
* Multicast 224.0.0.10.  
* Độc quyền Cisco (Cisco Proprietary). AD \= 90\.  
* Hỗ trợ cân bằng tải trên các đường không đều nhau (Unequal cost path load balancing).

Cấu hình EIGRP:

R1 (config) \# router eigrp 10

R1 (config) \# no auto-summary

R1 (config) \# network 10.0.0.0

**Bảng Administrative Distances (AD) mặc định:**

| Nguồn Route (Route Source) | Default Distance (AD) |
| :---- | :---- |
| Connected interface (Kết nối trực tiếp) | 0 |
| Static route (Tĩnh) | 1 |
| EIGRP summary route | 5 |
| External BGP | 20 |
| Internal EIGRP | 90 |
| IGRP | 100 |
| OSPF | 110 |
| RIP | 120 |

---

## CHUYỂN MẠCH (SWITCHING)

### Virtual LAN (VLAN)

Tạo VLAN để chia nhỏ Broadcast Domain (vùng quảng bá) ở Layer 3 trên Switch.

* Cơ sở dữ liệu VLAN lưu ở Flash (tên file: `vlan.dat`).  
* Dải VLAN: 1-1001 (Normal), 1002-1005 (Reserved), 1006-4096 (Extended).

Cấu hình tạo và gán VLAN vào cổng:

\#vlan 2

\#name Sales

\#exit

\#int fa 0/5

\#switchport mode access

\#switchport access vlan 2

### Trunking

Trunk dùng để kết nối giữa các Switch với nhau, cho phép nhiều VLAN đi qua.

* **Access Mode:** Chỉ cho 1 VLAN đi qua.  
* **Trunk Mode:** Cho phép traffic của nhiều VLAN đi qua.

Cấu hình cổng Trunk:

\#interface fastethernet 0/1

\#switchport mode trunk

\#switchport trunk encapsulation dot1q

### VLAN Trunking Protocol (V.T.P)

VTP giúp đồng bộ thông tin cấu hình VLAN giữa các Switch trong cùng một VTP Domain.

* **Các Mode:** Server (tạo/xóa/sửa VLAN), Client (chỉ nhận đồng bộ), Transparent (Cho phép cấu hình cục bộ, chuyển tiếp thông tin VTP nhưng không đồng bộ).

### Inter-VLAN'S (Router-on-a-stick)

Kỹ thuật cho phép các VLAN khác nhau giao tiếp với nhau bằng cách sử dụng 1 cổng vật lý trên Router chia thành nhiều cổng ảo (Sub-interfaces).

R1(config)\#interface fastethernet 0/0.2

R1(config-subif)\#encapsulation dot1q 2

R1(config-subif)\#ip address 10.0.0.1 255.0.0.0

### Spanning Tree Protocol (S.T.P)

Giao thức chống lặp vòng (loop-free) ở Layer 2\. Tự động block các cổng dự phòng để chống bão Broadcast (Broadcast storm).

* Trạng thái cổng (States): Blocking, Listening, Learning, Forwarding.

### Etherchannel (LACP / PAgP)

Công nghệ gộp nhiều cổng vật lý thành một cổng logic (Port-channel) để tăng băng thông và dự phòng.

* **PAgP:** Độc quyền Cisco.  
* **LACP:** Chuẩn mở IEEE (802.3ad). (Hay dùng trong cấu hình thực tế).

Cấu hình Etherchannel:

\#interface range fa0/1-2

\#channel-protocol pagp

\#channel-group 1 mode desirable

### First Hop Redundancy Protocol (F.H.R.P)

Dự phòng Gateway (cổng mặc định) cho thiết bị đầu cuối.

* **HSRP:** Cisco proprietary (Active/Standby).  
* **VRRP:** Open standard (Master/Backup).  
* **GLBP:** Cisco proprietary (Hỗ trợ Load balancing).

### Layer 2 Security (Port Security)

Giới hạn truy cập vào Switch dựa trên địa chỉ MAC.

* Các hành động vi phạm (Violation Modes): Shutdown (tắt cổng), Protect (bỏ qua gói tin không hợp lệ, không log), Restrict (bỏ qua, có log).

Cấu hình Port Security:

Switch(config)\#interface fa0/1

Switch(config-if)\#switchport mode access

Switch(config-if)\#switchport port-security

Switch(config-if)\#switchport port-security maximum 1

Switch(config-if)\#switchport port-security mac-address sticky

Switch(config-if)\#switchport port-security violation shutdown

---

## DANH SÁCH ĐIỀU KHIỂN TRUY CẬP (ACCESS CONTROL LIST \- ACL)

ACL dùng để lọc (filter) các luồng dữ liệu (traffic) đi vào hoặc đi ra khỏi một Interface.

1. **Standard ACL (1-99, 1300-1999):** Chỉ lọc dựa trên IP nguồn (Source IP). Nên đặt càng gần đích (Destination) càng tốt.  
2. **Extended ACL (100-199, 2000-2699):** Lọc dựa trên cả IP nguồn, IP đích, giao thức (Protocol) và Port. Nên đặt càng gần nguồn (Source) càng tốt.

Cấu hình Standard ACL:

Device(config)\# access-list 1 permit 172.16.5.22 0.0.0.0

Device(config)\# access-list 1 deny 172.16.7.34 0.0.0.0

Cấu hình Extended ACL:

Device(config)\# access-list 107 permit tcp any 172.69.0.0 0.0.255.255 eq telnet

Device(config)\# access-list 107 deny tcp any any

---

## QUẢN LÝ IOS (IOS MANAGEMENT)

Backup và Restore cấu hình qua máy chủ TFTP:

\#copy running-config tftp:

\#copy tftp: running-config

Backup IOS Image:

\#copy flash tftp:

Cấu hình mật khẩu (Passwords):

* Console Line (Cổng Console)  
* Aux Line  
* VTY Lines (Telnet/SSH)  
* Enable Password / Enable Secret (Được mã hóa)

Mã hóa tất cả password dạng text:

\#service password-encryption

---

## MẠNG DIỆN RỘNG (WAN)

WAN kết nối các mạng ở vùng địa lý rộng lớn, thường dùng đường truyền của các nhà cung cấp dịch vụ viễn thông (ISP).

**Các công nghệ WAN:**

1. **Dedicated (Đường truyền riêng/Leased-line):** HDLC, PPP.  
2. **Circuit Switching (Chuyển mạch kênh):** ISDN, PSDN.  
3. **Packet Switching (Chuyển mạch gói):** Frame Relay, ATM, X.25.

### Frame Relay

Công nghệ WAN chuyển mạch gói, sử dụng định danh DLCI (data-link connection identifiers) để xác định các kênh mạch ảo (Virtual Circuits).

Cấu hình Hub and Spoke (Static Mapping):

\#interface Serial0/0

\#encapsulation frame-relay

\#no frame-relay inverse arp

\#frame-relay map ip 20.0.0.2 102 broadcast

---

## IPv6 (Internet Protocol Version 6\)

Cải tiến lớn nhất là mở rộng không gian địa chỉ từ 32 bit (IPv4) lên 128 bit.

**Các tính năng nổi bật của IPv6:**

* Địa chỉ dài 128 bits (16 bytes).  
* Bắt buộc hỗ trợ IPSec (Bảo mật).  
* Sử dụng trường Flow Label để Router quản lý QoS tốt hơn.  
* Hỗ trợ tự động cấu hình (Auto-configuration), không bắt buộc phải có DHCP.  
* Không có địa chỉ Broadcast, sử dụng Multicast nhiều hơn.

| Thuộc tính | IPv4 | IPv6 |
| :---- | :---- | :---- |
| Kích thước | 32-bit | 128-bit |
| Phân giải MAC | Dùng ARP | Dùng thông điệp Multicast Neighbor Solicitation |
| Bảo mật | IPSec là tùy chọn | IPSec là bắt buộc |
| Cấu hình IP | Dùng DHCP | Có thể tự động cấu hình (Auto-configure) |

