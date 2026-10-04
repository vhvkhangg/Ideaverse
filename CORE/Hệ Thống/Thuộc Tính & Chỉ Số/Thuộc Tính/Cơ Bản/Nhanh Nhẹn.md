---
type: attribute
category: basic
growth-type: ordinary
allow-negative-base: false
allow-negative-effective: false
extraction: true
status: frozen
version: 1
tags:
  - ideaverse/system/attribute
---

# Nhanh Nhẹn

## Định Nghĩa

> Khả năng điều khiển cơ thể với tốc độ, độ chính xác và phản ứng cao.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm | Cơ Bản |
| Phương thức tăng trưởng | Thông thường |
| Base có thể âm | Không |
| Effective có thể âm | Không |
| Chiết xuất theo Chuyển | Có |

## Bản Chất

### Đại Diện Cho

- Phản xạ.
- Tốc độ động tác và đổi hướng.
- Phối hợp và độ chính xác của vận động cơ thể.

### Không Đại Diện Cho

- Tốc độ do phương tiện, cơ giáp hoặc thiết bị tạo ra nếu không phụ thuộc khả năng vận động của cá thể.
- Dịch chuyển tức thời hoặc năng lực không dựa trên vận động cơ thể.
- Sức Mạnh cơ bắp.

## Thang Giá Trị

- `~0.5`: tham chiếu gần đúng cho người trưởng thành khỏe mạnh bình thường.
- `1`: cực hạn tự nhiên của người thường.
- `>1`: vượt cực hạn người thường.
- Chủng tộc khác có thể có Base `>1` tự nhiên.
- Không có hard cap.

## Base / Effective

- Tăng trưởng vĩnh viễn sửa **Base**.
- Flat modifier tạm thời tác động lên Effective trước các `%` modifier.
- Các `%` modifier độc lập stack multiplicatively theo [[THUỘC TÍNH#2.2. Base và Effective]].
- Effective cuối cùng sàn tại `0`.

## Quan Hệ Với Chỉ Số/Tài Nguyên

Nhanh Nhẹn thường đóng góp vào `Tốc Độ Đánh`, `Tốc Độ Di Chuyển`, `Chính Xác`, `Né Tránh` và đại lượng vận động phù hợp. Không có conversion cố định toàn cục.

## Tăng Trưởng

Có thể tăng Base bằng tăng trưởng thông thường hợp lệ theo [[THUỘC TÍNH]].

## Suy Giảm

Debuff/hiệu ứng tạm thời mặc định tác động lên Effective; mechanic làm suy giảm vĩnh viễn phải ghi rõ rằng nó sửa Base.

## Điểm Thuộc Tính Tự Do

Có. `1 Điểm Thuộc Tính Tự Do = +1 Base` tại bậc Chuyển hiện tại.

## Chiết Xuất

- Có.
- Tuân theo 10 Chuyển, Thí Luyện và Hệ Số Chiết Xuất Tích Lũy trong [[THUỘC TÍNH]].

## Quy Đổi Giữa Các Hệ Thống

Power system khác có thể quy về Nhanh Nhẹn chuẩn Ideaverse; hệ số dẫn xuất do subsystem/build định nghĩa.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

Hai cá thể cùng `Nhanh Nhẹn: 10` không bắt buộc có cùng `Tốc Độ Di Chuyển` nếu nguồn chuyển đổi khác nhau.
