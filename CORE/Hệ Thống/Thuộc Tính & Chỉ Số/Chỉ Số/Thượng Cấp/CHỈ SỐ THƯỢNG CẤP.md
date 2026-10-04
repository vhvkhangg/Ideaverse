# CHỈ SỐ THƯỢNG CẤP

> [!ABSTRACT]
> Chỉ Số Thượng Cấp là các đại lượng hiếm hoặc can thiệp vào layer sâu: Hút Máu toàn diện, Sát Thương Chuẩn, Nhục Thể/Linh Hồn, tầm hiệu lực, Phụ Tố/Định Tính, Cố Giáp/Cố Kháng Phép, phòng ngự cuối và đa kênh Thi Triển.

> [!INFO] Quy tắc & công thức chung
> [[CHỈ SỐ]]

## 1. Hút Máu Toàn Phần

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Hút Máu Toàn Phần** | % | Hồi Sinh Mệnh từ damage thực tế hợp lệ của cả Đòn Đánh và Kỹ Năng. |

Mặc định không tự bao gồm DoT/Phụ Tố, phản sát thương, môi trường hoặc summon khác.

## 2. Sát Thương Chuẩn

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Sát Thương Chuẩn** | % | Offensive Modifier cho instance Sát Thương Chuẩn. |

Sát Thương Chuẩn bỏ qua mọi layer phòng thủ thông thường; phía phòng thủ chỉ còn `Kháng Sát Thương Nhục Thể/Linh Hồn`, `Phòng Ngự Tuyệt Đối`, `Giảm Sát Thương Cuối Cùng`. Chi tiết: [[CHỈ SỐ#12. Sát Thương Chuẩn]].

## 3. Nhục Thể & Linh Hồn

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Sát Thương Nhục Thể** | % | Offensive Modifier cho instance tác động Nhục Thể. |
| **Kháng Sát Thương Nhục Thể** | % Kháng | Kháng damage Nhục Thể theo mô hình tiệm cận. |
| **Tăng Sát Thương Linh Hồn** | % | Offensive Modifier cho instance tác động Linh Hồn. |
| **Kháng Sát Thương Linh Hồn** | % Kháng | Kháng damage Linh Hồn theo mô hình tiệm cận. |

Cận/Viễn chỉ áp cho Nhục Thể.

## 4. Tầm Hiệu Lực

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Tầm Đánh** | % | Tăng Tầm Đánh cơ sở của Vũ Khí/đòn đánh. |
| **Tăng Tầm Kỹ Năng** | % | Tăng Tầm Kỹ Năng cơ sở. |
| **Tăng Phạm Vi Ảnh Hưởng** | % | Tăng kích thước tuyến tính của AoE/phạm vi hợp lệ. |

Base range thuộc Vũ Khí/Kỹ Năng. Modifier độc lập nhân theo [[CHỈ SỐ#17. Tầm Hiệu Lực]].

## 5. Sức Phá Định Tính

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Tăng Sức Phá Định Tính** | % | Offensive Modifier cho Sức Phá Định Tính hợp lệ. |
| **Kháng Sức Phá Định Tính** | % Kháng | Giảm Sức Phá nhận vào theo mô hình Kháng tiệm cận. |

Không có công thức universal bắt buộc Sức Phá phải suy ra từ Thời Gian/Cường Độ; Phụ Tố/Kỹ Năng định nghĩa Sức Phá cơ sở riêng.

## 6. Phụ Tố — Thời Gian & Cường Độ

### 6.1. Khống Chế

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Giảm Thời Gian Khống Chế** | giây | Giảm flat duration nhận vào. |
| **Kháng Thời Gian Khống Chế** | % Kháng | Giảm duration theo mô hình Kháng tiệm cận. |
| **Tăng Thời Gian Khống Chế** | % | Tăng duration do bản thân áp dụng. |
| **Giảm Cường Độ Khống Chế** | Điểm | Giảm flat Cường Độ Nội Bộ. |
| **Kháng Cường Độ Khống Chế** | % Kháng | Giảm Cường Độ theo mô hình Kháng tiệm cận. |
| **Tăng Cường Độ Khống Chế** | % | Tăng Cường Độ do bản thân áp dụng. |

### 6.2. Debuff

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Giảm Thời Gian Debuff** | giây | Giảm flat duration nhận vào. |
| **Kháng Thời Gian Debuff** | % Kháng | Giảm duration theo mô hình Kháng tiệm cận. |
| **Tăng Thời Gian Debuff** | % | Tăng duration do bản thân áp dụng. |
| **Giảm Cường Độ Debuff** | Điểm | Giảm flat Cường Độ Nội Bộ. |
| **Kháng Cường Độ Debuff** | % Kháng | Giảm Cường Độ theo mô hình Kháng tiệm cận. |
| **Tăng Cường Độ Debuff** | % | Tăng Cường Độ do bản thân áp dụng. |

`Giảm` = flat; `Kháng` = mô hình `% Kháng`; `Tăng` = offensive modifier multiplicative.

## 7. Cố Giáp & Cố Kháng Phép

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Cố Giáp** | % | Tỷ lệ Giáp được bảo vệ khỏi Xuyên Giáp thông thường. |
| **Cố Kháng Phép** | % | Tỷ lệ Kháng Phép được bảo vệ khỏi Xuyên Kháng Phép thông thường. |

Nhiều nguồn Cố dùng coverage multiplicative; thứ tự canonical là **Cố → Xuyên % → Xuyên Điểm**.

## 8. Phòng Ngự Cuối

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Phòng Ngự Tuyệt Đối** | % Kháng | Layer universal dùng mô hình Kháng tiệm cận; giảm cả Sát Thương Chuẩn. |
| **Giảm Sát Thương Cuối Cùng** | Điểm | Flat cuối cùng trên từng damage instance sau Phòng Ngự Tuyệt Đối. |

Không thể đạt miễn nhiễm bằng stacking Phòng Ngự Tuyệt Đối hữu hạn; `Miễn Nhiễm` là mechanic riêng.

## 9. Số Kênh Thi Triển

| Chỉ Số | Đơn Vị | Ý Nghĩa |
|---|---:|---|
| **Số Kênh Thi Triển** | số nguyên | Số kênh độc lập có thể Thi Triển Kỹ Năng; không hard cap toàn hệ thống. |

Tên hiển thị:

```text
1 → Thi Triển
2 → Song Trọng Thi Triển
3 → Tam Trọng Thi Triển
4 → Tứ Trọng Thi Triển
...
```

Mỗi kênh:

1. hoạt động đồng thời với kênh khác;
2. bị chiếm trong toàn bộ Thời Gian Thi Triển/Duy Trì;
3. có bảng Hồi Chiêu riêng cho từng Kỹ Năng;
4. cooldown Kỹ Năng A không khóa Kỹ Năng B sau khi kênh rảnh;
5. cùng Kỹ Năng có thể dùng trên nhiều kênh nếu cooldown tương ứng sẵn sàng;
6. mỗi instance trả Tài Nguyên và phán định Crit, Weak Point, Phụ Tố, Hút Máu, damage, proc độc lập.

Hồi chiêu bắt đầu sau khi Thi Triển/Duy Trì kết thúc.
