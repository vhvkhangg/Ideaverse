---
type: resource
resource-category: core
has-thresholds: true
status: frozen
version: 1
tags:
  - ideaverse/system/resource
---

# SINH MỆNH LỰC

## Định Nghĩa

> Tài Nguyên biểu diễn trạng thái sinh mệnh hiện tại của cá thể.

## Phân Loại

| Thuộc tính | Giá trị |
|---|---|
| Nhóm Tài Nguyên | Cốt lõi |
| Đơn vị | Điểm |
| Có ngưỡng suy giảm | Có |

## Pool

```text
Sinh Mệnh Lực: hiện tại / Sinh Mệnh Lực Tối Đa
```

## Chỉ Số Liên Quan

- `Sinh Mệnh Lực Tối Đa`
- `Hồi Phục Sinh Mệnh Lực`
- `Tỷ Lệ Hồi Phục Sinh Mệnh Lực`

## Nguồn Tăng Trưởng

Giá trị tối đa/hồi phục có thể chịu ảnh hưởng từ Thuộc Tính, Công Pháp, Nghề Nghiệp, Thiên Phú, Trang Bị, Kỹ Năng hoặc mechanic khác; không có công thức universal bắt buộc.

## Tiêu Hao

Sinh Mệnh Lực giảm khi nhận sát thương hoặc bởi mechanic ghi rõ chi phí/tổn thất Sinh Mệnh Lực.

## Hồi Phục

Tuân theo các Chỉ Số hồi phục và mechanic liên quan; điều kiện hồi phục không bắt buộc giống nhau giữa mọi cá thể.

## Phụ Tố Nội Sinh

- **Tên:** Suy Nhược Sinh Mệnh
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

Không phá Định Tính, không có duration, không stack nhiều bậc và cập nhật động ngay khi tỷ lệ Sinh Mệnh Lực thay đổi.

## Trạng Thái 0%

```text
Sinh Mệnh Lực = 0
→ kích hoạt cơ chế Tử Vong
```

Đây là state transition, không phải `Suy Nhược Sinh Mệnh` cấp cao hơn X. Bất Tử, Hồi Sinh, mạng phụ hoặc điều kiện tử vong thay thế có thể can thiệp nếu ghi rõ.

## Chuyển Hóa

Không có quy tắc chuyển hóa mặc định cho Sinh Mệnh Lực. Mechanic muốn chuyển đổi chi phí/tổn thất sang Tài Nguyên khác phải định nghĩa riêng.

## Quan Hệ Với Thuộc Tính / Chỉ Số

[[Thể Chất]] thường có thể đóng góp vào `Sinh Mệnh Lực Tối Đa`/hồi phục theo hệ số của build; [[CHỈ SỐ]] định nghĩa pattern dung lượng và hồi phục.

## Trường Hợp Biên

- Giá trị hiện tại mặc định sàn tại `0`.
- Không vượt `Sinh Mệnh Lực Tối Đa` trừ khi mechanic cho phép lớp giá trị vượt ngưỡng riêng.
- `0%` được resolve bằng state transition trước khi coi là một bậc Phụ Tố mới.

## Ghi Chú Thiết Kế

`Sinh Mệnh Tối Đa` trong thiết kế cũ đã được chuẩn hóa thành **`Sinh Mệnh Lực Tối Đa`**.
