---
type: resource
resource-category: core
has-thresholds: true
status: frozen
version: 1
tags:
  - ideaverse/system/resource
---

# THỂ LỰC

## Định Nghĩa

> Tài Nguyên biểu diễn khả năng duy trì hoạt động thể chất hiện tại của cá thể.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm Tài Nguyên | Cốt lõi |
| Đơn vị | Điểm |
| Có ngưỡng suy giảm | Có |

## Pool

```text
Thể Lực: hiện tại / Thể Lực Tối Đa
```

## Chỉ Số Liên Quan

- `Thể Lực Tối Đa`
- `Hồi Phục Thể Lực`
- `Tỷ Lệ Hồi Phục Thể Lực`

## Nguồn Tăng Trưởng

`Thể Lực Tối Đa`/hồi phục có thể tăng bởi Thuộc Tính, Công Pháp, Nghề Nghiệp, Thiên Phú, Trang Bị hoặc mechanic khác.

## Tiêu Hao

Thể Lực có thể bị tiêu hao bởi vận động, chiến đấu, Kỹ Năng hoặc mechanic khác.

## Hồi Phục

Tuân theo các Chỉ Số hồi phục và điều kiện của cá thể; không có một tốc độ/điều kiện universal cho mọi build.

## Phụ Tố Nội Sinh

- **Tên:** Suy Kiệt Thể Lực
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

Không phá Định Tính, không có duration, không stack nhiều bậc và cập nhật động ngay khi tỷ lệ Thể Lực thay đổi.

## Trạng Thái 0%

Khi `Thể Lực = 0`:

- không thể khởi tạo hành động yêu cầu tiêu hao Thể Lực;
- hành động/Kỹ Năng cần duy trì Thể Lực không thể tiếp tục khi không đủ chi phí duy trì;
- hành động không sử dụng Thể Lực vẫn có thể thực hiện nếu các điều kiện khác cho phép.

`0%` là state transition, không phải một Cấp Phụ Tố mới.

## Chuyển Hóa

Không có chuyển hóa mặc định. Mechanic có thể thay thế/chuyển chi phí giữa Thể Lực và Tài Nguyên khác nếu định nghĩa rõ hiệu suất và điều kiện.

## Quan Hệ Với Thuộc Tính / Chỉ Số

[[Thể Chất]] và một phần [[Sức Mạnh]] có thể đóng góp vào Thể Lực theo hệ số build; [[CHỈ SỐ]] định nghĩa `Thể Lực Tối Đa` và các Chỉ Số hồi phục.

## Trường Hợp Biên

- Giá trị hiện tại mặc định sàn tại `0`.
- Không vượt `Thể Lực Tối Đa` nếu không có mechanic riêng.

## Ghi Chú Thiết Kế

Phụ Tố suy giảm của Thể Lực là nội sinh và dynamic, là ngoại lệ có chủ đích so với snapshot của Phụ Tố thông thường.
