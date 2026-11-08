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

# Sức Mạnh

## Định Nghĩa

> Khả năng tạo ra lực vật lý chủ động của cơ thể.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm | Cơ Bản |
| Phương thức tăng trưởng | Thông thường |
| Base có thể âm | Không |
| Effective có thể âm | Không |

## Bản Chất

### Đại Diện Cho

- Lực đánh, kéo, đẩy, nâng và mang vác.
- Khả năng phát lực trực tiếp bằng cơ thể.

### Không Đại Diện Cho

- Độ bền và khả năng chịu thương của cơ thể — thuộc [[Thể Chất]].
- Tốc độ phản ứng hoặc điều khiển cơ thể — thuộc [[Nhanh Nhẹn]].
- Kỹ thuật chiến đấu.

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

- `+10 Công Vật Lý` mỗi 1 Effective (Cơ Sở).
- `+1 Xuyên Giáp` (Điểm) mỗi 10 Effective (Trung Cấp).
- Không mặc định sinh Thể Lực hoặc Chỉ Số khác ngoài bảng này.

Bảng và thứ tự chuyển đổi canonical: [[THUỘC TÍNH#5. Chuyển Đổi Thuộc Tính → Chỉ Số/Tài Nguyên]].

## Tăng Trưởng

Có thể tăng Base bằng tăng trưởng thông thường hợp lệ như level, rèn luyện, Điểm Thuộc Tính Tự Do, Công Pháp, Nghề Nghiệp, Thiên Phú hoặc vật phẩm cải tạo bản thể.

## Suy Giảm

Debuff/hiệu ứng tạm thời mặc định tác động lên Effective; mechanic làm suy giảm vĩnh viễn phải ghi rõ rằng nó sửa Base.

## Điểm Thuộc Tính Tự Do

Có. `1 Điểm Thuộc Tính Tự Do = +1 Base`, không thêm bậc Chuyển vào tên; điểm cộng trước Chuyển được nhân thưởng Thí Luyện tương ứng. Xem [[THUỘC TÍNH#3. Điểm Thuộc Tính Tự Do]].

## Quy Đổi Giữa Các Hệ Thống

Power system khác ánh xạ về cùng thang Sức Mạnh của Ideaverse. Chỉ Số dẫn xuất theo bảng mặc định v2; mechanic riêng chỉ được thay đổi hệ số/cộng thêm nếu khai báo rõ, không tính trùng.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

Ví dụ `Sức Mạnh Effective = 15` tạo `150 Công Vật Lý` và `1.5 Xuyên Giáp` trước các nguồn Chỉ Số độc lập.
