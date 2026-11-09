---
title: "ISOFH — Giải pháp Ký Xác nhận Bệnh nhân qua Ứng dụng VNeID"
vendor: "Công ty Cổ phần Công nghệ ISOFH"
product: "Hệ thống Bệnh án điện tử ISOFH EMR tích hợp VNeID"
signing_method: "Xác nhận giao dịch điện tử qua ứng dụng VNeID (Push Notification)"
tt13_category: "Nhóm 3: Phương tiện điện tử khác theo Khoản 4 Điều 22 Luật GDĐT"
role: "Nhà phát triển phần mềm Y tế (HIS/EMR) & Đơn vị tích hợp giải pháp"
last_updated: "2026-11-09"
---

# ISOFH — Giải pháp Ký Xác nhận Bệnh nhân qua Ứng dụng VNeID

---

## 1. Thông tin Doanh nghiệp & Vị thế
- **Tên pháp nhân:** Công ty Cổ phần Công nghệ ISOFH `[Đã xác minh]`.
- **Sản phẩm:** Hệ thống Quản lý Bệnh viện (HIS), Bệnh án điện tử (EMR), Quản lý Thông tin Xét nghiệm (LIS), Lưu trữ và Truyền tải Hình ảnh (PACS) `[Đã xác minh]`.
- **Vai trò trong chuỗi cung ứng Y tế:** Nhà phát triển giải pháp phần mềm y tế lâm sàng hàng đầu; không phải là CA công cộng, đóng vai trò tích hợp cổng xác thực định danh điện tử vào quy trình quản lý bệnh viện `[Đã xác minh]`.
- **Đối tác liên quan:** Phối hợp cùng các đơn vị quản trị nền tảng định danh thuộc Đề án 06 (Cục C06 - Bộ Công An) và các cơ sở y tế thí điểm chuyển đổi số `[Đã xác minh]`.

---

## 2. Sản phẩm & Cơ chế Công nghệ

### 2.1 Phân định 4 Khái niệm Công nghệ liên quan đến VNeID
Trong giải pháp ứng dụng VNeID tại bệnh viện, cần phân biệt rõ 4 cấp độ kỹ thuật:
1. **Đăng nhập bằng VNeID (SSO):** Dùng tài khoản VNeID để đăng nhập vào Cổng thông tin/App của bệnh viện.
2. **Xác thực danh tính qua VNeID:** Đối soát thông tin hành chính của bệnh nhân với CSDL quốc gia về dân cư.
3. **Xác nhận giao dịch điện tử qua VNeID (Mô hình đang áp dụng):** Hệ thống EMR đẩy yêu cầu xác nhận một tài liệu cụ thể sang App VNeID của người bệnh; người bệnh mở app, xác thực sinh trắc/mã khóa để xác nhận chấp thuận nội dung.
4. **Chữ ký số tích hợp trong hệ thống định danh điện tử:** Sử dụng chứng thư số cá nhân được cấp và quản lý trong môi trường VNeID (theo Đề án 06) để ký số văn bản theo chuẩn PKI `[Đang trong quá trình hoàn thiện hạ tầng quốc gia]`.

### 2.2 Quy trình Vận hành Lâm sàng tại Bệnh viện (ISOFH EMR)

```
[Bác sĩ lập phiếu cam kết phẫu thuật / bảng kê trên ISOFH EMR]
                           │
                           ▼
1. Hệ thống ghi nhận số CCCD của bệnh nhân / người đại diện hợp pháp
                           │
                           ▼
2. ISOFH EMR gọi API gửi yêu cầu xác nhận sang nền tảng định danh VNeID
                           │
                           ▼
3. Ứng dụng VNeID trên điện thoại bệnh nhân nhận thông báo đẩy (Push Notification)
                           │
                           ▼
4. Bệnh nhân mở ứng dụng VNeID, xác thực mở khóa (FaceID/Vân tay)
   và xem nội dung văn bản đính kèm
                           │
                           ▼
5. Bệnh nhân bấm "Đồng ý", nhập Passcode của VNeID để xác nhận
                           │
                           ▼
6. Hệ thống VNeID phản hồi kết quả xác thực thành công (Callback API)
   ➔ ISOFH EMR ghi nhận trạng thái văn bản đã được người bệnh ký xác nhận
```

---

## 3. Căn cứ Pháp lý & Giá trị Chứng cứ

- **Phân nhóm theo Thông tư 13/2025/TT-BYT:** 
  - Thuộc **Nhóm 3: Sử dụng các hình thức xác nhận bằng phương tiện điện tử khác** theo quy định tại khoản 4 Điều 22 Luật Giao dịch điện tử số 20/2023/QH15 (thể hiện sự chấp thuận của chủ thể ký đối với thông điệp dữ liệu).
- **Căn cứ pháp lý áp dụng:**
  - Luật Giao dịch điện tử số 20/2023/QH15 (Điều 22 khoản 4).
  - Quyết định số 06/QĐ-TTg của Thủ tướng Chính phủ (Đề án 06 về phát triển ứng dụng dữ liệu dân cư).
  - Nghị định số 59/2022/NĐ-CP quy định về định danh và xác thực điện tử.
  - Thông tư số 13/2025/TT-BYT (Điều 3).
- **Đánh giá giá trị chứng cứ:**
  - Nhờ sử dụng tài khoản định danh điện tử Mức 2 (đã được Bộ Công An xác minh trực tiếp bằng sinh trắc học và CCCD gắn chip), **tính xác thực về danh tính chủ thể thực hiện là rất cao**.
  - *Lưu ý về bản chất:* Đây là hình thức "xác nhận điện tử" ghi nhận sự chấp thuận của người dùng trên nền tảng số của Nhà nước; về mặt kỹ thuật, nó khác với việc người bệnh trực tiếp nắm giữ một cặp khóa mật mã PKI độc lập ký vào tài liệu `[Nhận định chuyên môn]`.

---

## 4. Khách hàng & Triển khai Thực tế

| Cơ sở Y tế | Nội dung triển khai | Tình trạng | Nguồn xác minh |
|---|---|---|---|
| **Bệnh viện Đa khoa Xanh Pôn (Hà Nội)** | Triển khai mô hình bệnh nhân ký xác nhận hồ sơ bệnh án qua ứng dụng VNeID tích hợp phần mềm ISOFH EMR | Đã công bố triển khai chính thức | VTV1, Báo Điện tử Chính phủ, Cổng TTĐT Bộ Y tế `[Đã xác minh]` |
| **Bệnh viện Đa khoa Nông nghiệp** | Thí điểm các tiện ích định danh điện tử trong quản lý hồ sơ y tế | Thí điểm theo Đề án 06 | Báo chí ngành y tế `[Có nguồn tham khảo]` |

---

## 5. Đánh giá Cạnh tranh vs EasyCA

### 5.1 Điểm mạnh của ISOFH + VNeID
- **Ủng hộ chính sách mạnh mẽ:** Giải pháp bám sát mục tiêu của Đề án 06 Chính phủ, tạo động lực chính trị rất lớn để Ban Giám đốc các bệnh viện công lập ưu tiên áp dụng.
- **Tiết kiệm chi phí phần cứng:** Không bắt buộc bệnh viện phải đầu tư đầu đọc thẻ chuyên dụng tại từng giường bệnh hay quầy thủ tục (người bệnh tự sử dụng điện thoại cá nhân).
- **Tích hợp sâu trong EMR:** Vì ISOFH trực tiếp phát triển hệ thống EMR nên luồng trải nghiệm của bác sĩ khi gửi phiếu và nhận trạng thái ký rất mượt mà.

### 5.2 Điểm yếu & Hạn chế Vận hành
- **Rào cản thiết bị & nhóm người dùng yếu thế:** Bắt buộc người bệnh phải có: smartphone có kết nối mạng internet, đã cài đặt và kích hoạt tài khoản VNeID Mức 2, và nhớ mật khẩu/Passcode. Thực tế tại các cơ sở khám chữa bệnh công lập: tỷ lệ lớn người cao tuổi, trẻ em, người có hoàn cảnh khó khăn hoặc bệnh nhân cấp cứu đột xuất không đáp ứng đủ các điều kiện này để tự ký.
- **Phụ thuộc tính sẵn sàng của hạ tầng mạng:** Bất kỳ sự cố gián đoạn nào về đường truyền viễn thông hoặc bảo trì hệ thống máy chủ xác thực đều có thể làm chậm quy trình giải quyết thủ tục khám chữa bệnh.
- **Tính đóng kín hệ sinh thái:** Giải pháp hiện gắn chặt với phần mềm EMR của ISOFH; các bệnh viện đang vận hành HIS/EMR của đơn vị khác (VNPT, Viettel, FPT) sẽ gặp rào cản lớn về chi phí và thời gian nếu muốn tích hợp luồng tương tự.

---

## 6. Nguồn Tham khảo
1. Cổng thông tin điện tử Bộ Y tế — Thông tin về triển khai ký số người bệnh tại BV Đa khoa Xanh Pôn.
2. Báo Điện tử Chính phủ (baochinhphu.vn) — Chuyên đề triển khai Đề án 06 trong lĩnh vực y tế.
3. Bản tin Thời sự Đài Truyền hình Việt Nam (VTV1) — Phóng sự chuyển đổi số hồ sơ bệnh án tại Hà Nội.
4. Website chính thức Công ty CP Công nghệ ISOFH: `isofh.com`.
5. Nghị định số 59/2022/NĐ-CP quy định về định danh và xác thực điện tử.
