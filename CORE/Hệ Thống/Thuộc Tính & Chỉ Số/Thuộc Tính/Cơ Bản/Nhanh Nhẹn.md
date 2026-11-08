---
type: attribute
category: basic
growth-type: ordinary
allow-negative-base: false
allow-negative-effective: false
status: frozen
version: 2
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

- Mỗi 1 Effective: `+2 đòn/s Tốc Độ Đánh`, `+8 m/s Tốc Độ Di Chuyển` (Cơ Sở).
- Mỗi 10 Effective: `+1 Chính Xác` và `+1 Né Tránh` (Điểm, Trung Cấp).
- Không tự tăng `Tỷ Lệ Chí Mạng` hoặc xác suất Đón Đỡ.

Bảng và thứ tự chuyển đổi canonical: [[THUỘC TÍNH#5. Chuyển Đổi Thuộc Tính → Chỉ Số/Tài Nguyên]].

## Tăng Trưởng

Có thể tăng Base bằng tăng trưởng thông thường hợp lệ theo [[THUỘC TÍNH]].

## Suy Giảm

Debuff/hiệu ứng tạm thời mặc định tác động lên Effective; mechanic làm suy giảm vĩnh viễn phải ghi rõ rằng nó sửa Base.

## Điểm Thuộc Tính Tự Do

Có. `1 Điểm Thuộc Tính Tự Do = +1 Base`, không thêm bậc Chuyển vào tên; điểm cộng trước Chuyển được nhân thưởng Thí Luyện tương ứng. Xem [[THUỘC TÍNH#3. Điểm Thuộc Tính Tự Do]].

## Quy Đổi Giữa Các Hệ Thống

Power system khác ánh xạ về cùng thang Nhanh Nhẹn của Ideaverse. Chỉ Số dẫn xuất theo bảng mặc định v2; mechanic riêng chỉ được thay đổi hệ số/cộng thêm nếu khai báo rõ, không tính trùng.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

Ví dụ `Nhanh Nhẹn Effective = 15` tạo `30 đòn/s`, `120 m/s`, `1.5 Chính Xác` và `1.5 Né Tránh` trước nguồn khác.
