---
title: "Mô hình Ký tay trên Tablet Cảm ứng (DentalFlow & HIS Phòng khám)"
vendor: "DentalFlow, BambuFit, Nanosoft, LinkCare và nhiều HIS nội bộ"
product: "Tính năng Ký cảm ứng trên iPad / Tablet / Bảng vẽ Wacom"
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

## 1. Cơ chế Hoạt động: "Bản chất chỉ là một bức ảnh vẽ"

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

## 2. Vì sao Viện Khoa học Hình sự KHÔNG THỂ Giám định Chữ ký trên Kính?

Trong lĩnh vực y tế, tranh chấp thường xảy ra khi có tai biến hoặc kết quả điều trị không như mong đợi (ví dụ: cấy Implant bị đào thải, phẫu thuật thẩm mỹ hỏng, sốc phản vệ thuốc).

Khi bệnh nhân khởi kiện ra Tòa án và tuyên bố: *"Tôi chưa từng ký vào bản cam kết này. Nét vẽ nguệch ngoạc trên màn hình iPad đó là do nhân viên phòng khám tự vẽ lên để chối bỏ trách nhiệm!"*.

**Tòa án trưng cầu giám định chữ ký:**
- Theo quy chuẩn giám định chữ ký của **Viện Khoa học Hình sự (Bộ Công An)**, giám định viên dựa vào các yếu tố vật lý gồm:
  + Lực tì đè cơ học tạo độ lún trên thớ giấy.
  + Chiều hướng ngòi bút xé rách sợi cellulose của giấy.
  + Độ đậm nhạt của dòng mực và điểm dừng bút.
  + Phản xạ co bóp cơ tay vô thức của người ký.
- **Nét vẽ trên màn hình kính cảm ứng điện dung (Capacitive Screen) HOÀN TOÀN MẤT ĐI các thuộc tính này**.
- **Kết luận của cơ quan giám định:** Không đủ cơ sở khoa học để xác định nét vẽ trên màn hình kính có phải do chính người đó vẽ hay không.
- **Hậu quả:** Tòa án tuyên bố văn bản vô hiệu, cơ sở y tế chịu toàn bộ trách nhiệm bồi thường thiệt hại và mất uy tín thương hiệu.

---

## 3. Kịch bản Bán hàng Thực chiến khi Thuyết phục Bệnh viện Chuyển đổi

Khi EasyCA tiếp cận các Bệnh viện tư nhân, Bệnh viện quốc tế, Bệnh viện thẩm mỹ, Chuỗi nha khoa lớn đang dùng hình thức Ký tay Tablet:

> **Đòn bẩy tư vấn "sát thương cao":**  
> *"Ban Giám đốc đang đầu tư hàng chục tỷ đồng cho cơ sở vật chất và thương hiệu, nhưng lại giao tính mạng pháp lý của Bệnh viện vào một nét vẽ nguệch ngoạc trên màn hình iPad. Khi xảy ra một ca tai biến phẫu thuật hay khiếu nại viện phí lớn, nét vẽ đó hoàn toàn không bảo vệ được Bác sĩ trước Tòa án.  
> **EasyCA nâng cấp toàn bộ quy trình này thành Chuẩn PKI Quốc tế:** Bệnh nhân vẫn ký trên tablet, nhưng đằng sau là công nghệ mã hóa PKI niêm phong tài liệu, đảm bảo hồ sơ có giá trị pháp lý tuyệt đối theo Thông tư 13/2025/TT-BYT."*
