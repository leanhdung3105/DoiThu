---
title: "Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ Chữ ký số Bệnh viện"
description: "Danh mục báo cáo phân tích đối thủ cạnh tranh chữ ký số bệnh nhân/người nhà tại bệnh viện Việt Nam theo chuẩn khách quan."
last_updated: "2026-11-09"
---

# Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ

Bộ tài liệu được thiết kế theo cấu trúc Markdown chuẩn (hỗ trợ Frontmatter), sẵn sàng để tích hợp và hiển thị trực tiếp lên website tài liệu (Docsify, Astro, Next.js, Nuxt Content, Docusaurus...).

Tất cả các tài liệu được chuẩn hóa theo khung phân tích chuyên môn 6 phần, gắn nhãn kiểm chứng thông tin minh bạch (`[Đã xác minh]`, `[Có nguồn tham khảo]`, `[Nhận định]`, `[Chưa xác minh]`).

---

## Danh mục Tài liệu

| STT | Tên File | Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Nhóm theo TT 13/2025 |
|:---:|---|---|---|:---:|
| 00 | [**`00-tong-quan-so-sanh.md`**](00-tong-quan-so-sanh.md) | **Báo cáo Tổng quan** | Ma trận so sánh 13 tiêu chí & phân tích chuỗi giá trị | **Tổng hợp** |
| 01 | [**`01-easyca-softdreams.md`**](01-easyca-softdreams.md) | **EasyCA (SoftDreams)** | **Chữ ký số PKI (Remote Signing / Cloud HSM)** | **Nhóm 1** |
| 02 | [**`02-2id-2contract.md`**](02-2id-2contract.md) | **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | **Nhóm 2 & 3** |
| 03 | [**`03-isofh-vneid.md`**](03-isofh-vneid.md) | **ISOFH (BV Xanh Pôn)** | Chữ ký số PKI xác thực qua App VNeID (VNPT SmartCA) | **Nhóm 1** |
| 04 | [**`04-viettel-hms.md`**](04-viettel-hms.md) | **Viettel HMS** | Ký cảm ứng trên Tablet & Xác thực VNeID | **Nhóm 3** |
| 05 | [**`05-vnpt-his.md`**](05-vnpt-his.md) | **VNPT HIS / SmartCA** | Ký qua App VNeID, Tablet & SmartCA cá nhân | **Nhóm 3 & 1** |
| 06 | [**`06-fpt-ehospital.md`**](06-fpt-ehospital.md) | **FPT eHospital** | Xác thực qua mã OTP SMS / Zalo & eSign | **Nhóm 3** |
| 07 | [**`07-ky-tay-tablet.md`**](07-ky-tay-tablet.md) | **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký cảm ứng trên màn hình thiết bị | **Nhóm 3** |

---

## Cấu trúc Tiêu chuẩn 6 Phần áp dụng trên Từng Đối thủ

Mỗi hồ sơ đối thủ được trình bày theo cấu trúc đồng nhất:
1. **Thông tin doanh nghiệp:** Pháp nhân, sản phẩm, vai trò trong chuỗi cung ứng y tế, mức độ hiện diện thị trường.
2. **Sản phẩm và công nghệ:** Phân tách luồng cán bộ y tế vs bệnh nhân, công nghệ định danh, xác thực, ký số, lưu trữ và tích hợp HIS/EMR.
3. **Căn cứ pháp lý:** Phân nhóm theo Điều 3 Thông tư 13/2025/TT-BYT, Luật Giao dịch điện tử 2023, Nghị định 23/2025/NĐ-CP, Luật Bảo vệ dữ liệu cá nhân 91/2025/QH15 và Nghị định 356/2025/NĐ-CP.
4. **Khách hàng và triển khai:** Cơ sở y tế đã triển khai, quy mô, tình trạng vận hành, nguồn xác minh.
5. **Bảng đánh giá tiêu chuẩn 13 tiêu chí & Khả năng cạnh tranh vs EasyCA:** Điểm mạnh, điểm yếu, rào cản chuyển đổi, chiến lược cạnh tranh.
6. **Nguồn tham khảo & Bằng chứng xác thực:** Văn bản quy phạm pháp luật, cổng thông tin chính thức, hồ sơ đấu thầu công khai.
