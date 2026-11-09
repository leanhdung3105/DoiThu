---
title: "Mô hình Ký tay trên Tablet Cảm ứng (DentalFlow & HIS Phòng khám)"
vendor: "DentalFlow, BambuFit, Nanosoft, LinkCare và nhiều HIS nội bộ"
product: "Tính năng Ký cảm ứng trên iPad / Tablet / Wacom"
signing_method: "Vẽ chữ ký bằng tay/bút stylus trên màn hình cảm ứng"
tt13_category: "Hình thức 3 (Phương tiện điện tử khác — Cấp thấp nhất)"
legal_standing: "Rất yếu (Dễ bị Tòa án bác bỏ khi tranh chấp)"
target_hospital: "Bệnh viện tư, bệnh viện thẩm mỹ, chuỗi nha khoa & phòng khám"
deployments: "Chiếm tới 70-80% phòng khám tư nhân và nhiều khoa khám bệnh"
role: "Mô hình phổ biến nhất cần thuyết phục chuyển đổi sang PKI"
---

# Mô hình Ký tay trên Tablet Cảm ứng tại Phòng khám & Bệnh viện

Đây là phương thức được sử dụng phổ biến nhất hiện nay tại các chuỗi phòng khám nha khoa (như DentalFlow), bệnh viện thẩm mỹ, mắt và các bệnh viện tư nhân: Bệnh nhân dùng bút stylus hoặc ngón tay vẽ chữ ký trực tiếp lên màn hình máy tính bảng (iPad/Android).

---

## 1. Bản chất Kỹ thuật: "Chỉ là một bức ảnh vẽ"

```
[Bệnh nhân vẽ chữ ký lên màn hình Tablet]
                  │
                  ▼
[Phần mềm chụp ảnh nét vẽ (chuỗi base64 PNG)]
                  │
                  ▼
[Chèn ảnh vào ô chữ ký trên file PDF]
                  │
                  ▼
[Lưu file PDF vào máy chủ bệnh viện / phòng khám]
```

### 3 Lỗ hổng Chết người về Kỹ thuật:
1. **Không có mã hóa khóa công khai (PKI):** Hoàn toàn không sinh cặp khóa Private Key / Public Key.
2. **Không có tính toàn vẹn (Tamper-proofing):** File PDF sau khi chèn ảnh chữ ký không được mã hóa băm (Hash). Nếu ai đó sửa nội dung cam kết, viện phí hay phác đồ điều trị, ảnh chữ ký vẫn hiển thị bình thường.
3. **Dễ bị sao chép & giả mạo:** Bất kỳ nhân viên IT nào có quyền truy cập cơ sở dữ liệu đều có thể trích xuất ảnh chữ ký này và dán vào bất kỳ biên bản nào khác mà không ai biết.

---

## 2. Rủi ro Pháp lý khi Kiện tụng Y khoa

- **Cơ quan giám định không thể kết luận:** Theo Viện Khoa học Hình sự (Bộ Công An), việc giám định chữ ký truyền thống dựa trên: **lực tì đè cơ học, thớ giấy xé, độ đậm nhạt của mực, điểm dừng bút**. Nét vẽ trên mặt kính cảm ứng điện dung **hoàn toàn mất đi các thuộc tính này**.
- **Dễ bị người bệnh chối bỏ:** Khi xảy ra tai biến y khoa, bệnh nhân/người nhà chỉ cần tuyên bố: *"Tôi chưa từng ký vào bản này. Nét vẽ nguệch ngoạc trên màn hình là do nhân viên y tế tự vẽ sau khi xảy ra sự cố"*. Bệnh viện hoàn toàn mất quyền tự vệ trước Tòa.

---

## 3. Vì sao các Cơ sở Y tế vẫn chuộng dùng?

- ✅ **Rất rẻ & dễ tích hợp:** Lập trình viên chỉ cần vài dòng mã HTML5 Canvas là xong.
- ✅ **Bệnh nhân quen thuộc:** Không cần giải thích nhiều, thao tác nhanh như ký giấy.

---

## 4. Kịch bản EasyCA Thuyết phục Bệnh viện Chuyển đổi sang PKI

> *"Ban Giám đốc đang đầu tư hàng chục tỷ đồng cho uy tín và thương hiệu, nhưng lại giao tính mạng pháp lý của Bệnh viện vào một nét vẽ nguệch ngoạc trên màn hình iPad. Khi xảy ra tranh chấp phẫu thuật, nét vẽ đó hoàn toàn không bảo vệ được Bác sĩ.  
> **EasyCA nâng cấp quy trình này thành Chuẩn PKI:** Bệnh nhân vẫn ký trên tablet, nhưng đằng sau là công nghệ mã hóa PKI niêm phong tài liệu, đảm bảo giá trị pháp lý tuyệt đối theo Thông tư 13/2025/TT-BYT."*

