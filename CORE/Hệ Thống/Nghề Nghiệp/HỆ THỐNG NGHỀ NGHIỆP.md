# HỆ THỐNG NGHỀ NGHIỆP

> [!WARNING] Trạng thái IN DESIGN
> Hệ Thống Nghề Nghiệp chưa freeze toàn phần. Phần sau là **cross-system contract FROZEN theo [[THUỘC TÍNH]] v2**, không định nghĩa đủ mọi cơ chế Nghề Nghiệp.

## Cross-System Contract Với Thuộc Tính v2

### Chuyển

- Nghề Nghiệp có **10 lần Chuyển**, từ `I` đến `X`.
- `I–X` là **bậc Nghề Nghiệp**, không gắn thêm vào tên `Sức Mạnh / Thể Chất / Nhanh Nhẹn / Tinh Thần`.
- Mỗi lần Chuyển có một cấp Thí Luyện, áp dụng Hồi Báo đồng thời cho Base của cả bốn Thuộc Tính Cơ Bản.
- Thuộc Tính Đặc Biệt không nhận Hồi Báo Thí Luyện mặc định.
- **Không có Chiết Xuất**, hệ số `K`, hay đơn vị Thuộc Tính theo bậc Chuyển.

### Thí Luyện Khi Chuyển

| Cấp Thí Luyện | Hồi Báo lên Base |
|---:|---:|
| I | `×2` |
| II | `×5` |
| III | `×10` |
| IV | `×100` |

Công thức chuẩn:

$$
B_{\mathrm{sau}}=B_{\mathrm{truoc}}\times R
$$

Sau Chuyển, Chỉ Số và Tối Đa Tài Nguyên dẫn xuất được tính lại theo bảng tại [[THUỘC TÍNH#5. Chuyển Đổi Thuộc Tính → Chỉ Số/Tài Nguyên]]. Hồi Báo không tự nhân lặp các Chỉ Số đã có.

### Điểm Thuộc Tính Tự Do

- `1` Điểm Thuộc Tính Tự Do = `+1 Base` của một Thuộc Tính Cơ Bản, không phụ thuộc số lần Chuyển.
- Điểm được cộng trước Chuyển tham gia Hồi Báo; điểm cộng sau Chuyển không nhận Hồi Báo của lần đã qua.
- Nghề Nghiệp phẩm chất cao nhất độc hữu Nhân Vật Chính: `+10` điểm/level.
- Nhân vật khác: tối đa `+5` điểm/level từ Nghề Nghiệp.
- Lộ trình nhận điểm theo loại/phẩm chất Nghề Nghiệp vẫn **IN DESIGN**.

## Chưa Thiết Kế/Chưa Freeze

- Tên lore chính thức và điều kiện mở bốn cấp Thí Luyện.
- Điều kiện mở Chuyển và thời điểm nhận Hồi Báo.
- Phẩm Chất Nghề Nghiệp đầy đủ.
- Bảng progression level và Điểm Thuộc Tính của từng Nghề.
- Các mechanic Nghề Nghiệp khác.
