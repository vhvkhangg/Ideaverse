# HỆ THỐNG THUỘC TÍNH v1

**Status:** FROZEN  
**Source of Truth:** [[THUỘC TÍNH]]

## Frozen Decisions

### Phân loại

- Thuộc Tính Cơ Bản:
  - Sức Mạnh
  - Thể Chất
  - Nhanh Nhẹn
  - Tinh Thần
- Thuộc Tính Đặc Biệt:
  - Ngộ Tính
  - Mị Lực
  - Vận Khí

### Tăng trưởng

- Cơ Bản có thể tăng bằng level, Điểm Thuộc Tính Tự Do và các phương thức thông thường được hệ thống cho phép.
- Đặc Biệt chỉ thay đổi bằng phương thức đặc biệt/hiếm.

### Thang số

- Dùng thang tuyến tính.
- `1` là mốc cực hạn tự nhiên của người thường đối với thuộc tính tương ứng.
- Cho phép scientific notation khi số lớn, ví dụ `1e10`, `3e50`.
- Phân biệt Base và Effective.

### Giá trị âm

- Sức Mạnh, Thể Chất, Nhanh Nhẹn, Tinh Thần: Base và Effective không âm.
- Ngộ Tính: Base `>= 0`; modifier có thể làm Effective `< 0`.
- Mị Lực: Base và Effective có thể âm.
- Vận Khí: Base và Effective có thể âm.

### Chiết xuất

- Chỉ áp dụng cho 4 Thuộc Tính Cơ Bản.
- Gắn với 10 lần Chuyển Nghề, ký hiệu `I` đến `X`.
- Cách hiển thị: `Sức Mạnh I: x`, `Sức Mạnh II: x`, ...; không dùng `Sức Mạnh: x I`.
- Mọi lần Chuyển dùng cùng một hệ số chiết xuất cố định `K`.
- Giá trị `K` chưa được chốt.
- Chiết xuất đổi cấp biểu diễn, không tự làm giảm sức mạnh thực tế tại thời điểm Chuyển.

### Quy đổi xuyên thế giới

- Mọi power system đều được quy đổi về lớp Thuộc Tính chung của Ideaverse để so sánh.
- Hệ thống bản địa của từng thế giới vẫn được giữ nguyên; lớp Thuộc Tính không thay thế lore nguyên tác.

## Chưa Freeze

- Giá trị cụ thể của `K`.
- Quy tắc nhận và tiêu Điểm Thuộc Tính Tự Do.
- Công thức modifier chi tiết.
- Công thức từ Thuộc Tính sang Chỉ Số.
- Toàn bộ thiết kế Chỉ Số.
