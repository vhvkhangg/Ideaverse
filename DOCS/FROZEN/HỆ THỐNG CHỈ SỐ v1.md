---
status: frozen
version: 1
system: Chỉ Số
---

# HỆ THỐNG CHỈ SỐ v1

> [!SUCCESS] FROZEN
> Tài liệu này ghi **decision log** của Hệ Thống Chỉ Số v1. Source of truth chi tiết: [[CHỈ SỐ]]. Nếu một quyết định ở đây được mở lại, đổi trạng thái tại [[DESIGN STATUS]] thành `REOPENED` trước khi sửa canonical rule.

## Frozen Decisions

### Kiến Trúc

- Chỉ Số chia `Cơ Sở / Trung Cấp / Thượng Cấp`.
- Tài Nguyên là subsystem riêng; Chỉ Số chỉ định nghĩa `<Tài Nguyên> Tối Đa`, hồi phục và các đại lượng liên quan.
- Các Chỉ Số có thể xuất hiện trên Trang Bị nếu mechanic cho phép.

> [!NOTE] Chuẩn hóa terminology sau freeze
> `Sinh Mệnh Tối Đa` được đổi tên thành **`Sinh Mệnh Lực Tối Đa`** để khớp [[SINH MỆNH LỰC]]. `Pháp Lực` và `Đấu Khí` được xác định là các loại [[NĂNG LƯỢNG]], không phải category Tài Nguyên hard-code. Đây là chỉnh terminology/taxonomy liên subsystem, không thay đổi công thức Chỉ Số v1.

### Modifier

- Offensive Modifier `%` độc lập stack **multiplicatively**.
- Modifier âm được phép khi mechanic cho phép; multiplier không âm.
- Các `% Kháng` thông thường dùng mô hình tiệm cận: giá trị hữu hạn không đạt 100% hiệu lực.
- `Miễn Nhiễm 100%` là mechanic riêng.
- `Kháng Chí Mạng` là ngoại lệ: giảm trực tiếp điểm phần trăm Crit Chance.

### Damage Taxonomy

- Loại: `Vật Lý / Pháp Thuật / Chuẩn`.
- Nguyên Tố là tag độc lập, không phải Loại Sát Thương thứ tư.
- Đối tượng: `Nhục Thể / Linh Hồn`.
- `Cận Chiến / Viễn Trình` là tag chỉ áp cho Nhục Thể.

### Chính Xác / Né Tránh

```text
P(hit) = Accuracy / (Accuracy + Evasion)
```

với trường hợp biên được định nghĩa tại [[CHỈ SỐ#7.1. Chính Xác ↔ Né Tránh]].

### Chí Mạng / Nhược Điểm

- Crit là RNG; Nhược Điểm là conditional/positional.
- Có thể xảy ra đồng thời.
- Multiplier Crit và Weak Point **nhân nhau**.
- Kháng ST Crit/Weak chỉ giảm phần bonus và dùng mô hình Kháng tiệm cận.
- Dung Sai Nhược Điểm mở rộng hitbox phán định, không đổi kích thước vật lý thật.

### Giáp / Kháng Phép

- Defense không âm.
- `Cố → Xuyên % → Xuyên Điểm`.
- Công thức defense:

```text
D_sau = D² / (D + Defense Hiệu Lực)
```

- Defense mạnh hơn trước nhiều hit nhỏ là chủ ý thiết kế.

### Kháng

- Các layer Kháng độc lập nhân phần damage còn lại.
- `Toàn Nguyên Tố` và Kháng nguyên tố cụ thể cùng áp dụng.
- Vật Lý/Pháp Thuật/Nguyên Tố Kháng Tính có thể âm để biểu diễn weakness.
- `Phòng Ngự Tuyệt Đối` dùng cùng mô hình tiệm cận.

### Sát Thương Chuẩn

Sát Thương Chuẩn bỏ qua mọi defense thông thường. Defense còn hiệu lực:

```text
Kháng Sát Thương Nhục Thể/Linh Hồn
→ Phòng Ngự Tuyệt Đối
→ Giảm Sát Thương Cuối Cùng
```

`Kháng Chí Mạng` vẫn có thể giảm xác suất Crit vì đây là phán định xác suất.

### Định Tính / Phụ Tố

- `Định Tính` là pool chung chống Khống Chế + Debuff (`Phụ Tố`).
- Định Tính floor `0`; Sức Phá dư bị mất.
- Khi Định Tính ở `0`, mọi Phụ Tố hợp lệ tiếp theo có thể được thiết lập trực tiếp.
- Hồi phục chỉ bắt đầu sau `Trì Hoãn Hồi Phục Định Tính` tính từ lần cuối nhận Sức Phá.
- Cấp Phụ Tố `I–X`; `901+ = X`; Internal Value không hard cap.
- Thời Gian/Cường Độ snapshot khi áp dụng; Kháng tăng sau đó không sửa Phụ Tố đang tồn tại.
- `Thời Gian Cộng Dồn Tối Đa Có Hiệu Lực` có thể được mechanic tăng/giảm; overflow mất hẳn.
- Không bắt buộc một công thức universal suy ra Sức Phá từ Thời Gian/Cường Độ.

### Kỹ Năng / Kênh Thi Triển

- Không có global `Tốc Độ Thi Triển` hoặc `Tốc Độ Hồi Chiêu`.
- Độ Thuần Thục đủ điều kiện → Kỹ Năng tăng Cấp; Cấp Kỹ Năng quyết định progression thông số.
- Cooldown bắt đầu sau khi Thi Triển/Duy Trì kết thúc.
- `Số Kênh Thi Triển` không hard cap; mỗi kênh có cooldown riêng theo từng Kỹ Năng.

## Deferred / Out of Scope

Không nằm trong freeze Chỉ Số v1:

- Công thức Thuộc Tính → Chỉ Số.
- Chi tiết Hệ Thống Tài Nguyên ngoài các pattern Chỉ Số liên quan.
- Progression chi tiết từng Kỹ Năng.
- Data/balance cụ thể cho từng Phụ Tố, Trang Bị, Nghề Nghiệp...
- Calculator/web triển khai các công thức.
