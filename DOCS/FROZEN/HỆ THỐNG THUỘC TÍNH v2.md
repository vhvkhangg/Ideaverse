---
status: frozen
version: 2
system: Thuộc Tính
supersedes: HỆ THỐNG THUỘC TÍNH v1
---

# HỆ THỐNG THUỘC TÍNH v2

> [!SUCCESS] FROZEN — HIỆN HÀNH
> Đây là quyết định canonical của Hệ Thống Thuộc Tính từ v2. Source of truth: [[THUỘC TÍNH]]. Bản v1: [[HỆ THỐNG THUỘC TÍNH v1]] (SUPERSEDED, chỉ đọc như lịch sử). Thay đổi mới phải được mở lại tại [[DESIGN STATUS]] trước khi sửa quy tắc.

## 1. Phần Giữ Nguyên Từ v1

- Bốn Thuộc Tính Cơ Bản: `Sức Mạnh / Thể Chất / Nhanh Nhẹn / Tinh Thần`.
- Ba Thuộc Tính Đặc Biệt: `Ngộ Tính / Mị Lực / Vận Khí`.
- Thang tuyến tính `0 / ~0.5 / 1 / >1`, không hard cap, cho phép scientific notation.
- Base tăng trưởng vĩnh viễn; Effective từ Base + flat rồi nhân `%` modifier độc lập; quy tắc số âm giữ như v1.
- Một Điểm Thuộc Tính Tự Do `= +1 Base` của một Thuộc Tính Cơ Bản; MC tối đa phẩm chất Nghề Nghiệp có `+10` điểm/level, nhân vật khác tối đa `+5` điểm/level, vật phẩm trao điểm cực hiếm.
- Thuộc Tính Đặc Biệt không nhận Điểm Tự Do thông thường; Ngộ Tính/Mị Lực/Vận Khí giữ vai trò và giới hạn phán định đã xác định trong v1.

## 2. Bãi Bỏ Cơ Chế Chiết Xuất

- Bỏ **toàn bộ Chiết Xuất Thuộc Tính**, `K`, `C_r`, `Equivalent` và công thức chia/nén sau Chuyển.
- `I–X` chỉ đánh dấu **bậc Chuyển Nghề Nghiệp**; tên Thuộc Tính luôn là `Sức Mạnh`, `Thể Chất`, `Nhanh Nhẹn`, `Tinh Thần` (không có hậu tố).
- Mọi nhân vật so sánh trên cùng thang Thuộc Tính trực tiếp; không có hệ số quy đổi lịch sử Thí Luyện.

## 3. Thưởng Thí Luyện Khi Chuyển

Giữ 10 lần Chuyển. Mỗi lần Chuyển có bốn cấp Thí Luyện, tăng trực tiếp Base của cả bốn Thuộc Tính Cơ Bản:

| Cấp Thí Luyện | R |
|---|---:|
| I | `×2` |
| II | `×5` |
| III | `×10` |
| IV | `×100` |

$$
B_{\mathrm{sau}}=B_{\mathrm{truoc}}\times R
$$

Điểm Tự Do đã phân bổ trước Chuyển tham gia thưởng; điểm phân bổ sau Chuyển không hồi tố thưởng đã nhận. Thí Luyện không tự nhân riêng mọi Chỉ Số dẫn xuất hoặc giá trị Tài Nguyên hiện tại: phải tính lại theo Thuộc Tính mới.

## 4. Chuyển Đổi Mặc Định Sang Chỉ Số Cơ Sở

**Mỗi +1 Thuộc Tính Effective** tạo đóng góp trước modifier Chỉ Số:

| Thuộc Tính | Chỉ Số Cơ Sở |
|---|---|
| Sức Mạnh | `+10 Công Vật Lý` |
| Thể Chất | `+100 Sinh Mệnh Lực Tối Đa`, `+100 Thể Lực Tối Đa`, `+5 Giáp`, `+10 Định Tính Tối Đa` |
| Nhanh Nhẹn | `+2 đòn/s Tốc Độ Đánh`, `+8 m/s Tốc Độ Di Chuyển` |
| Tinh Thần | `+10 Công Pháp Thuật`, `+100 Tinh Lực Tối Đa`, `+5 Kháng Phép`, `+10 Định Tính Tối Đa` |

`Định Tính Tối Đa` nhận cả Thể Chất lẫn Tinh Thần. Không chuyển trực tiếp thành hồi phục `% Tối Đa/s` (cũng không mặc định có hồi phục flat từ bảng này).

## 5. Chuyển Đổi Mặc Định Sang Chỉ Số Trung Cấp

**Mỗi +10 Thuộc Tính Effective** tạo:

| Thuộc Tính | Chỉ Số Trung Cấp |
|---|---|
| Sức Mạnh | `+1 Xuyên Giáp` (Điểm) |
| Thể Chất | `+1 Giá Trị Vật Lý Kháng Tính` (`R`) |
| Nhanh Nhẹn | `+1 Chính Xác`, `+1 Né Tránh` (Điểm) |
| Tinh Thần | `+1 Xuyên Kháng Phép` (Điểm), `+1 Giá Trị Pháp Thuật Kháng Tính` (`R`) |

Công thức tuyến tính, **không làm tròn theo mốc**: `15 Nhanh Nhẹn = +1.5 Chính Xác, +1.5 Né Tránh`. `+1 Giá Trị Kháng R` không phải giảm trực tiếp `1%` damage; dùng mô hình Kháng tiệm cận của [[CHỈ SỐ]].

## 6. Năng Lượng và Những Nhóm Không Chuyển Đổi

Một pool [[NĂNG LƯỢNG]] đã mở khóa, tương thích Tinh Thần, nhận dung lượng dẫn xuất `100 × Tinh Thần Effective × C_tương thích`; pool khác độc lập. `C=0` là không nhận đóng góp; `C=1` là chuẩn một pool tương thích, hệ số khác phải được mechanic sở hữu khai báo. Không tự mở khóa hoặc tạo pool mới.

**Không chuyển đổi trực tiếp/mặc định** từ Thuộc Tính vào:

- **mọi Chỉ Số Thượng Cấp**;
- Chỉ Số **xác suất** (Crit Chance, Block Chance...) hoặc Kháng Chí Mạng;
- **Hút Máu**;
- các `% Tăng Sát Thương` theo Loại/tag;
- hồi phục `% Tối Đa/s`.

Chính Xác/Né Tránh là **Điểm**, nên được nhận đóng góp; Kháng Tính `R` là giá trị Kháng, không phải xác suất. Các Chỉ Số không liệt kê trong bảng **không** được tự suy ra từ Thuộc Tính.

## 7. Công Thức Đóng Góp & Nguồn Ngoại Lệ

$$
Contribution_s=\sum_i EffectiveAttribute_i\times c_{i,s}
$$

Cộng thêm các nguồn Chỉ Số độc lập rồi xử lý modifier riêng theo [[CHỈ SỐ]]. Nguồn như Công Pháp, Nghề Nghiệp, Thiên Phú hoặc Kỹ Năng có thể bổ sung/chỉnh hệ số đã định nghĩa, nhưng phải ghi rõ mục tiêu, cách cộng/nhân, không được tính đúp một đóng góp. Không thay đổi cơ chế Giáp, Kháng, damage pipeline hoặc quy tắc Tài Nguyên v1.

## 8. Quan Hệ Phiên Bản

- `Thuộc Tính v2`: **FROZEN**, hiện hành.
- `Thuộc Tính v1`: **SUPERSEDED**, chỉ lưu lịch sử, không dùng Chiết Xuất/Equivalent nữa.
- `Chỉ Số v1` và `Tài Nguyên v1`: vẫn **FROZEN** về công thức cơ chế. Bảng chuyển đổi giá trị sang chúng do Thuộc Tính v2 sở hữu.
- `Nghề Nghiệp`: vẫn **IN DESIGN** ngoài phần cross-system contract ở trên.

Bảng, ví dụ và công thức chi tiết: [[THUỘC TÍNH]].
