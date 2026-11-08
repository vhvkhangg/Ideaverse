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

# Tinh Thần

## Định Nghĩa

> Cường độ, độ ổn định và khả năng vận hành của ý thức/tinh thần.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm | Cơ Bản |
| Phương thức tăng trưởng | Thông thường |
| Base có thể âm | Không |
| Effective có thể âm | Không |

## Bản Chất

### Đại Diện Cho

- Khả năng tập trung và chịu tải tinh thần.
- Khả năng vận hành nhiều tác vụ tinh thần đồng thời.
- Nền tảng cho cảm nhận, điều khiển Năng Lượng hoặc kháng tác động tinh thần khi subsystem tương ứng sử dụng nó.

### Không Đại Diện Cho

- Trí thông minh nói chung.
- Khả năng học và lĩnh ngộ — thuộc [[Ngộ Tính]].
- Kiến thức mà cá thể đã tích lũy.

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

- Mỗi 1 Effective: `+10 Công Pháp Thuật`, `+100 Tinh Lực Tối Đa`, `+5 Kháng Phép`, `+10 Định Tính Tối Đa`.
- Mỗi 10 Effective: `+1 Xuyên Kháng Phép` và `+1 Giá Trị Pháp Thuật Kháng Tính` (Trung Cấp).
- Năng Lượng Tối Đa của từng pool tương thích: `100 × Tinh Thần Effective × C_tương thích` nếu pool đã mở khóa.
- Không tự tăng hồi phục `% Tối Đa/s`.

Bảng và thứ tự chuyển đổi canonical: [[THUỘC TÍNH#5. Chuyển Đổi Thuộc Tính → Chỉ Số/Tài Nguyên]].

## Tăng Trưởng

Có thể tăng Base bằng tăng trưởng thông thường hợp lệ theo [[THUỘC TÍNH]].

## Suy Giảm

Debuff/hiệu ứng tạm thời mặc định tác động lên Effective; mechanic làm suy giảm vĩnh viễn phải ghi rõ rằng nó sửa Base.

## Điểm Thuộc Tính Tự Do

Có. `1 Điểm Thuộc Tính Tự Do = +1 Base`, không thêm bậc Chuyển vào tên; điểm cộng trước Chuyển được nhân thưởng Thí Luyện tương ứng. Xem [[THUỘC TÍNH#3. Điểm Thuộc Tính Tự Do]].

## Quy Đổi Giữa Các Hệ Thống

Power system khác ánh xạ về cùng thang Tinh Thần của Ideaverse. Chỉ Số dẫn xuất theo bảng mặc định v2; mechanic riêng chỉ được thay đổi hệ số/cộng thêm nếu khai báo rõ, không tính trùng.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

Ví dụ `Tinh Thần Effective = 10` tạo `100 Công Pháp Thuật`, `1000 Tinh Lực Tối Đa`, `50 Kháng Phép`, `100 Định Tính Tối Đa`, `1 Xuyên Kháng Phép`, `1 Giá Trị Pháp Thuật Kháng Tính`; pool Năng Lượng đã mở khóa và `C_tương thích=1` có đóng góp `1000` dung lượng.
