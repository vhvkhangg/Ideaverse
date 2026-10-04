---
type: attribute
category: special
growth-type: special
allow-negative-base: true
allow-negative-effective: true
extraction: false
status: frozen
version: 1
tags:
  - ideaverse/system/attribute
---

# Vận Khí

## Định Nghĩa

> Mức độ thiên lệch thuận lợi hoặc bất lợi của cá thể trong những sự kiện vốn có yếu tố xác suất.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm | Đặc Biệt |
| Phương thức tăng trưởng | Đặc biệt/hiếm |
| Base có thể âm | Có |
| Effective có thể âm | Có |
| Chiết xuất theo Chuyển | Không |

## Bản Chất

### Đại Diện Cho

- Khả năng làm lệch trọng số/xác suất của các kết quả vốn đã tồn tại trong tập khả thi.

### Không Đại Diện Cho

- Khả năng tạo ra kết quả bất khả thi.
- Khả năng biến xác suất `0` thành xác suất dương.

## Thang Giá Trị

- `1` là cực hạn tự nhiên của người thường đối với Vận Khí thuận lợi.
- `>0`: thiên hướng thuận lợi; `=0`: trung tính; `<0`: thiên hướng bất lợi.
- Base và Effective có thể âm.
- Không có hard cap ở phía dương hoặc âm.

## Base / Effective

- Effective tuân theo `Base → Flat → Percentage Modifier multiplicative` trong [[THUỘC TÍNH#2.2. Base và Effective]].
- Quy tắc dấu/sàn theo bảng tại [[THUỘC TÍNH#2.3. Quy Tắc Giá Trị Âm]].

## Quan Hệ Với Chỉ Số/Tài Nguyên

Vận Khí mặc định không sinh Chỉ Số chiến đấu trực tiếp. Mỗi subsystem xác suất phải định nghĩa cách Vận Khí điều chỉnh trọng số/xác suất của chính nó.

## Tăng Trưởng

Chỉ thay đổi bằng phương thức đặc biệt/hiếm như cơ duyên, quyền năng, nguyền rủa, cướp đoạt hoặc mechanic tương đương.

## Suy Giảm

Modifier/debuff có thể làm giảm Effective theo rule chung; mechanic làm thay đổi Base phải ghi rõ.

## Điểm Thuộc Tính Tự Do

Không nhận Điểm Thuộc Tính Tự Do thông thường.

## Chiết Xuất

- Không.
- Không thêm hậu tố Chuyển `I–X`.

## Quy Đổi Giữa Các Hệ Thống

Power system khác có thể ánh xạ khái niệm tương đương về Vận Khí, nhưng subsystem sử dụng nó phải tự định nghĩa check/hệ số cụ thể thay vì dùng conversion chiến đấu toàn cục.

## Trường Hợp Biên

Vận Khí chỉ tác động tới khả năng vốn đã tồn tại; kết quả có xác suất `0` vẫn là `0`.

## Ví Dụ

Vật phẩm có xác suất rơi `>0` có thể chịu ảnh hưởng của Vận Khí; vật phẩm không nằm trong tập kết quả có thể xảy ra thì không.
