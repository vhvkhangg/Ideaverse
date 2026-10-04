# CHỈ SỐ TRUNG CẤP

> [!ABSTRACT]
> Chỉ Số Trung Cấp là các đại lượng chuyên biệt hơn Cơ Sở, chủ yếu tác động vào phán định đòn đánh, Chí Mạng, Nhược Điểm, Đón Đỡ, Xuyên phòng, Kháng Tính, modifier sát thương và Hút Máu.

> [!INFO] Quy tắc & công thức chung
> [[CHỈ SỐ]]

## 1. Chính Xác & Né Tránh

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Chính Xác** | Điểm | Khả năng khiến đòn đánh/Kỹ Năng hợp lệ đánh trúng. |
| **Né Tránh** | Điểm | Khả năng tránh một đòn đánh/Kỹ Năng có thể né. |

Công thức canonical: `P(hit) = Chính Xác / (Chính Xác + Né Tránh)` với các trường hợp biên tại [[CHỈ SỐ#7.1. Chính Xác ↔ Né Tránh]].

## 2. Chí Mạng

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tỷ Lệ Chí Mạng** | % | Xác suất instance hợp lệ trở thành Chí Mạng. |
| **Kháng Chí Mạng** | % | Trừ trực tiếp theo điểm phần trăm vào Tỷ Lệ Chí Mạng; có thể overcap. |
| **Sát Thương Chí Mạng** | × | Multiplier khi Chí Mạng xảy ra. |
| **Kháng Sát Thương Chí Mạng** | % Kháng | Chỉ giảm bonus Crit bằng mô hình Kháng tiệm cận. |

`Kháng Chí Mạng` là ngoại lệ không dùng công thức Kháng tiệm cận; `Kháng Sát Thương Chí Mạng` thì có.

## 3. Nhược Điểm

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Dung Sai Nhược Điểm** | % | Mở rộng vùng phán định nhưng không đổi kích thước vật lý thật. |
| **Sát Thương Nhược Điểm** | × | Multiplier khi đánh trúng Nhược Điểm. |
| **Kháng Sát Thương Nhược Điểm** | % Kháng | Chỉ giảm bonus Nhược Điểm theo mô hình Kháng tiệm cận. |

Không có `Tỷ Lệ Nhược Điểm`. Crit và Nhược Điểm có thể đồng thời xảy ra và **nhân multiplier**.

## 4. Đón Đỡ

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tỷ Lệ Đón Đỡ** | % | Xác suất Đón Đỡ instance hợp lệ. |
| **Hiệu Quả Đón Đỡ** | % | Tỷ lệ damage giảm khi Đón Đỡ thành công. |

Đón Đỡ được resolve trước Giáp/Kháng Phép.

## 5. Xuyên Phòng

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Xuyên Giáp** | Điểm | Bỏ qua Giáp có thể bị xuyên theo Điểm. |
| **Tỷ Lệ Xuyên Giáp** | % | Bỏ qua tỷ lệ Giáp có thể bị xuyên. |
| **Xuyên Kháng Phép** | Điểm | Bỏ qua Kháng Phép có thể bị xuyên theo Điểm. |
| **Tỷ Lệ Xuyên Kháng Phép** | % | Bỏ qua tỷ lệ Kháng Phép có thể bị xuyên. |

Thứ tự canonical: **Cố → Xuyên % → Xuyên Điểm**. Công thức: [[CHỈ SỐ#9. Giáp, Kháng Phép, Cố Giáp/Cố Kháng Phép & Xuyên]].

## 6. Tăng Sát Thương Theo Loại

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Sát Thương Vật Lý** | % | Modifier cho instance Vật Lý. |
| **Tăng Sát Thương Pháp Thuật** | % | Modifier cho instance Pháp Thuật. |

Các Offensive Modifier độc lập **nhân**. `Tăng Sát Thương Chuẩn` thuộc Thượng Cấp.

## 7. Kháng Tính

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Vật Lý Kháng Tính** | % Kháng | Layer Kháng cho Sát Thương Vật Lý; có thể âm. |
| **Pháp Thuật Kháng Tính** | % Kháng | Layer Kháng cho Sát Thương Pháp Thuật; có thể âm. |
| **Toàn Nguyên Tố Kháng Tính** | % Kháng | Tác động lên mọi instance mang tag Nguyên Tố. |
| **`<Nguyên Tố> Kháng Tính`** | % Kháng | Kháng riêng cho Hỏa/Băng/Lôi/...; có thể âm. |

Mọi nguồn được chuyển qua mô hình Kháng tiệm cận rồi **nhân phần damage còn lại**. Toàn Nguyên Tố và Kháng nguyên tố riêng cùng áp dụng nếu instance có tag phù hợp.

## 8. Cận Chiến & Viễn Trình

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Sát Thương Cận Chiến** | % | Offensive Modifier cho instance Nhục Thể có tag Cận Chiến. |
| **Kháng Sát Thương Cận Chiến** | % Kháng | Kháng damage Nhục Thể tag Cận Chiến. |
| **Tăng Sát Thương Viễn Trình** | % | Offensive Modifier cho instance Nhục Thể có tag Viễn Trình. |
| **Kháng Sát Thương Viễn Trình** | % Kháng | Kháng damage Nhục Thể tag Viễn Trình. |

Cận/Viễn dựa trên **tag**, không dựa khoảng cách thực tế và không áp cho Linh Hồn.

## 9. Hút Máu

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Hút Máu Đòn Đánh** | % | Hồi Sinh Mệnh dựa trên damage thực tế hợp lệ từ Đòn Đánh. |
| **Hút Máu Kỹ Năng** | % | Hồi Sinh Mệnh dựa trên damage thực tế hợp lệ từ Kỹ Năng. |

Mặc định không áp cho DoT/Phụ Tố, phản sát thương, môi trường hoặc summon/thực thể khác.

## 10. Định Tính Chuyên Sâu

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Trì Hoãn Hồi Phục Định Tính** | giây | Thời gian từ lần cuối nhận Sức Phá tới khi bắt đầu hồi Định Tính. |

Chỉ Số này có thể bị modifier bởi Kỹ Năng, Trang Bị hoặc mechanic khác.
