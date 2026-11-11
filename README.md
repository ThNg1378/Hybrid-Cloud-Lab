<div align="center">

# ☁️ Hybrid-Cloud-Lab

**Enterprise-grade hybrid network. Secure, monitored, and identity-driven.**

🌐 [ Read more report (Updated)](#) · 🛡️ [System & Security Focus](#)

![Status: Active](https://img.shields.io/badge/Status-Active-success?style=flat-square) ![Topology: Hub-and-Spoke](https://img.shields.io/badge/Topology-Hub--and--Spoke-blue?style=flat-square) ![Cloud: Azure](https://img.shields.io/badge/Cloud-Azure_Entra_ID-0089D6?style=flat-square) ![License: MIT](https://img.shields.io/badge/License-MIT-gray?style=flat-square)

**VMware Workstation · MikroTik RouterOS · Windows Server · PRTG Monitor · Azure**

</div>

---

### 🚀 Nhanh gọn. Bảo mật. Trực quan.
Mô phỏng kiến trúc mạng doanh nghiệp thực tế, giải quyết bài toán đa chi nhánh (Multi-site) với tiêu chuẩn bảo mật Zero Trust.

Virtualization network architect in real coporation, to solve the multi-site networking challenge base on the  Zero Trust Architecture.

| 🔒 Zero Trust IAM | 🛡️ Site-to-Site VPN | 🚦 Traffic Control | 📈 Deep Visibility |
| :--- | :--- | :--- | :--- |
| **Azure SSO & MFA**<br>Identify access management, prevent data leakage. | **IPsec Tunnel**<br>Encrypt all data in transit between HQ and Branches. | **VLAN Segmentation**<br>Isolate Guest, Staff, and Management networks. | **PRTG Network**<br>Monitor uptime, bandwidth and system health 24/7. |

<div align="center">
  <br>
  <i>(Sơ đồ kiến trúc tổng thể mạng Hub-and-Spoke)</i>
  <br><br>
  <b>[ 🖼️ CHÈN SƠ ĐỒ MẠNG DRAW.IO CỦA BẠN VÀO ĐÂY ]</b>
  <br><br>
</div>

---

### ⚡ Tại sao lại chọn kiến trúc này?
*Kiến trúc mạng truyền thống SMB vs Hybrid-Cloud-Lab:*

| Tiêu chí | Mạng Doanh nghiệp Truyền thống | Hybrid-Cloud-Lab |
| :--- | :--- | :--- |
| **Bảo mật truy cập (IAM)** | Mật khẩu nội bộ, dễ bị tấn công Brute-force | **Azure Entra ID (MFA & SSO)** |
| **Kết nối chi nhánh** | NAT Port ra Public, không mã hóa (Rủi ro MitM) | **IPsec VPN Tunnel** mã hóa 256-bit |
| **Cô lập mạng (Isolation)** | Dùng chung 1 dải IP mạng phẳng (Flat Network) | Phân mảnh **VLAN 10, 20, 30** nghiêm ngặt |
| **Giám sát hệ thống** | Đợi user báo lỗi mạng mới bắt đầu xử lý | **PRTG Core Probe** cảnh báo chủ động |
| **Khả năng mở rộng** | Chắp vá, khó quản lý tập trung | **Chuẩn Enterprise**, sẵn sàng tích hợp IDS/IPS |

---

### 🖼️ Bộ sưu tập (Screenshots)
*(Dự án thực chiến phải có minh chứng. Hãy chèn các hình ảnh thực tế của bạn vào đây)*

* 🛡️ **Azure MFA Login:** Giao diện bắt buộc nhập mã Authenticator khi đăng nhập. `[Chèn hình]`
* 🔒 **IPsec Tunnel Established:** Trạng thái mã hóa kết nối giữa 2 Router trên Winbox. `[Chèn hình]`
* 📊 **PRTG Dashboard:** Giao diện xanh/đỏ giám sát Traffic VLAN và Ping. `[Chèn hình]`
* 🌐 **VLAN Routing:** Bảng định tuyến nội bộ tại HQ. `[Chèn hình]`

---

### ✨ Hệ thống này hoạt động như thế nào? (What it does)
Dự án không chỉ là cài đặt phần mềm, mà là sự phối hợp của chuỗi công nghệ:
* **Định tuyến & Chuyển mạch:** Sử dụng MikroTik làm Core Router, cấu hình Trunking và Access Port để chia các VLAN nội bộ. Luồng dữ liệu của các phòng ban bị cô lập hoàn toàn.
* **Kết nối từ xa (Remote Branch):** Thay vì thuê đường truyền riêng (Leased-line) đắt đỏ, hệ thống dùng Internet công cộng nhưng thiết lập đường hầm **IPsec VPN** để nối mạng Chi nhánh vào Trụ sở chính như một mạng LAN nội bộ.
* **Đồng bộ Đám mây (Cloud Sync):** Máy chủ Active Directory (Windows Server) dưới local được đồng bộ lên **Azure Cloud**. Người dùng chỉ cần 1 tài khoản duy nhất (SSO) để truy cập mọi dịch vụ và bắt buộc phải dùng **MFA** khi ở ngoài công ty.
* **Giám sát chủ động:** PRTG Network Monitor liên tục quét (ping, SNMP) thiết bị mạng. Đảm bảo ống VPN luôn thông suốt và băng thông không bị nghẽn.

---

### 👨‍💻 Dành cho Kỹ sư & Nhà tuyển dụng (Repository Layout)
Cấu trúc kho lưu trữ được quy hoạch theo chuẩn **Documentation-as-Code** giúp bất kỳ ai cũng có thể hiểu và tái tạo lại Lab.

| Thư mục / Thành phần | Chức năng (What it is) |
| :--- | :--- |
| `docs/` | Chứa tài liệu thiết kế: Bảng quy hoạch IP, VLAN và file gốc sơ đồ kiến trúc mạng. |
| `01-network-infrastructure/` | Các script/file export cấu hình (`.rsc`) của Router MikroTik (VLAN, NAT, Firewall). |
| `02-ipsec-vpn/` | Hướng dẫn và cấu hình tạo đường hầm mã hóa Site-to-Site giữa HQ và Branch. |
| `03-identity-and-cloud/` | Cấu hình Active Directory và các Policy đồng bộ lên Azure Entra ID (MFA, SSO). |
| `04-monitoring/` | File xuất danh sách các Sensor giám sát từ PRTG Core Probe. |

---
*Được thiết kế và triển khai bởi **Nguyễn Hoàng Thanh Thiên** - Sinh viên ATTT định hướng System / Network & Security.*