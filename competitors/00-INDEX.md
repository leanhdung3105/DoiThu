---
title: "Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ Chữ ký số Bệnh viện"
description: "Danh mục các đơn vị thực tế có giải pháp chữ ký số cho bệnh nhân/người nhà tại bệnh viện Việt Nam."
last_updated: "2026-11-09"
---

# Mục lục & Cấu trúc Dữ liệu Nghiên cứu Đối thủ

Bộ tài liệu được thiết kế theo cấu trúc Markdown chuẩn (hỗ trợ Frontmatter), sẵn sàng để tích hợp và hiển thị trực tiếp lên website (Astro, Next.js, Nuxt Content, Docusaurus, VitePress...).

Tất cả các tài liệu tập trung **100% vào giải pháp ký xác nhận cho Bệnh nhân & Người nhà bệnh nhân tại Bệnh viện**, loại bỏ toàn bộ các đơn vị CA chỉ bán Token thuế cho doanh nghiệp.

---

## Danh mục Tài liệu

| STT | Tên File | Đơn vị / Giải pháp | Phương thức ký bệnh nhân | Phân loại TT 13 |
|:---:|---|---|---|:---:|
| 00 | [**`00-tong-quan-so-sanh.md`**](00-tong-quan-so-sanh.md) | **Bảng Tổng quan & So sánh** | Ma trận 7 giải pháp & phân tích kỹ thuật | **Tổng hợp** |
| 01 | [**`01-easyca-softdreams.md`**](01-easyca-softdreams.md) | **EasyCA (SoftDreams)** | **CKS chuẩn PKI (Cloud HSM / eKYC)** | **Hình thức 1** ✅ |
| 02 | [**`02-2id-2contract.md`**](02-2id-2contract.md) | **2ID / 2Contract** | Quét chip CCCD (NFC) + Đối soát khuôn mặt | **Hình thức 2 & 3** |
| 03 | [**`03-isofh-vneid.md`**](03-isofh-vneid.md) | **ISOFH (BV Xanh Pôn)** | Ký xác thực qua App VNeID (Push Noti) | **Hình thức 3** |
| 04 | [**`04-viettel-hms.md`**](04-viettel-hms.md) | **Viettel HMS** | Ký tay trên Tablet cảm ứng & VNeID | **Hình thức 3** |
| 05 | [**`05-vnpt-his.md`**](05-vnpt-his.md) | **VNPT HIS / SmartCA** | Ký qua App VNeID & Tiềm năng SmartCA | **Hình thức 3 & 1** |
| 06 | [**`06-fpt-ehospital.md`**](06-fpt-ehospital.md) | **FPT eHospital** | Ký qua mã xác thực OTP SMS & VNeID | **Hình thức 3** |
| 07 | [**`07-ky-tay-tablet.md`**](07-ky-tay-tablet.md) | **Ký tay Tablet (DentalFlow...)** | Vẽ chữ ký ngón tay/stylus lên màn hình | **Hình thức 3** |

---

## Chuẩn Dữ liệu Frontmatter trên Mỗi File

Mỗi file đều chứa metadata ở đầu file dạng YAML:

```yaml
---
title: "Tên giải pháp"
vendor: "Tên nhà cung cấp"
product: "Tên sản phẩm"
signing_method: "Phương thức ký của người bệnh"
tt13_category: "Phân loại theo Thông tư 13/2025/TT-BYT"
legal_standing: "Đánh giá mức độ pháp lý / chống chối bỏ"
target_hospital: "Phân khúc khách hàng bệnh viện mục tiêu"
deployments: "Các bệnh viện đã triển khai thực tế"
role: "Vai trò đối với EasyCA"
---
```

Nhờ cấu trúc này, khi bạn xây dựng website, bạn có thể dễ dàng duyệt qua các file Markdown để:
- Hiển thị danh sách card đối thủ có gắn tag phân loại (Tag `tt13_category`, Tag `signing_method`).
- Lọc theo mức độ pháp lý hoặc phương thức ký (PKI, CCCD, VNeID, Tablet, OTP).
- Tự động dựng bảng so sánh tính năng dựa trên metadata.
