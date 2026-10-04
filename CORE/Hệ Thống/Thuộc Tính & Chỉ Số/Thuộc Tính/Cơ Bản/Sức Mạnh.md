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
| Chiết xuất theo Chuyển | Có |

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

Sức Mạnh thường đóng góp vào [[CHỈ SỐ CƠ SỞ|Công Vật Lý]], khả năng phát lực và một phần Thể Lực/Chỉ Số vật lý nếu subsystem quy định. Không có conversion cố định toàn cục; hệ số do Chủng Tộc, Nghề Nghiệp, Công Pháp, Huyết Mạch, Thiên Phú hoặc power system sở hữu.

## Tăng Trưởng

Có thể tăng Base bằng tăng trưởng thông thường hợp lệ như level, rèn luyện, Điểm Thuộc Tính Tự Do, Công Pháp, Nghề Nghiệp, Thiên Phú hoặc vật phẩm cải tạo bản thể.

## Suy Giảm

Debuff/hiệu ứng tạm thời mặc định tác động lên Effective; mechanic làm suy giảm vĩnh viễn phải ghi rõ rằng nó sửa Base.

## Điểm Thuộc Tính Tự Do

Có. `1 Điểm Thuộc Tính Tự Do = +1 Base` tại bậc Chuyển hiện tại; xem [[THUỘC TÍNH#3. Điểm Thuộc Tính Tự Do]].

## Chiết Xuất

- Có.
- Tuân theo 10 Chuyển, Thí Luyện và Hệ Số Chiết Xuất Tích Lũy tại [[THUỘC TÍNH#4. Chuyển, Thí Luyện và Chiết Xuất Thuộc Tính]].

## Quy Đổi Giữa Các Hệ Thống

Power system khác có thể quy về Sức Mạnh chuẩn Ideaverse để so sánh nhưng vẫn giữ lore bản địa; không có universal conversion coefficient.

## Trường Hợp Biên

- Base không âm.
- Effective không âm.
- Không có hard cap.

## Ví Dụ

`Sức Mạnh III: 10` nhận `+1 Điểm Thuộc Tính Tự Do` sau Chuyển III → `Sức Mạnh III: 11`.
