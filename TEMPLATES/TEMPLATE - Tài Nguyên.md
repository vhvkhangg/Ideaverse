---
type: resource
resource-category:
has-thresholds:
status: draft
version:
tags:
  - ideaverse/system/resource
---

# {{title}}

## Định Nghĩa

> 

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm Tài Nguyên | |
| Đơn vị | Điểm |
| Có ngưỡng suy giảm | |

## Pool

```text
{{title}}: hiện tại / tối đa
```

## Chỉ Số Liên Quan

- `{{title}} Tối Đa`
- `Hồi Phục {{title}}`
- `Tỷ Lệ Hồi Phục {{title}}`

## Nguồn Tăng Trưởng

-

## Tiêu Hao

-

## Hồi Phục

-

## Phụ Tố Nội Sinh

- **Tên:**
- **Loại:** Phụ Tố Nội Sinh Duy Trì Theo Điều Kiện

| Tỷ lệ hiện tại | Cường Độ Nội Bộ | Cấp |
|---:|---:|---:|
| `> 70%` | `0` | Không có |
| `(50%, 70%]` | `100` | I |
| `(30%, 50%]` | `200` | II |
| `(10%, 30%]` | `400` | IV |
| `(5%, 10%]` | `600` | VI |
| `(1%, 5%]` | `800` | VIII |
| `(0%, 1%]` | `1000` | X |
| `0%` | — | Trạng thái biên |

> Xóa mục này nếu Tài Nguyên không sử dụng cơ chế ngưỡng suy giảm canonical.

## Trạng Thái 0%

-

## Chuyển Hóa

-

## Quan Hệ Với Thuộc Tính / Chỉ Số

-

## Trường Hợp Biên

-

## Ghi Chú Thiết Kế

-
