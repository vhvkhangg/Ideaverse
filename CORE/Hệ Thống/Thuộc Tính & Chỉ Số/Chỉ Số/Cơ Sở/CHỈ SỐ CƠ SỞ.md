# CHỈ SỐ CƠ SỞ

> [!ABSTRACT]
> Chỉ Số Cơ Sở là các đại lượng nền tảng dùng để mô tả một cá thể chiến đấu. `Cơ Sở` không có nghĩa là dễ tăng; một Chỉ Số Cơ Sở vẫn có thể bị giới hạn bởi hệ thống, chủng tộc, cấp độ, Trang Bị hoặc nguồn tăng trưởng hiếm.

> [!INFO] Quy tắc & công thức chung
> [[CHỈ SỐ]]

## 1. Sinh Mệnh & Tài Nguyên

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Sinh Mệnh Lực Tối Đa** | Điểm | Giới hạn [[SINH MỆNH LỰC]]. Giá trị Sinh Mệnh Lực hiện tại thuộc [[TÀI NGUYÊN]]. |
| **`<Tài Nguyên> Tối Đa`** | Điểm | Pattern dung lượng tối đa cho mọi Tài Nguyên, bao gồm từng loại [[NĂNG LƯỢNG]]. |
| **`Hồi Phục <Tài Nguyên>`** | Điểm/s | Hồi phục flat mỗi giây khi điều kiện hồi phục được thỏa mãn. |
| **`Tỷ Lệ Hồi Phục <Tài Nguyên>`** | % Tối Đa/s | Hồi phục dựa trên giá trị Tối Đa mỗi giây. |

Không hard-code danh sách Tài Nguyên hoặc danh sách loại Năng Lượng. Tài Nguyên mới có thể dùng cùng pattern mà không sửa schema Chỉ Số. `Pháp Lực` và `Đấu Khí` được xem là các loại [[NĂNG LƯỢNG]], không phải category hard-code riêng.

## 2. Định Tính

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Định Tính Tối Đa** | Điểm | Dung lượng tối đa của pool Định Tính chống thiết lập Phụ Tố. |
| **Hồi Phục Định Tính** | Điểm/s | Lượng hồi phục flat mỗi giây sau Trì Hoãn Hồi Phục. |
| **Tỷ Lệ Hồi Phục Định Tính** | % Tối Đa/s | Lượng hồi dựa trên Định Tính Tối Đa mỗi giây. |

Công thức canonical xem [[CHỈ SỐ#15.5. Hồi Phục Định Tính]].

## 3. Công & Phòng Cơ Bản

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Công Vật Lý** | Điểm | Nền tảng offensive cho cơ chế Sát Thương Vật Lý; không đồng nhất với Thuộc Tính [[Sức Mạnh]]. |
| **Công Pháp Thuật** | Điểm | Nền tảng offensive cho cơ chế Sát Thương Pháp Thuật. |
| **Giáp** | Điểm | Defense Điểm cho Sát Thương Vật Lý. |
| **Kháng Phép** | Điểm | Defense Điểm cho Sát Thương Pháp Thuật. |

`Giáp/Kháng Phép` đi qua công thức `D²/(D + Defense Hiệu Lực)`; xem [[CHỈ SỐ#9. Giáp, Kháng Phép, Cố Giáp/Cố Kháng Phép & Xuyên]].

## 4. Tốc Độ

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tốc Độ Đánh** | đòn/s | Tốc độ tấn công cơ sở trước modifier vũ khí và hiệu ứng. |
| **Tốc Độ Di Chuyển** | m/s | Tốc độ di chuyển thực tế trước modifier/cơ chế di chuyển đặc biệt. |

### Modifier Vũ Khí cho Tốc Độ Đánh

```text
Tốc Độ Đánh cá thể: 10 đòn/s

Chùy:    ×0.8 → 8/s
Nắm Đấm: ×1.0 → 10/s
Dao Găm: ×1.2 → 12/s
```

Nhiều modifier `%` độc lập dùng quy tắc multiplicative của [[CHỈ SỐ#3.2. Modifier Phần Trăm Thông Thường]].

## 5. Ghi Chú

- `Tầm Đánh`, `Tầm Kỹ Năng`, `Phạm Vi Ảnh Hưởng` cơ sở thuộc Vũ Khí/Kỹ Năng; nhân vật chỉ có modifier tương ứng ở Thượng Cấp.
- Không tồn tại Chỉ Số toàn nhân vật `Tốc Độ Thi Triển` hoặc `Tốc Độ Hồi Chiêu`.
