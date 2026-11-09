---
title: "Hồ sơ Đối thủ: ISOFH — Mô hình Tích hợp Bệnh án Điện tử EMR, VNeID & Chữ ký số PKI"
vendor: "Công ty Cổ phần Công nghệ ISOFH"
product: "Hệ thống Bệnh án điện tử ISOFH EMR tích hợp nền tảng định danh VNeID & Chữ ký số"
signing_method: "Chữ ký số PKI cá nhân tích hợp luồng xác thực và phê duyệt qua ứng dụng VNeID"
tt13_category: "Nhóm 1: Chữ ký điện tử hợp pháp (khi sử dụng chứng thư số cá nhân đăng ký qua VNeID)"
role: "Nhà phát triển giải pháp phần mềm Y tế (HIS/EMR) & Đơn vị tích hợp quy trình lâm sàng"
last_updated: "2026-11-09"
verification_status: "Đã xác minh triển khai thí điểm tại BV Đa khoa Xanh Pôn; Chưa xác minh áp dụng đại trà toàn quốc"
---

# Hồ sơ Đối thủ: ISOFH — Mô hình Tích hợp Bệnh án Điện tử EMR, VNeID & Chữ ký số PKI

---

## 1. Thông tin Doanh nghiệp & Phân định Vai trò Đối tác

### 1.1 Thông tin Pháp nhân
- **Tên doanh nghiệp:** Công ty Cổ phần Công nghệ ISOFH `[Đã xác minh]`.
- **Sản phẩm cốt lõi:** Hệ thống Quản lý Bệnh viện (HIS), Bệnh án điện tử (EMR), Quản lý Xét nghiệm (LIS), Lưu trữ và Truyền tải Hình ảnh (PACS) `[Đã xác minh]`.
- **Bản chất vai trò:** ISOFH là **Nhà phát triển phần mềm y tế lâm sàng và Đơn vị tích hợp quy trình (System Integrator)**; ISOFH **không phải là Tổ chức cung cấp dịch vụ chứng thực chữ ký số công cộng (CA)** `[Đã xác minh]`.

### 1.2 Phân định Rõ ràng 4 Chủ thể trong Mô hình Triển khai tại Bệnh viện Xanh Pôn
Để hiểu đúng bản chất pháp lý và kỹ thuật, không được gộp chung các chủ thể thành một khái niệm duy nhất:
1. **Bệnh viện Đa khoa Xanh Pôn (Chủ thể sử dụng & Kiểm soát dữ liệu):** Đơn vị tổ chức quy trình khám chữa bệnh, ban hành quy chế sử dụng bệnh án điện tử và chịu trách nhiệm pháp lý cao nhất về hồ sơ bệnh án.
2. **ISOFH (Đơn vị phát triển phần mềm & Tích hợp quy trình):** Cung cấp hệ thống phần mềm HIS/EMR, xây dựng luồng giao diện lâm sàng để bác sĩ tạo phiếu và nhận kết quả phản hồi trạng thái ký.
3. **VNeID — Cục C06 Bộ Công An (Nền tảng Định danh & Xác thực Điện tử Quốc gia):** Đóng vai trò là kênh định danh, xác thực người dùng và gửi thông báo tương tác (Push Notification) đến thiết bị di động của công dân. *Lưu ý: VNeID không phải là CA cấp chứng thư số công cộng*.
4. **VNPT SmartCA hoặc CA công cộng hợp tác (Tổ chức cung cấp dịch vụ tin cậy):** Đơn vị trực tiếp cấp chứng thư số cá nhân cho người bệnh (người bệnh thực hiện đăng ký/liên kết chứng thư số thông qua ứng dụng VNeID hoặc cổng dịch vụ công) và vận hành hệ thống ký số từ xa (Remote Signing).

---

## 2. Sản phẩm & Cơ chế Công nghệ Thực tế

### 2.1 Phân loại Chính xác theo Thông tư 13/2025/TT-BYT
- **Không được mặc định xếp giải pháp VNeID tại Xanh Pôn vào Nhóm 3:**
  - Nếu quy trình thực tế người bệnh chỉ mở app VNeID bấm "Đồng ý" để xác nhận một giao dịch hành chính mà không sinh khóa mật mã: Đó là hình thức xác nhận điện tử thuộc **Nhóm 3**.
  - Tuy nhiên, trong mô hình thí điểm tại Bệnh viện Xanh Pôn, người bệnh thực hiện đăng ký chứng thư số cá nhân (được cung cấp bởi VNPT SmartCA hoặc CA công cộng liên kết qua VNeID), sau đó sử dụng khóa bí mật cá nhân để ký số vào hồ sơ bệnh án: **Đây là mô hình Chữ ký số PKI thuộc Nhóm 1 (Chữ ký điện tử hợp pháp)** có tích hợp VNeID làm kênh xác thực và phê duyệt giao dịch `[Nhận định kỹ thuật chuẩn xác]`.

### 2.2 Sơ đồ Luồng Ký số Bệnh nhân tại Bệnh viện Xanh Pôn

```
[Bệnh nhân đăng ký / liên kết Chứng thư chữ ký số cá nhân (VNPT SmartCA/CA) qua VNeID]
                                         │
                                         ▼
[Bác sĩ tạo phiếu phẫu thuật / bảng kê trên phần mềm ISOFH EMR]
                                         │
                                         ▼
[ISOFH EMR gửi yêu cầu ký tài liệu kèm mã định danh của bệnh nhân sang cổng VNeID]
                                         │
                                         ▼
[Ứng dụng VNeID trên smartphone của bệnh nhân nhận thông báo đẩy (Push Notification)]
                                         │
                                         ▼
[Bệnh nhân mở VNeID, xác thực sinh trắc học khuôn mặt/vân tay trên thiết bị để xem tài liệu]
                                         │
                                         ▼
[Bệnh nhân bấm "Xác nhận ký" và nhập mã PIN / Passcode bảo mật trên ứng dụng]
                                         │
                                         ▼
[Yêu cầu phê duyệt được gửi tới hệ thống HSM của Nhà cấp CA (VNPT SmartCA/CA liên kết)]
                                         │
                                         ▼
[HSM kích hoạt khóa bí mật của Bệnh nhân để tạo Chữ ký số PKI trên tài liệu PDF]
                                         │
                                         ▼
[Hệ thống phản hồi trạng thái ký thành công về ISOFH EMR để lưu trữ vào hồ sơ bệnh án]
```

---

## 3. Căn cứ Pháp lý & Rà soát Tuân thủ

### 3.1 Căn cứ theo Luật Giao dịch điện tử 2023 & Thông tư 13/2025/TT-BYT
- **Phân nhóm Thông tư 13:** Thuộc **Nhóm 1: Sử dụng chữ ký điện tử hợp pháp** (khi sử dụng chứng thư số cá nhân của người bệnh).
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 8, Điều 11, Điều 22 và khoản 2 Điều 23).
  - Nghị định số 23/2025/NĐ-CP về chữ ký điện tử và dịch vụ tin cậy (Điều 36 về cấp chứng thư chữ ký số bằng phương tiện điện tử).
  - Quyết định số 06/QĐ-TTg của Thủ tướng Chính phủ (Đề án 06).
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ:**
  - Mô hình kết hợp này đạt **độ tin cậy chứng minh rất cao**: Danh tính người bệnh được bảo đảm bởi Cơ sở dữ liệu quốc gia về dân cư (VNeID); chữ ký trên văn bản là chữ ký số PKI được bảo đảm bởi CA công cộng được cấp phép; tính toàn vẹn tài liệu được bảo đảm bằng hàm băm mật mã.

### 3.2 Tuân thủ Pháp luật về Bảo vệ Dữ liệu Cá nhân
- **Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP:**
  - Việc luân chuyển thông tin y tế (Điều 26) qua nền tảng trung gian VNeID đòi hỏi quy định phân định trách nhiệm rất nghiêm ngặt giữa Bệnh viện, đơn vị phát triển phần mềm ISOFH và cơ quan quản lý nền tảng.
  - Phải bảo đảm nguyên tắc thu nhỏ dữ liệu (Data Minimization): Cổng kết nối VNeID chỉ tiếp nhận thông tin yêu cầu xác nhận và tóm tắt giao dịch, không được truyền tải toàn bộ dữ liệu bệnh án chi tiết nếu không có sự đồng ý cụ thể của người bệnh.

---

## 4. Khách hàng & Triển khai Thực tế: Dữ liệu Xác minh

| Cơ sở Y tế | Quy mô & Phạm vi Công bố | Thời điểm & Nguồn xác minh | Đánh giá Hiện trạng Vận hành Thực tế |
|---|---|---|---|
| **Bệnh viện Đa khoa Xanh Pôn (Hà Nội)** | Công bố áp dụng ký số người bệnh qua VNeID cho 100% bệnh nhân nội trú và thí điểm tại 03 phòng khám ngoại trú. | Tháng 11/2023 – 2024. Nguồn: Cổng TTĐT Bộ Y tế, Báo Điện tử Chính phủ, VTV1, Báo Hà Nội Mới `[Đã xác minh thông tin công bố]` | `[Đã xác minh]` Có triển khai thí điểm thực tế; tuy nhiên tỷ lệ người bệnh tự thực hiện ký thành công trên tổng lưu lượng khám ngoại trú hàng ngày vẫn cần theo dõi số liệu thực tế do rào cản thiết bị của người dân. |
| **Bệnh viện Đa khoa Nông nghiệp** | Thí điểm các tiện ích liên kết sổ sức khỏe điện tử và định danh điện tử theo Đề án 06. | Năm 2024. Nguồn: Bản tin ngành y tế `[Có nguồn tham khảo]` | `[Có nguồn công bố nhưng chưa xác minh phạm vi toàn diện]` |

> *Lưu ý nghiên cứu:* Không được lấy trường hợp điển hình tại Bệnh viện Xanh Pôn để suy diễn rằng toàn bộ các bệnh viện công lập tại Việt Nam đều đang vận hành mô hình này. Phần lớn các cơ sở y tế khác mới ở giai đoạn tìm hiểu hoặc triển khai từng phần do phụ thuộc vào sự sẵn sàng của hạ tầng Đề án 06.

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của Mô hình ISOFH + VNeID + SmartCA
- **Lợi thế truyền thông và chỉ đạo chuyển đổi số:** Được các cơ quan quản lý nhà nước (Bộ Y tế, Bộ Công An, UBND các tỉnh) bảo trợ và ưu tiên truyền thông như một mô hình mẫu của Đề án 06.
- **Tiết kiệm chi phí đầu tư thiết bị tại viện:** Tận dụng smartphone cá nhân của người bệnh, bệnh viện không phải mua sắm hàng loạt đầu đọc thẻ chuyên dụng tại các khoa điều trị.
- **Tích hợp sâu trong quy trình EMR:** Do ISOFH trực tiếp phát triển phần mềm bệnh án điện tử nên việc kích hoạt lệnh ký từ hồ sơ bệnh án diễn ra rất đồng bộ.

### 5.2 Điểm yếu & Rào cản Lâm sàng
1. **Rào cản thiết bị & kỹ năng số của người bệnh:** Bắt buộc người bệnh phải có: (1) Smartphone có kết nối 4G/Wifi, (2) Đã cài đặt VNeID và kích hoạt tài khoản Mức 2, (3) Đã liên kết hoặc đăng ký dịch vụ chứng thư số cá nhân, (4) Nhớ mật khẩu đăng nhập và Passcode. Đối với nhóm bệnh nhân lớn tuổi, người bệnh nặng, người có hoàn cảnh khó khăn hoặc trường hợp cấp cứu, tỷ lệ tự thao tác thành công là một thách thức lớn trong thực tế vận hành.
2. **Phụ thuộc đường truyền và tính sẵn sàng của hệ thống mạng:** Quy trình phụ thuộc vào độ ổn định của nhiều tầng dịch vụ (Internet viện, mạng viễn thông của người bệnh, máy chủ VNeID, hệ thống CA từ xa).
3. **Tính đóng kín giải pháp:** ISOFH phát triển mô hình này tối ưu hóa riêng cho hệ thống EMR của ISOFH; các bệnh viện đang dùng phần mềm HIS/EMR của các hãng khác rất khó áp dụng nếu không có sự hợp tác kỹ thuật giữa các đối thủ phần mềm với nhau.

### 5.3 Bài học & Cơ hội Chiến lược cho EasyCA
- **Không phủ nhận mô hình VNeID:** EasyCA cần nhìn nhận VNeID là một kênh định danh và xác thực xuất sắc của Nhà nước.
- **Chiến lược Đa kênh của EasyCA:** EasyCA cần xây dựng giải pháp ký số PKI hỗ trợ đa dạng phương thức kích hoạt:
  - Nếu bệnh nhân có VNeID và smartphone: Cho phép xác thực qua VNeID để ký số EasyCA.
  - Nếu bệnh nhân là người cao tuổi, không có smartphone: Hỗ trợ luồng eKYC qua thẻ CCCD gắn chip tại quầy tiếp đón hoặc thiết bị cầm tay của điều dưỡng.
  - Nếu người nhà ở xa: Cung cấp luồng ký số từ xa qua liên kết web an toàn.
  - Điều này giúp Bệnh viện đạt tỷ lệ ký số thành công tiệm cận 100% đối tượng người bệnh mà không bị gián đoạn quy trình khám chữa bệnh.

---

## 6. Nguồn Tham khảo & Bằng chứng Xác thực
1. Cổng thông tin điện tử Bộ Y tế (`moh.gov.vn`) — Bài viết: "Bệnh viện Đa khoa Xanh Pôn tiên phong ứng dụng chữ ký số cho người bệnh qua VNeID".
2. Báo Điện tử Chính phủ (`baochinhphu.vn`) — Chuyên đề triển khai Đề án 06 tại Thủ đô Hà Nội.
3. Bản tin Thời sự Đài Truyền hình Việt Nam (VTV1) — Phóng sự Bệnh án điện tử không giấy tờ tại BV Xanh Pôn.
4. Website chính thức Công ty CP Công nghệ ISOFH: `isofh.com`.
5. Luật Giao dịch điện tử số 20/2023/QH15 và Nghị định số 23/2025/NĐ-CP.
6. Luật Bảo vệ dữ liệu cá nhân số 91/2025/QH15 và Nghị định số 356/2025/NĐ-CP.
