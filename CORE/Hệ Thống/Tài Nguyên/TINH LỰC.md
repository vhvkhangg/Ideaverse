---
type: resource
resource-category: core
has-thresholds: true
status: frozen
version: 1
tags:
  - ideaverse/system/resource
---

# TINH LỰC

## Định Nghĩa

> Tài Nguyên biểu diễn khả năng duy trì hoạt động tinh thần hiện tại của cá thể.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm Tài Nguyên | Cốt lõi |
| Đơn vị | Điểm |
| Có ngưỡng suy giảm | Có |

## Pool

```text
Tinh Lực: hiện tại / Tinh Lực Tối Đa
```

## Chỉ Số Liên Quan

- `Tinh Lực Tối Đa`
- `Hồi Phục Tinh Lực`
- `Tỷ Lệ Hồi Phục Tinh Lực`

## Nguồn Tăng Trưởng

`Tinh Lực Tối Đa`/hồi phục có thể tăng bởi Thuộc Tính, Công Pháp, Nghề Nghiệp, Thiên Phú, Trang Bị hoặc mechanic khác.

## Tiêu Hao

Tinh Lực bị tiêu hao bởi Kỹ Năng/tác vụ tinh thần hoặc mechanic ghi rõ sử dụng pool này.

## Hồi Phục

Tuân theo các Chỉ Số hồi phục và điều kiện riêng của cá thể/build.

## Phụ Tố Nội Sinh

- **Tên:** Suy Kiệt Tinh Lực
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

Không phá Định Tính, không có duration, không stack nhiều bậc và cập nhật động ngay khi tỷ lệ Tinh Lực thay đổi.

## Trạng Thái 0%

Khi `Tinh Lực = 0`:

- không thể khởi tạo Kỹ Năng/tác vụ yêu cầu tiêu hao Tinh Lực;
- không thể tiếp tục Kỹ Năng/tác vụ cần duy trì Tinh Lực khi không đủ chi phí duy trì;
- không mặc định cá thể lập tức bất tỉnh hoặc hôn mê; trạng thái đó phải đến từ Phụ Tố hoặc mechanic cụ thể.

`0%` là state transition, không phải một Cấp Phụ Tố mới.

## Chuyển Hóa

Không có chuyển hóa mặc định. Mechanic có thể thay thế/chuyển chi phí giữa Tinh Lực và Tài Nguyên khác nếu định nghĩa rõ.

## Quan Hệ Với Thuộc Tính / Chỉ Số

`Tinh Lực` không đồng nhất với [[Tinh Thần]]. [[Tinh Thần]] là năng lực nền; Tinh Lực là pool trạng thái có thể tiêu hao/hồi phục. Hệ số chuyển đổi do build/subsystem định nghĩa.

## Trường Hợp Biên

- Giá trị hiện tại mặc định sàn tại `0`.
- Không vượt `Tinh Lực Tối Đa` nếu không có mechanic riêng.

## Ghi Chú Thiết Kế

Phụ Tố suy giảm của Tinh Lực là nội sinh và dynamic, là ngoại lệ có chủ đích so với snapshot của Phụ Tố thông thường.
