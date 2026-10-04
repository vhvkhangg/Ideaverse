---
status: frozen
version: 1
system: Tài Nguyên
---

# HỆ THỐNG TÀI NGUYÊN v1

> [!SUCCESS] FROZEN
> Decision log của Hệ Thống Tài Nguyên v1. Source of truth chi tiết: [[TÀI NGUYÊN]] và [[NĂNG LƯỢNG]]. Nếu mở lại một quyết định bên dưới, đổi trạng thái tại [[DESIGN STATUS]] thành `REOPENED` trước khi sửa canonical rule.

## Frozen Decisions

### Kiến Trúc

- Tài Nguyên là pool `Hiện Tại / Tối Đa`.
- Nhóm cốt lõi: `Sinh Mệnh Lực / Thể Lực / Tinh Lực / Năng Lượng`.
- `Pháp Lực`, `Đấu Khí`, `Linh Lực`, `Chân Nguyên`... là **loại Năng Lượng**, không phải category hard-code riêng.
- Một cá thể có thể sở hữu nhiều pool Năng Lượng độc lập.
- Pattern Chỉ Số: `<Tài Nguyên> Tối Đa / Hồi Phục <Tài Nguyên> / Tỷ Lệ Hồi Phục <Tài Nguyên>`.

### Phụ Tố Suy Giảm Tài Nguyên

Mỗi Tài Nguyên sau có một Phụ Tố nội sinh duy nhất:

```text
Sinh Mệnh Lực → Suy Nhược Sinh Mệnh
Thể Lực       → Suy Kiệt Thể Lực
Tinh Lực      → Suy Kiệt Tinh Lực
```

Mapping:

```text
>70%       → không có
(50,70]%   → I   / 100
(30,50]%   → II  / 200
(10,30]%   → IV  / 400
(5,10]%    → VI  / 600
(1,5]%     → VIII/ 800
(0,1]%     → X   / 1000
0%         → state transition riêng
```

- Phụ Tố này không phá Định Tính.
- Không có duration và không stack nhiều bậc.
- Cường Độ cập nhật động theo tỷ lệ hiện tại; đây là ngoại lệ với snapshot Phụ Tố thông thường.

### Trạng Thái 0%

- `Sinh Mệnh Lực = 0` → kích hoạt cơ chế Tử Vong, trừ mechanic đặc biệt can thiệp.
- `Thể Lực = 0` → không thể khởi tạo/duy trì hành động cần Thể Lực.
- `Tinh Lực = 0` → không thể khởi tạo/duy trì tác vụ cần Tinh Lực; không mặc định bất tỉnh.
- Một pool Năng Lượng = `0` → không thể thanh toán chi phí từ pool đó.

### Phẩm Chất Năng Lượng

```text
Vô Sắc   Q=1
Nhất Sắc Q=2
Nhị Sắc  Q=4
Tam Sắc  Q=16     ← Chất Biến
Tứ Sắc   Q=32
Ngũ Sắc  Q=64
Lục Sắc  Q=256    ← Chất Biến
Thất Sắc Q=512
Bát Sắc  Q=1024
Cửu Sắc  Q=4096   ← Chất Biến
Thập Sắc Q=16384  ← Chất Biến · Tuyệt Cao Vô Thượng
```

- `Vô → Cửu` là phạm vi thông thường.
- `Thập Sắc — Tuyệt Cao Vô Thượng` hiện thuộc Năng Lượng của Nhân Vật Chính.
- Bước thường `×2`; đi vào `Tam/Lục/Cửu/Thập` là `×4`.

### Độ Tinh Khiết

- Phẩm Chất không đặt trần Độ Tinh Khiết riêng theo từng Sắc.
- Vô Sắc và Cửu Sắc đều có thể đạt ví dụ `99%`.
- `Vô → Cửu` luôn `<100%` trong canonical v1.
- Năng Lượng Thập Sắc của Nhân Vật Chính có `100%` Độ Tinh Khiết.

### Hiệu Năng

```text
P = Độ Tinh Khiết / 100
E = Q × P
T = Số Lượng × Q × P
```

`E/T` là giá trị kỹ thuật để quy đổi, không phải multiplier damage universal.

### Tinh Luyện

```text
P₁ = P₀ + (1 - P₀) × R
A₁ = A₀ × (P₀ / P₁) × ηᵣ
```

- `0 ≤ R < 1` cho quá trình thông thường nên độ tinh khiết tiến tới nhưng không chạm 100%.
- `0 < ηᵣ ≤ 1`.
- Tinh luyện tăng Độ Tinh Khiết, không mặc định tăng Phẩm Chất.

### Thăng Phẩm

```text
A₁ = A₀ × (Q₀ × P₀) / (Q₁ × P₁) × ηₚ
```

với `0 < ηₚ ≤ 1` mặc định.

### Chuyển Hóa

```text
Aₜ = Aₛ × (Qₛ × Pₛ) / (Qₜ × Pₜ) × ηc
```

- Mặc định `0 < ηc ≤ 1`.
- Chuyển hóa không mặc định `1:1`.
- Không được tự tạo Hiệu Năng vô hạn; nếu tổng hiệu suất vượt 100%, mechanic phải chỉ ra nguồn Hiệu Năng bổ sung.

### Kỹ Năng & Phẩm Chất

- Kỹ Năng/Công Pháp có thể yêu cầu Phẩm Chất Năng Lượng tối thiểu.
- Quantity không mặc định thay thế Quality.
- Phẩm Chất/Độ Tinh Khiết có thể ảnh hưởng tiêu hao, uy lực và Đặc Tính nhưng không có multiplier universal bắt buộc.

## Deferred / Out of Scope

- Gói modifier cụ thể của ba Phụ Tố nội sinh.
- Taxonomy đầy đủ mọi loại Năng Lượng/Đặc Tính.
- Điều kiện Thăng Phẩm cụ thể của từng Công Pháp.
- Công thức từng Kỹ Năng khai thác `Q/P/E`.
- Balance cụ thể cho từng `R/η`.
