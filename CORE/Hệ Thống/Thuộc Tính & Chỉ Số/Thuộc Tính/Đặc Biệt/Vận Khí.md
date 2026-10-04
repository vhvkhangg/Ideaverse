---
type: attribute
category: special
growth-type: special
allow-negative-base: true
allow-negative-effective: true
extraction: false
tags:
  - ideaverse/system/attribute
---

# Vận Khí

## Định Nghĩa

> Mức độ thiên lệch thuận lợi hoặc bất lợi của cá thể trong những sự kiện vốn có yếu tố xác suất.

## Quy Tắc Cốt Lõi

> Vận Khí chỉ tác động tới **khả năng vốn đã tồn tại**. Nó không tự tạo ra một kết quả bất khả thi hoặc một khả năng bằng `0`.

Ví dụ:

- Vật phẩm có xác suất rơi > 0 → Vận Khí có thể ảnh hưởng.
- Vật phẩm không nằm trong tập kết quả có thể xảy ra → Vận Khí không tự sinh ra nó.

## Giá Trị Âm

- `> 0`: thiên hướng thuận lợi.
- `= 0`: trung tính.
- `< 0`: thiên hướng bất lợi.

Giá trị Vận Khí không tự xác định công thức xác suất. Mỗi subsystem sử dụng Vận Khí phải định nghĩa cách nó ảnh hưởng xác suất nếu cần.

## Tăng Trưởng

Chỉ thay đổi bằng phương thức đặc biệt/hiếm như cơ duyên, quyền năng, nguyền rủa, cướp đoạt hoặc cơ chế tương đương đã được định nghĩa.

## Chiết Xuất

Không.
