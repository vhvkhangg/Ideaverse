---
type: system
status: frozen
version: 1
scope: resources
tags:
  - ideaverse/system/resource
---

# TÀI NGUYÊN

> [!SUCCESS] Source of Truth — FROZEN v1
> Đây là **nguồn định nghĩa canonical** cho Hệ Thống Tài Nguyên của Ideaverse. Bản đồ cấp cao hơn: [[HỆ THỐNG THIẾT LẬP]]. Các Chỉ Số dung lượng/hồi phục được định nghĩa tại [[CHỈ SỐ]]. Decision log: [[HỆ THỐNG TÀI NGUYÊN v1]].

## 1. Định Nghĩa

**Tài Nguyên** là đại lượng trạng thái có giá trị hiện tại và giới hạn tối đa, thường được biểu diễn dưới dạng:

```text
Giá Trị Hiện Tại / Giá Trị Tối Đa
```

Ví dụ:

```text
Thể Lực: 700 / 1.000
Chân Nguyên: 8.000 / 10.000
```

Tài Nguyên khác với Chỉ Số:

```text
Thể Lực Tối Đa: 1.000     ← Chỉ Số
Thể Lực: 700 / 1.000      ← Tài Nguyên
```

Theo mặc định:

- Giá Trị Hiện Tại có floor `0`.
- Giá Trị Hiện Tại không vượt Giá Trị Tối Đa, trừ khi mechanic ghi rõ cơ chế vượt giới hạn.
- Tăng/giảm Giá Trị Tối Đa không đồng nghĩa tự động hồi/tiêu hao cùng lượng Giá Trị Hiện Tại; mechanic gây thay đổi phải quy định cách xử lý nếu cần.
- Tỷ lệ phần trăm của Tài Nguyên được tính bằng `Hiện Tại / Tối Đa` sau khi các thay đổi hợp lệ lên Giá Trị Tối Đa đã được resolve.

## 2. Các Nhóm Tài Nguyên Cốt Lõi

- [[SINH MỆNH LỰC]]
- [[THỂ LỰC]]
- [[TINH LỰC]]
- [[NĂNG LƯỢNG]]

`Pháp Lực`, `Đấu Khí`, `Linh Lực`, `Chân Nguyên`, `Ma Nguyên`... là **các loại Năng Lượng cụ thể**, không phải các nhóm Tài Nguyên hard-code song song với Năng Lượng.

Một cá thể có thể đồng thời sở hữu nhiều pool Năng Lượng độc lập nếu Công Pháp, Nghề Nghiệp, Chủng Tộc, Thiên Phú hoặc mechanic khác cho phép.

## 3. Pattern Chỉ Số Liên Quan

Mỗi Tài Nguyên có thể liên kết với các Chỉ Số theo pattern:

```text
<Tài Nguyên> Tối Đa
Hồi Phục <Tài Nguyên>
Tỷ Lệ Hồi Phục <Tài Nguyên>
```

Ví dụ:

```text
Sinh Mệnh Lực Tối Đa
Hồi Phục Sinh Mệnh Lực
Tỷ Lệ Hồi Phục Sinh Mệnh Lực
```

hoặc:

```text
Chân Nguyên Tối Đa
Hồi Phục Chân Nguyên
Tỷ Lệ Hồi Phục Chân Nguyên
```

Giá Trị Tối Đa và tốc độ hồi phục có thể được tác động bởi [[THUỘC TÍNH]], Công Pháp, Nghề Nghiệp, Thiên Phú, Trang Bị, Kỹ Năng hoặc mechanic khác. **Không có công thức universal bắt buộc Thuộc Tính phải quy đổi sang Tài Nguyên theo một tỷ lệ cố định.**

## 4. Phụ Tố Nội Sinh Do Suy Giảm Tài Nguyên

Cơ chế này mặc định áp dụng cho:

- [[SINH MỆNH LỰC]] → **Suy Nhược Sinh Mệnh**;
- [[THỂ LỰC]] → **Suy Kiệt Thể Lực**;
- [[TINH LỰC]] → **Suy Kiệt Tinh Lực**.

Mỗi Tài Nguyên chỉ có **một Phụ Tố nội sinh duy nhất**; Cường Độ của Phụ Tố thay đổi động theo tỷ lệ Tài Nguyên hiện tại.

### 4.1. Mapping Canonical

| Tỷ lệ Tài Nguyên hiện tại | Cường Độ Nội Bộ | Cấp hiển thị |
|---:|---:|---:|
| `> 70%` | `0` | Không có Phụ Tố |
| `(50%, 70%]` | `100` | I |
| `(30%, 50%]` | `200` | II |
| `(10%, 30%]` | `400` | IV |
| `(5%, 10%]` | `600` | VI |
| `(1%, 5%]` | `800` | VIII |
| `(0%, 1%]` | `1000` | X |
| `0%` | — | Trạng thái biên riêng |

Các mức `III / V / VII / IX` không được dùng cho mapping mặc định này. Chúng vẫn tồn tại trong Hệ Thống Phụ Tố và có thể xuất hiện từ mechanic khác.

### 4.2. Quy Tắc Vận Hành

Các Phụ Tố suy giảm Tài Nguyên là **Phụ Tố Nội Sinh Duy Trì Theo Điều Kiện**:

- không cần phá [[CHỈ SỐ#15. Phụ Tố & Định Tính|Định Tính]] để được thiết lập;
- không có Thời Gian tồn tại cố định;
- không cộng dồn Thời Gian;
- không cộng dồn nhiều bậc cùng nguồn;
- tại mọi thời điểm chỉ Cường Độ tương ứng tỷ lệ hiện tại có hiệu lực;
- khi tỷ lệ giảm, Cường Độ tăng ngay theo mốc mới;
- khi tỷ lệ hồi phục, Cường Độ giảm hoặc Phụ Tố biến mất ngay theo mốc mới;
- đây là **ngoại lệ có chủ ý** đối với quy tắc snapshot của Phụ Tố thông thường.

Hệ Thống Tài Nguyên chỉ freeze **tên, điều kiện kích hoạt và Cường Độ**. Gói modifier/hậu quả chi tiết của từng Phụ Tố có thể được mở rộng trong catalog Phụ Tố mà không thay đổi mapping canonical trên.

## 5. Trạng Thái 0%

`0%` là **state transition**, không phải Cấp Phụ Tố cao hơn X.

### 5.1. Sinh Mệnh Lực = 0

Kích hoạt **cơ chế Tử Vong** đối với thực thể phụ thuộc Sinh Mệnh Lực.

Mechanic đặc biệt như Bất Tử, Hồi Sinh, mạng phụ, thay thế điều kiện tử vong hoặc chuyển tổn thất sang hệ khác có quyền can thiệp nếu ghi rõ.

### 5.2. Thể Lực = 0

- Không thể khởi tạo hành động yêu cầu tiêu hao Thể Lực.
- Hành động/Kỹ Năng cần duy trì Thể Lực không thể tiếp tục khi không còn đủ chi phí duy trì.
- Hành động không sử dụng Thể Lực vẫn có thể thực hiện nếu các điều kiện khác cho phép.

### 5.3. Tinh Lực = 0

- Không thể khởi tạo tác vụ/Kỹ Năng yêu cầu tiêu hao Tinh Lực.
- Không thể tiếp tục tác vụ cần duy trì Tinh Lực khi không còn đủ chi phí duy trì.
- Không mặc định mọi cá thể lập tức bất tỉnh; bất tỉnh/hôn mê phải đến từ Phụ Tố hoặc mechanic cụ thể.

### 5.4. Năng Lượng = 0

Một pool Năng Lượng ở `0` không thể thanh toán chi phí từ chính pool đó. Các pool Năng Lượng khác của cùng cá thể không bị cạn theo nếu mechanic không liên kết chúng.

## 6. Tiêu Hao & Hồi Phục

Một Tài Nguyên có thể thay đổi bởi:

- tiêu hao từ Kỹ Năng, hành động hoặc cơ chế;
- hồi phục tự nhiên;
- hồi phục flat;
- hồi phục theo `% Tối Đa`;
- vật phẩm, kỹ năng, môi trường hoặc hiệu ứng;
- chuyển hóa giữa các Tài Nguyên/Năng Lượng;
- tinh luyện đối với [[NĂNG LƯỢNG]].

Không mặc định mọi Tài Nguyên đều tự hồi phục. Điều kiện hồi phục thuộc định nghĩa của từng Tài Nguyên hoặc mechanic cung cấp nó.

## 7. Năng Lượng

[[NĂNG LƯỢNG]] là nhóm Tài Nguyên có thêm các trục:

- Loại Năng Lượng;
- Số Lượng;
- Phẩm Chất `Vô Sắc → Cửu Sắc`, cùng ngoại lệ `Thập Sắc — Tuyệt Cao Vô Thượng`;
- Độ Tinh Khiết;
- Đặc Tính;
- Tinh Luyện;
- Thăng Phẩm;
- Chuyển Hóa.

Công thức canonical: [[NĂNG LƯỢNG]].

## 8. Chuyển Hóa

Tài Nguyên/Năng Lượng chỉ chuyển hóa lẫn nhau khi mechanic cho phép. Không tồn tại tỷ lệ universal `1:1`.

Đối với Năng Lượng, chuyển hóa phải tuân theo nguyên tắc bảo toàn Hiệu Năng và Hiệu Suất Chuyển Hóa tại [[NĂNG LƯỢNG#10. Chuyển Hóa Năng Lượng]].

## 9. Quy Tắc Kiến Trúc

- Tài Nguyên lưu **trạng thái hiện tại**; Chỉ Số lưu **giới hạn và modifier vận hành**.
- Không hard-code mọi loại Năng Lượng vào schema chung.
- Một mechanic mới nên tái sử dụng pattern `<Tài Nguyên> Tối Đa / Hồi Phục / Tỷ Lệ Hồi Phục` nếu phù hợp trước khi tạo Chỉ Số mới.
- Năng Lượng cụ thể là instance; [[NĂNG LƯỢNG]] chỉ định nghĩa luật chung.

## 10. Deferred / Ngoài Phạm Vi Freeze v1

Các phần sau **không làm Hệ Thống Tài Nguyên v1 trở thành chưa hoàn thiện**:

- công thức Thuộc Tính → Chỉ Số Tài Nguyên;
- gói modifier chi tiết của `Suy Nhược Sinh Mệnh / Suy Kiệt Thể Lực / Suy Kiệt Tinh Lực`;
- taxonomy đầy đủ của mọi loại Năng Lượng và Đặc Tính;
- điều kiện cụ thể của từng Công Pháp để Thăng Phẩm;
- balance cụ thể của từng Kỹ Năng dùng Năng Lượng.
