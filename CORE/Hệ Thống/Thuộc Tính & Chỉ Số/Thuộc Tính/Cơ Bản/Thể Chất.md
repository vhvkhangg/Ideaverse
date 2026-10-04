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

# Thể Chất

## Định Nghĩa

> Chất lượng tổng thể, sức chịu đựng và khả năng duy trì hoạt động của cơ thể.

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

- Sức bền và khả năng chịu tải cơ thể.
- Khả năng chịu thương và phục hồi tự nhiên.
- Khả năng thích nghi với áp lực thể chất và môi trường.

### Không Đại Diện Cho

- Sức Mạnh cơ bắp thuần túy — thuộc [[Sức Mạnh]].
- Giá trị Sinh Mệnh Lực hiện tại — thuộc [[SINH MỆNH LỰC]].

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

Thể Chất thường đóng góp vào `Sinh Mệnh Lực Tối Đa`, `Thể Lực Tối Đa`, hồi phục thể chất và các đại lượng độ bền phù hợp. Không có conversion cố định toàn cục; hệ số phụ thuộc build/subsystem.

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

Power system khác có thể quy về Thể Chất chuẩn Ideaverse; hệ số dẫn xuất Chỉ Số/Tài Nguyên vẫn do subsystem/build định nghĩa.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

Hai cá thể cùng `Thể Chất: 10` có thể có `Sinh Mệnh Lực Tối Đa` khác nhau nếu Chủng Tộc/Nghề Nghiệp/Công Pháp cho hệ số chuyển đổi khác nhau.
