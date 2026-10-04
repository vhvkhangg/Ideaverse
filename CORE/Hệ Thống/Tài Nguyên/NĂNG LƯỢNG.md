---
type: resource-system
status: frozen
version: 1
resource-category: energy
tags:
  - ideaverse/system/resource
  - ideaverse/system/energy
---

# NĂNG LƯỢNG

> [!SUCCESS] Source of Truth — FROZEN v1
> Đây là nguồn định nghĩa canonical cho **Năng Lượng** trong [[TÀI NGUYÊN]]. `Pháp Lực`, `Đấu Khí`, `Linh Lực`, `Chân Nguyên`... là các loại Năng Lượng cụ thể, không phải subsystem song song.

## 1. Định Nghĩa

**Năng Lượng** là nhóm Tài Nguyên dùng làm nguồn vận hành cho Công Pháp, Kỹ Năng, Võ Kỹ, Ma Pháp hoặc hệ thống sức mạnh tương đương.

Mỗi loại Năng Lượng là một pool độc lập:

```text
<Tên Năng Lượng>: hiện tại / tối đa
```

Ví dụ:

```text
Chân Nguyên: 8.000 / 10.000
Pháp Lực: 2.500 / 4.000
```

Một cá thể có thể đồng thời sở hữu nhiều loại Năng Lượng nếu mechanic cho phép.

## 2. Các Trục Mô Tả Độc Lập

Một pool Năng Lượng có các trục chính:

1. **Loại Năng Lượng** — bản chất/nguồn gốc, ví dụ Pháp Lực, Đấu Khí, Chân Nguyên.
2. **Số Lượng** — `Hiện Tại / Tối Đa`.
3. **Phẩm Chất** — cấp độ bản chất của Năng Lượng.
4. **Độ Tinh Khiết** — tỷ lệ thành phần tinh thuần.
5. **Đặc Tính** — tính chất/hiệu ứng riêng của loại Năng Lượng.

Phẩm Chất và Độ Tinh Khiết **không đồng nhất** và không ràng buộc tuyến tính với nhau.

## 3. Phẩm Chất Năng Lượng

### 3.1. Thứ Tự & Hệ Số Phẩm Chất

| Bậc | Phẩm Chất | Hệ Số Phẩm Chất `Q` | Ghi Chú |
|---:|---|---:|---|
| 0 | Vô Sắc | `1` | Mốc nền |
| 1 | Nhất Sắc | `2` | |
| 2 | Nhị Sắc | `4` | |
| 3 | Tam Sắc | `16` | **Chất Biến** |
| 4 | Tứ Sắc | `32` | |
| 5 | Ngũ Sắc | `64` | |
| 6 | Lục Sắc | `256` | **Chất Biến** |
| 7 | Thất Sắc | `512` | |
| 8 | Bát Sắc | `1024` | |
| 9 | Cửu Sắc | `4096` | **Chất Biến** |
| 10 | **Thập Sắc — Tuyệt Cao Vô Thượng** | `16384` | **Chất Biến · Vượt Giới Hạn** |

Quy luật progression:

- bước thông thường tăng `×2`;
- khi **đi vào** `Tam Sắc`, `Lục Sắc`, `Cửu Sắc`, `Thập Sắc`, Hệ Số tăng `×4` so với bậc ngay trước;
- các mốc trên được gọi là **mốc Chất Biến**.

`Vô Sắc → Cửu Sắc` là phạm vi Phẩm Chất thông thường. `Thập Sắc — Tuyệt Cao Vô Thượng` là Phẩm Chất vượt giới hạn, hiện thuộc Năng Lượng của [[NHÂN VẬT CHÍNH]].

### 3.2. Vai Trò

Phẩm Chất mô tả **cấp độ bản chất và tiềm năng trên mỗi đơn vị Năng Lượng**.

Phẩm Chất cao hơn có thể cho phép mechanic:

- giảm tiêu hao Năng Lượng của Kỹ Năng;
- tăng hiệu quả/uy lực Kỹ Năng;
- tăng cường hoặc mở khóa Đặc Tính;
- đáp ứng yêu cầu Phẩm Chất tối thiểu;
- áp đảo Năng Lượng Phẩm Chất thấp hơn khi rule cụ thể cho phép.

`Q` là **hệ số chuẩn để quy đổi Hiệu Năng**, không phải mặc định `×Q Sát Thương` cho mọi Kỹ Năng.

## 4. Độ Tinh Khiết

**Độ Tinh Khiết** biểu diễn tỷ lệ thành phần Năng Lượng thực sự tinh thuần trong một pool.

Gọi:

```text
P = Độ Tinh Khiết / 100
```

Ví dụ:

```text
80%    → P = 0.8
99.99% → P = 0.9999
```

### 4.1. Quan Hệ Với Phẩm Chất

Phẩm Chất **không đặt trần Độ Tinh Khiết khác nhau theo từng Sắc**.

Ví dụ đều hợp lệ:

```text
Vô Sắc — 99%
Cửu Sắc — 99%
```

Canonical v1:

- Năng Lượng `Vô Sắc → Cửu Sắc` có `P < 1`;
- có thể tiến gần `100%` tùy ý nhưng không tự nhiên chạm `100%`;
- **Năng Lượng Thập Sắc của Nhân Vật Chính có Độ Tinh Khiết = 100%**.

### 4.2. Vai Trò

Độ Tinh Khiết phản ánh **mức khai thác thực tế** của Phẩm Chất và có thể được mechanic dùng để xác định:

- hiệu suất sử dụng;
- mức hao hụt/lãng phí;
- độ ổn định và khả năng kiểm soát;
- mức phát huy Đặc Tính;
- nguy cơ tạp chất/phản phệ.

## 5. Hiệu Năng Năng Lượng

### 5.1. Hiệu Năng Trên Mỗi Đơn Vị

Gọi:

- `Q` = Hệ Số Phẩm Chất;
- `P` = Độ Tinh Khiết chuẩn hóa.

**Hệ Số Hiệu Năng**:

```text
E = Q × P
```

`E` mô tả Hiệu Năng hữu dụng tương đối trên mỗi đơn vị Năng Lượng.

### 5.2. Tổng Hiệu Năng

Với `A` là Số Lượng Năng Lượng:

```text
T = A × Q × P
```

`T` dùng làm đại lượng chuẩn khi tinh luyện, Thăng Phẩm hoặc chuyển hóa cần bảo toàn Hiệu Năng.

> [!IMPORTANT]
> `E` và `T` là **giá trị kỹ thuật nội bộ**. Không mặc định Kỹ Năng gây Sát Thương bằng `Damage × E`. Từng Kỹ Năng/Công Pháp quyết định cách tận dụng Phẩm Chất, Độ Tinh Khiết và Đặc Tính.

## 6. Đặc Tính Năng Lượng

**Đặc Tính** thuộc về loại Năng Lượng, không thuộc trực tiếp về Sắc.

Ví dụ:

```text
Xích Viêm Chân Nguyên
Phẩm Chất: Ngũ Sắc
Độ Tinh Khiết: 93%
Đặc Tính:
- Hỏa
- Thiêu Đốt
- Xâm Thực
```

Hai Năng Lượng cùng Phẩm Chất có thể có Đặc Tính hoàn toàn khác nhau.

Phẩm Chất và Độ Tinh Khiết có thể làm Đặc Tính mạnh hơn, ổn định hơn hoặc mở thêm hiệu ứng nếu mechanic cụ thể quy định.

## 7. Yêu Cầu Phẩm Chất

Kỹ Năng, Công Pháp hoặc mechanic có thể yêu cầu **Phẩm Chất Năng Lượng tối thiểu**.

Ví dụ:

```text
Yêu cầu: Năng Lượng ≥ Thất Sắc
```

Mặc định:

- Năng Lượng thấp hơn yêu cầu không thể thanh toán yêu cầu Phẩm Chất chỉ bằng cách tăng Số Lượng;
- Quantity không tự thay thế Quality;
- mechanic đặc biệt có thể bypass hoặc thay đổi rule nếu ghi rõ.

## 8. Tinh Luyện Độ Tinh Khiết

**Tinh Luyện** làm tăng Độ Tinh Khiết nhưng không mặc định làm tăng Phẩm Chất.

Gọi:

- `P₀` = Độ Tinh Khiết trước tinh luyện;
- `R` = Hiệu Suất Loại Tạp Chất của lần tinh luyện, với `0 ≤ R < 1` trong quá trình thông thường.

Độ Tinh Khiết sau tinh luyện:

```text
P₁ = P₀ + (1 - P₀) × R
```

Ví dụ với `R = 50%`:

```text
60% → 80% → 90% → 95% → 97.5% → ...
```

Do đó quá trình thông thường có thể tiến vô hạn tới `100%` nhưng không chạm `100%` bằng một giá trị `R < 1` hữu hạn.

### 8.1. Số Lượng Sau Tinh Luyện

Gọi:

- `A₀` = Số Lượng trước tinh luyện;
- `ηᵣ` = Hiệu Suất Bảo Toàn thành phần tinh thuần, `0 < ηᵣ ≤ 1`.

```text
A₁ = A₀ × (P₀ / P₁) × ηᵣ
```

Nếu `ηᵣ = 1`, công thức chỉ loại bỏ phần tạp chất cần thiết để đạt `P₁`. Nếu `ηᵣ < 1`, quá trình còn làm thất thoát một phần Năng Lượng tinh thuần.

Ví dụ:

```text
1.000 @ 60%
→ tinh luyện lên 80%, ηᵣ = 1
→ 750 @ 80%
```

## 9. Thăng Phẩm

**Thăng Phẩm** là quá trình tăng Phẩm Chất/Sắc. Nó tách biệt với Tinh Luyện.

```text
Tam Sắc 99%
```

không tự trở thành `Tứ Sắc` chỉ vì tiếp tục tinh luyện.

Nếu một mechanic Thăng Phẩm bảo toàn Hiệu Năng với hiệu suất `ηₚ`, lượng đầu ra được quy đổi:

```text
A₁ = A₀ × (Q₀ × P₀) / (Q₁ × P₁) × ηₚ
```

với:

```text
0 < ηₚ ≤ 1
```

Ví dụ không hao hụt, giữ cùng Độ Tinh Khiết:

```text
1.000 Tam Sắc 80%
Q₀ = 16
→ Tứ Sắc 80%
Q₁ = 32
→ 500 Tứ Sắc 80%
```

Các mốc Chất Biến làm lượng quy đổi giảm mạnh hơn vì `Q` nhảy `×4`.

Điều kiện để Thăng Phẩm thuộc Công Pháp/Thiên Phú/Cơ duyên/mechanic cụ thể, không có một điều kiện universal duy nhất.

## 10. Chuyển Hóa Năng Lượng

Hai loại Năng Lượng chỉ chuyển hóa khi mechanic cho phép.

Gọi:

- `Aₛ, Qₛ, Pₛ` = Số Lượng, Phẩm Chất và Độ Tinh Khiết nguồn;
- `Qₜ, Pₜ` = Phẩm Chất và Độ Tinh Khiết đích;
- `ηc` = Hiệu Suất Chuyển Hóa.

```text
Aₜ = Aₛ × (Qₛ × Pₛ) / (Qₜ × Pₜ) × ηc
```

Mặc định:

```text
0 < ηc ≤ 1
```

`Aₜ` có thể lớn hơn `Aₛ` khi Năng Lượng đích có Hiệu Năng trên mỗi đơn vị thấp hơn; điều này **không tạo thêm Hiệu Năng**.

### 10.1. Không Sinh Năng Lượng Vô Hạn

Một chu trình chuyển hóa mặc định không được tự sinh thêm Tổng Hiệu Năng.

Nếu mechanic cho phép hiệu suất tổng vượt `100%`, mechanic đó phải xác định **nguồn Hiệu Năng bổ sung** đến từ đâu.

## 11. Quan Hệ Với Kỹ Năng

Phẩm Chất/Độ Tinh Khiết cao hơn **có thể** tác động tới Kỹ Năng theo ba hướng chính:

1. **Hiệu Suất** — giảm lượng Năng Lượng cần thiết.
2. **Uy Lực / Hiệu Quả** — tăng output của Kỹ Năng.
3. **Đặc Tính** — bổ sung hoặc tăng cường hiệu ứng đặc biệt.

Không bắt buộc mọi Kỹ Năng sử dụng cả ba hướng, và không có multiplier universal áp cho mọi Kỹ Năng.

## 12. Quan Hệ Với Chỉ Số

Mỗi loại Năng Lượng có thể dùng:

```text
<Tên Năng Lượng> Tối Đa
Hồi Phục <Tên Năng Lượng>
Tỷ Lệ Hồi Phục <Tên Năng Lượng>
```

Các Chỉ Số trên có thể được tăng bởi Thuộc Tính, Công Pháp, Nghề Nghiệp, Thiên Phú, Trang Bị hoặc mechanic khác.

## 13. Trạng Thái Cạn Năng Lượng

Khi một pool Năng Lượng về `0`:

- không thể thanh toán chi phí bằng chính pool đó;
- các Kỹ Năng/Công Pháp yêu cầu pool đó không thể được khởi tạo nếu thiếu chi phí;
- pool Năng Lượng khác không tự động cạn theo;
- mechanic chuyển đổi/thay thế chi phí có thể can thiệp nếu ghi rõ.

## 14. Deferred / Ngoài Phạm Vi Freeze v1

- taxonomy đầy đủ của mọi loại Năng Lượng;
- danh sách đầy đủ Đặc Tính;
- điều kiện Thăng Phẩm cụ thể của từng Công Pháp;
- công thức từng Kỹ Năng dùng `E/Q/P` để tính tiêu hao, uy lực hoặc hiệu ứng;
- balance cụ thể của `R`, `ηᵣ`, `ηₚ`, `ηc` theo từng mechanic.
