---
type: system
status: frozen
version: 1
scope: stats
tags:
  - ideaverse/system/stat
---

# CHỈ SỐ

> [!ABSTRACT] Source of Truth
> Đây là **nguồn định nghĩa canonical** cho Hệ Thống Chỉ Số v1. Trạng thái: **FROZEN**. Bản đồ subsystem: [[HỆ THỐNG THUỘC TÍNH & CHỈ SỐ]]. Decision log: [[HỆ THỐNG CHỈ SỐ v1]].

## 1. Phạm Vi

**Chỉ Số** là các đại lượng vận hành dùng để mô tả khả năng chiến đấu, phòng thủ, hồi phục, phán định và các cơ chế chuyên biệt của một cá thể.

Hệ thống phân biệt ba lớp:

- **Thuộc Tính:** nền tảng chuẩn hóa của cá thể, xem [[THUỘC TÍNH]].
- **Chỉ Số:** đại lượng được dùng trực tiếp trong công thức/phán định hoặc được Trang Bị, Kỹ Năng, hiệu ứng và cơ chế khác sửa đổi.
- **Tài Nguyên:** trạng thái dạng `hiện tại / tối đa`; source of truth: [[TÀI NGUYÊN]].

Ví dụ:

```text
Chân Nguyên Tối Đa: 10.000      ← Chỉ Số
Chân Nguyên: 7.500 / 10.000     ← Tài Nguyên
```

`Định Tính Tối Đa`, `Hồi Phục Định Tính` và `Tỷ Lệ Hồi Phục Định Tính` là Chỉ Số; `Định Tính hiện tại / tối đa` thuộc Hệ Thống Tài Nguyên.

## 2. Phân Cấp

Chỉ Số được chia thành ba cấp. Phân cấp phản ánh **vai trò cơ chế, độ hiếm và mức độ can thiệp vào hệ thống**, không có nghĩa mọi Chỉ Số Thượng Cấp luôn mạnh hơn mọi Chỉ Số Trung Cấp.

- [[CHỈ SỐ CƠ SỞ]] — các đại lượng nền tảng. `Cơ Sở` không đồng nghĩa với dễ tăng.
- [[CHỈ SỐ TRUNG CẤP]] — các đại lượng chuyên biệt như Chính Xác/Né Tránh, Chí Mạng, Nhược Điểm, Xuyên, Kháng Tính, modifier sát thương và Hút Máu.
- [[CHỈ SỐ THƯỢNG CẤP]] — các đại lượng hiếm hoặc can thiệp vào layer sâu như Phụ Tố, Định Tính, Sát Thương Chuẩn, tầm hiệu lực, phòng ngự cuối và đa kênh Thi Triển.

## 3. Ký Hiệu & Quy Ước Toán Học

### 3.1. Đơn Vị

- `Điểm` — giá trị phẳng.
- `%` — giá trị phần trăm hoặc Giá Trị Kháng tùy Chỉ Số.
- `×` — hệ số nhân, ví dụ `Sát Thương Chí Mạng ×1.8`.
- `đòn/s`, `m/s`, `giây` — đơn vị vật lý/thời gian.
- `số nguyên` — cơ chế rời rạc như `Số Kênh Thi Triển`.

Không gộp `Điểm/%` vào cùng một Chỉ Số. Flat và tỷ lệ là các giá trị/cơ chế khác nhau.

### 3.2. Modifier Phần Trăm Thông Thường

Các modifier `%` độc lập được **nhân**, không cộng trực tiếp, trừ khi một cơ chế ghi rõ ngoại lệ.

Với modifier `B_i` viết dưới dạng số thập phân (`+50% = 0.5`, `-30% = -0.3`):

```text
M_i = max(0, 1 + B_i)
M_tổng = Π M_i
Giá trị sau modifier = Giá trị trước modifier × M_tổng
```

Ví dụ:

```text
+50% Sát Thương Vật Lý
+40% Sát Thương Cận Chiến
+30% Sát Thương Nhục Thể

→ ×1.5 ×1.4 ×1.3
→ ×2.73
```

Modifier âm được phép nếu cơ chế cho phép; multiplier không được âm.

### 3.3. Mô Hình Kháng Tiệm Cận

Ngoại trừ `Kháng Chí Mạng`, mọi Chỉ Số `% Kháng` thuộc mô hình này đều **không thể đạt 100% hiệu lực bằng một giá trị hữu hạn**. `100% miễn nhiễm` phải đến từ mechanic **Miễn Nhiễm**, không phải stacking Kháng thông thường.

Với một nguồn Giá Trị Kháng `R`:

```text
R >= 0:
Hệ Số Còn Lại K(R) = 100 / (100 + R)

R < 0 (chỉ với loại Kháng cho phép âm):
K(R) = 1 + |R| / 100
```

Nhiều nguồn Kháng độc lập được nhân:

```text
K_tổng = Π K(R_i)
Kháng Hiệu Lực = 1 - K_tổng
Giá trị sau Kháng = Giá trị trước Kháng × K_tổng
```

Ví dụ hai nguồn `Kháng = 100`:

```text
K = 0.5 × 0.5 = 0.25
→ còn 25%
→ Kháng Hiệu Lực = 75%
```

Giá Trị Kháng càng lớn thì hiệu lực càng tiến gần `100%` nhưng không bằng `100%` với giá trị hữu hạn.

Các nhóm dùng mô hình này gồm:

- `Vật Lý Kháng Tính`, `Pháp Thuật Kháng Tính`, `Toàn Nguyên Tố Kháng Tính`, `<Nguyên Tố> Kháng Tính`.
- `Kháng Sát Thương Cận Chiến`, `Kháng Sát Thương Viễn Trình`.
- `Kháng Sát Thương Nhục Thể`, `Kháng Sát Thương Linh Hồn`.
- `Kháng Sát Thương Chí Mạng`, `Kháng Sát Thương Nhược Điểm`.
- `Kháng Sức Phá Định Tính`.
- `Kháng Thời Gian Khống Chế/Debuff`, `Kháng Cường Độ Khống Chế/Debuff`.
- `Phòng Ngự Tuyệt Đối`.

`Kháng Chí Mạng` là **ngoại lệ**: nó giảm trực tiếp tỷ lệ Chí Mạng theo điểm phần trăm.

### 3.4. Snapshot

Nếu một giá trị được phán định tại thời điểm hiệu ứng được áp dụng, kết quả đã phán định được **snapshot**. Thay đổi Chỉ Số sau đó không tự động tính lại hiệu ứng đang tồn tại, trừ khi mechanic ghi rõ.

Quy tắc này đặc biệt áp dụng cho Thời Gian/Cường Độ của Phụ Tố.

## 4. Pattern Chỉ Số Liên Quan Tài Nguyên

Không hard-code mọi loại Tài Nguyên vào schema. Mỗi Tài Nguyên có thể sinh các Chỉ Số:

```text
<Tài Nguyên> Tối Đa
Hồi Phục <Tài Nguyên>
Tỷ Lệ Hồi Phục <Tài Nguyên>
```

Ví dụ: `Sinh Mệnh Lực`, `Thể Lực`, `Tinh Lực` và từng loại [[NĂNG LƯỢNG]] như `Pháp Lực`, `Đấu Khí`, `Linh Lực`, `Chân Nguyên`...

`Sinh Mệnh Lực` và `Định Tính` dùng cùng tư tưởng nhưng là cơ chế nền được ghi rõ trong [[CHỈ SỐ CƠ SỞ]].

## 5. Mô Hình Sát Thương

Một damage instance có thể mang nhiều tag độc lập.

### 5.1. Loại Sát Thương

- **Vật Lý**
- **Pháp Thuật**
- **Chuẩn**

`Nguyên Tố` không phải một Loại Sát Thương cạnh tranh với ba loại trên.

### 5.2. Nguyên Tố

Ví dụ: `Không Nguyên Tố`, `Hỏa`, `Thủy`, `Băng`, `Lôi`, `Phong`, `Thổ`, `Quang`, `Ám`...

```text
Hỏa Cầu   → Pháp Thuật + Hỏa
Hỏa Quyền → Vật Lý + Hỏa
```

### 5.3. Đối Tượng Tác Động

- **Nhục Thể**
- **Linh Hồn**

### 5.4. Khoảng Cách

Chỉ áp dụng cho sát thương **Nhục Thể**:

- **Cận Chiến**
- **Viễn Trình**

Phân loại dựa trên **tag**, không dựa trên khoảng cách thực tế lúc trúng.

## 6. Offensive Modifier

Mọi modifier tăng/giảm sát thương hợp lệ được resolve theo quy tắc multiplicative ở §3.2.

Ví dụ một instance `Vật Lý + Nhục Thể + Cận Chiến` có thể đồng thời nhận:

```text
Tăng Sát Thương Vật Lý
Tăng Sát Thương Nhục Thể
Tăng Sát Thương Cận Chiến
```

Nếu là Sát Thương Chuẩn thì dùng `Tăng Sát Thương Chuẩn` thay cho modifier theo Loại Vật Lý/Pháp Thuật.

## 7. Chính Xác, Né Tránh & Đón Đỡ

### 7.1. Chính Xác ↔ Né Tránh

Với `A = Chính Xác`, `E = Né Tránh`:

```text
E = 0                         → Tỷ Lệ Đánh Trúng = 100%
A = 0 và E > 0               → Tỷ Lệ Đánh Trúng = 0%
A > 0 và E > 0               → P(hit) = A / (A + E)
```

Hai bên bằng nhau → `50%` đánh trúng. Kỹ Năng/cơ chế `Tất Trúng`, `Không Thể Né`... có thể bypass công thức nếu ghi rõ.

### 7.2. Đón Đỡ

Nếu phán định Đón Đỡ thành công:

```text
D_sau_đón_đỡ = max(0, D × (1 - Hiệu Quả Đón Đỡ))
```

`Tỷ Lệ Đón Đỡ` quyết định xác suất; `Hiệu Quả Đón Đỡ` quyết định lượng sát thương giảm. Đón Đỡ được resolve **trước** Giáp/Kháng Phép.

## 8. Chí Mạng & Nhược Điểm

### 8.1. Tỷ Lệ Chí Mạng

```text
Tỷ Lệ Chí Mạng Hiệu Lực
= clamp(Tỷ Lệ Chí Mạng - Kháng Chí Mạng, 0%, 100%)
```

`Kháng Chí Mạng` có thể overcap trên `100%`; xác suất cuối vẫn floor `0%`. Đây là Chỉ Số giảm xác suất, **không dùng mô hình Kháng tiệm cận**.

### 8.2. Sát Thương Chí Mạng

Nếu `M_crit` là multiplier Chí Mạng cơ sở và `K_crit` là tích các hệ số còn lại từ `Kháng Sát Thương Chí Mạng`:

```text
Bonus Crit = max(0, M_crit - 1)
M_crit_hiệu_lực = 1 + Bonus Crit × K_crit
```

Kháng chỉ giảm **bonus Crit**, không làm multiplier xuống dưới `×1`.

### 8.3. Nhược Điểm

Nhược Điểm là phán định điều kiện/vị trí, không phải RNG thứ hai.

`Dung Sai Nhược Điểm` mở rộng **vùng phán định**, không thay đổi kích thước vật lý thật. Với kích thước tuyến tính cơ sở `L`:

```text
L_hiệu_lực = L × Π max(0, 1 + B_i)
```

Nếu `M_weak` là multiplier Nhược Điểm cơ sở và `K_weak` là tích hệ số từ `Kháng Sát Thương Nhược Điểm`:

```text
Bonus Weak = max(0, M_weak - 1)
M_weak_hiệu_lực = 1 + Bonus Weak × K_weak
```

### 8.4. Crit × Weak Point

Nếu cả hai cùng xảy ra, chúng **nhân**:

```text
D' = D × M_crit_hiệu_lực × M_weak_hiệu_lực
```

## 9. Giáp, Kháng Phép, Cố Giáp/Cố Kháng Phép & Xuyên

### 9.1. Giáp/Kháng Phép Không Âm

`Giáp` và `Kháng Phép` hiệu lực floor tại `0`. Weakness được biểu diễn qua Kháng Tính âm, không qua Giáp/Kháng Phép âm.

### 9.2. Stacking Cố Giáp/Cố Kháng Phép

Nhiều nguồn `Cố Giáp` hoặc `Cố Kháng Phép` độc lập dùng coverage multiplicative:

```text
C_hiệu_lực = 1 - Π(1 - C_i)
```

với `C_i` là tỷ lệ trong `[0, 1]` của từng nguồn thông thường.

### 9.3. Stacking Tỷ Lệ Xuyên

Nhiều nguồn `Tỷ Lệ Xuyên` độc lập:

```text
P_hiệu_lực = 1 - Π(1 - P_i)
```

`P_hiệu_lực` nằm trong `[0, 1]`. Các nguồn Xuyên `Điểm` cộng thành `P_flat`.

### 9.4. Thứ Tự Xuyên

Với `Def` là Giáp hoặc Kháng Phép đã hoàn tất modifier, `C` là Cố Giáp/Cố Kháng Phép hiệu lực:

```text
Def_cố = Def × C
Def_có_thể_xuyên = Def - Def_cố

Def_sau_xuyên_% = Def_có_thể_xuyên × (1 - P_hiệu_lực)
Def_sau_xuyên_điểm = max(0, Def_sau_xuyên_% - P_flat)

Def_hiệu_lực = Def_cố + Def_sau_xuyên_điểm
```

Thứ tự canonical:

```text
Defense hoàn chỉnh
→ tách phần Cố
→ Xuyên % trên phần có thể xuyên
→ Xuyên Điểm
→ cộng lại phần Cố
```

### 9.5. Công Thức Giáp/Kháng Phép

Với `D > 0` là sát thương đi vào layer và `Def_hiệu_lực >= 0`:

```text
Def_hiệu_lực = 0 → D_sau = D
Def_hiệu_lực > 0 → D_sau = D² / (D + Def_hiệu_lực)
```

Tương đương:

```text
D_sau = D × D / (D + Def_hiệu_lực)
```

Tính chất:

- `D = Def` → còn `50%`.
- Tỷ lệ `Damage : Defense` tương đương cho kết quả tương đương ở mọi power scale.
- Defense mạnh hơn trước nhiều hit nhỏ so với một hit lớn có cùng tổng damage; đây là **chủ ý thiết kế**.

Sát Thương Vật Lý dùng `Giáp`; Sát Thương Pháp Thuật dùng `Kháng Phép`; Sát Thương Chuẩn bỏ qua cả hai.

## 10. Kháng Tính & Kháng Sát Thương Theo Tag

Mỗi nguồn Kháng dùng mô hình §3.3 và các layer **nhân** phần sát thương còn lại.

### 10.1. Vật Lý / Pháp Thuật

- Sát Thương Vật Lý chịu `Vật Lý Kháng Tính`.
- Sát Thương Pháp Thuật chịu `Pháp Thuật Kháng Tính`.

Hai Kháng Tính này có thể âm.

### 10.2. Nguyên Tố

Nếu instance mang tag nguyên tố, nó chịu đồng thời:

```text
Toàn Nguyên Tố Kháng Tính
<Nguyên Tố> Kháng Tính tương ứng
```

Các layer nhân nhau. Ví dụ `Hỏa` chịu cả `Toàn Nguyên Tố` và `Hỏa Kháng Tính`.

### 10.3. Cận Chiến / Viễn Trình

Chỉ áp dụng cho instance **Nhục Thể** mang tag tương ứng. Các nguồn Kháng Cận/Viễn dùng mô hình tiệm cận.

### 10.4. Nhục Thể / Linh Hồn

Mọi instance hợp lệ chịu `Kháng Sát Thương Nhục Thể` hoặc `Kháng Sát Thương Linh Hồn` theo đối tượng tác động.

## 11. Pipeline Sát Thương Vật Lý / Pháp Thuật

Pipeline canonical:

```text
Sát Thương Cơ Sở
→ Offensive Modifier hợp lệ (multiplicative)
→ phán định Chí Mạng
→ phán định Nhược Điểm
→ nhân Crit / Weak Point nếu có
→ phán định Đón Đỡ; áp Hiệu Quả Đón Đỡ nếu thành công
→ Giáp hoặc Kháng Phép (sau Cố + Xuyên)
→ Kháng Sát Thương Cận/Viễn nếu hợp lệ
→ Vật Lý/Pháp Thuật Kháng Tính
→ Toàn Nguyên Tố Kháng Tính nếu có tag Nguyên Tố
→ <Nguyên Tố> Kháng Tính tương ứng
→ Kháng Sát Thương Nhục Thể/Linh Hồn
→ Phòng Ngự Tuyệt Đối
→ Giảm Sát Thương Cuối Cùng
→ floor 0
→ Sát Thương Thực Nhận
```

Do nhiều layer là phép nhân, một số bước có thể giao hoán về mặt số học; pipeline trên vẫn là **thứ tự canonical để debug, mô tả và triển khai calculator**.

## 12. Sát Thương Chuẩn

Sát Thương Chuẩn bypass các defense thông thường. Sau Offensive Modifier, Chí Mạng/Nhược Điểm và các phán định liên quan, pipeline phòng thủ của Sát Thương Chuẩn chỉ còn:

```text
Kháng Sát Thương Nhục Thể hoặc Linh Hồn
→ Phòng Ngự Tuyệt Đối
→ Giảm Sát Thương Cuối Cùng
→ floor 0
```

Sát Thương Chuẩn bỏ qua:

- Giáp, Kháng Phép.
- Cố Giáp, Cố Kháng Phép và toàn bộ Xuyên tương ứng.
- Kháng Sát Thương Cận Chiến/Viễn Trình.
- Vật Lý/Pháp Thuật Kháng Tính.
- Toàn Nguyên Tố và Kháng Tính nguyên tố riêng.
- `Kháng Sát Thương Chí Mạng` và `Kháng Sát Thương Nhược Điểm` đối với bonus damage của instance Chuẩn.

`Kháng Chí Mạng` vẫn có thể làm giảm **xác suất** Chí Mạng vì đây là phán định xác suất, không phải layer giảm Sát Thương Chuẩn.

## 13. Phòng Ngự Tuyệt Đối & Giảm Sát Thương Cuối Cùng

### 13.1. Phòng Ngự Tuyệt Đối

`Phòng Ngự Tuyệt Đối` dùng mô hình Kháng tiệm cận §3.3:

```text
D' = D × Π K(Phòng Ngự Tuyệt Đối_i)
```

Không thể đạt `100%` hiệu lực bằng giá trị hữu hạn; miễn nhiễm hoàn toàn phải đến từ mechanic riêng.

### 13.2. Giảm Sát Thương Cuối Cùng

Áp sau Phòng Ngự Tuyệt Đối trên **từng damage instance**:

```text
D_final = max(0, D' - Giảm Sát Thương Cuối Cùng)
```

Do là flat per-instance, Chỉ Số này mạnh trước multi-hit/chip damage hơn một hit cực lớn.

## 14. Hút Máu

Hút Máu mặc định tính từ **Sát Thương Thực Nhận hợp lệ thực tế đã gây ra** sau pipeline phòng thủ.

- `Hút Máu Đòn Đánh` — Đòn Đánh hợp lệ.
- `Hút Máu Kỹ Năng` — Kỹ Năng hợp lệ.
- `Hút Máu Toàn Phần` — cả hai nhóm trên.

Mặc định không áp dụng cho DoT/Phụ Tố, phản sát thương, môi trường hoặc damage của summon/thực thể khác trừ khi nguồn ghi ngoại lệ.

## 15. Phụ Tố & Định Tính

### 15.1. Phụ Tố

**Phụ Tố** là tên chung cho **Khống Chế** và **Debuff**.

Mỗi Phụ Tố có thể định nghĩa:

- Thời Gian Cơ Sở.
- Cường Độ Nội Bộ Cơ Sở.
- Cấp hiển thị `I–X`.
- Sức Phá Định Tính Cơ Sở.
- `Thời Gian Cộng Dồn Tối Đa Có Hiệu Lực`.
- các giới hạn/mechanic riêng khác.

Không có công thức bắt buộc biến Thời Gian/Cường Độ thành Sức Phá Định Tính. Mỗi Phụ Tố/Kỹ Năng định nghĩa Sức Phá cơ sở và quan hệ riêng nếu cần.

### 15.2. Cấp Phụ Tố

| Cường Độ Nội Bộ | Cấp Hiển Thị |
|---:|:---:|
| `1–100` | I |
| `101–200` | II |
| `201–300` | III |
| `301–400` | IV |
| `401–500` | V |
| `501–600` | VI |
| `601–700` | VII |
| `701–800` | VIII |
| `801–900` | IX |
| `901+` | X |

Giá trị nội bộ không hard cap. Overcap vẫn có ý nghĩa khi gặp Kháng/Giảm Cường Độ.

### 15.3. Sức Phá Định Tính

Với `Break_base` và các modifier Tăng Sức Phá độc lập `B_i`:

```text
Break_tăng = Break_base × Π max(0, 1 + B_i)
Break_final = Break_tăng × Π K(Kháng Sức Phá Định Tính_i)
```

Sau đó:

```text
Định Tính mới = max(0, Định Tính hiện tại - Break_final)
```

Sức Phá dư bị mất; Định Tính không âm và không carry overflow.

### 15.4. Thiết Lập Phụ Tố

```text
Định Tính > 0 sau Sức Phá
→ Phụ Tố chưa được thiết lập

Định Tính = 0
→ Phụ Tố làm Định Tính về 0 được thiết lập
→ khi vẫn ở 0, mọi Phụ Tố hợp lệ tiếp theo có thể được thiết lập trực tiếp
```

### 15.5. Hồi Phục Định Tính

Sau **lần cuối nhận Sức Phá Định Tính**, phải hết `Trì Hoãn Hồi Phục Định Tính` mới bắt đầu hồi.

Mỗi giây:

```text
Hồi Phục Định Tính mỗi giây
= Hồi Phục Định Tính
+ Định Tính Tối Đa × Tỷ Lệ Hồi Phục Định Tính / 100
```

Nhận Sức Phá mới làm mới thời điểm bắt đầu trì hoãn, kể cả khi Định Tính đang ở `0`.

Reset toàn bộ/một phần Định Tính là mechanic đặc biệt, không phải hành vi mặc định.

### 15.6. Thời Gian Phụ Tố

Với `T_base`, các nguồn Tăng Thời Gian `B_i`, hệ số Kháng `K_time` và tổng `Giảm Thời Gian` flat:

```text
T_applied
= max(0,
    T_base
    × Π max(0, 1 + B_i)
    × K_time
    - Giảm Thời Gian
  )
```

`K_time` là tích các `K(R_i)` từ Kháng Thời Gian tương ứng.

Nếu cùng Phụ Tố đang tồn tại:

```text
T_mới = min(
  T_hiện_tại + T_applied,
  Thời Gian Cộng Dồn Tối Đa Có Hiệu Lực hiện tại
)
```

Phần vượt cap mất hẳn. Cap có thể được tăng/giảm bởi Thiên Phú, Kỹ Năng, Trang Bị hoặc mechanic khác. Mặc định cap được đọc tại thời điểm cộng dồn mới; thay đổi sau đó không tự viết lại duration đã snapshot nếu mechanic không ghi rõ.

### 15.7. Cường Độ Phụ Tố

Với `I_base`, các nguồn Tăng Cường Độ `B_i`, hệ số Kháng `K_intensity` và tổng `Giảm Cường Độ` flat:

```text
I_applied
= max(0,
    I_base
    × Π max(0, 1 + B_i)
    × K_intensity
    - Giảm Cường Độ
  )
```

Giá trị sau phán định được snapshot rồi cộng vào Cường Độ Nội Bộ đang tồn tại theo rule của Phụ Tố. Internal Value có thể overcap vô hạn; display tối đa X.

Nếu mục tiêu tăng Kháng sau khi Phụ Tố đã được áp dụng, Phụ Tố hiện hữu **không tự yếu đi**; lần áp dụng sau mới dùng giá trị Kháng mới.

## 16. Thi Triển Kỹ Năng, Hồi Chiêu & Kênh Thi Triển

Không tồn tại Chỉ Số toàn nhân vật `Tốc Độ Thi Pháp`, `Tốc Độ Thi Triển` hoặc `Tốc Độ Hồi Chiêu`.

Mỗi Kỹ Năng có:

- Độ Thuần Thục.
- Cấp Kỹ Năng.
- Thời Gian Thi Triển.
- Thời Gian Hồi Chiêu.

```text
Sử dụng Kỹ Năng
→ tăng Độ Thuần Thục
→ đủ điều kiện
→ Kỹ Năng tăng Cấp
→ Cấp cao hơn có thể giảm Thời Gian Thi Triển/Hồi Chiêu và cải thiện thông số khác theo thiết kế Kỹ Năng
```

Hồi chiêu bắt đầu **sau khi Thi Triển hoàn tất**. Với Kỹ Năng Duy Trì, hồi chiêu bắt đầu sau khi Duy Trì kết thúc.

`Số Kênh Thi Triển` không có hard cap toàn hệ thống.

Mỗi kênh:

1. Hoạt động đồng thời với các kênh khác.
2. Bị chiếm trong toàn bộ Thời Gian Thi Triển/Duy Trì.
3. Có bảng Hồi Chiêu riêng cho từng Kỹ Năng.
4. Kỹ Năng A đang hồi trên Kênh I không khóa Kỹ Năng B khi kênh đã rảnh.
5. Cùng Kỹ Năng có thể được dùng trên nhiều kênh nếu từng cooldown tương ứng sẵn sàng.
6. Mỗi instance trả Tài Nguyên riêng và phán định Chí Mạng, Nhược Điểm, Phụ Tố, Hút Máu, damage và proc độc lập.

Tên hiển thị có thể dùng `Song/Tam/Tứ/... Trọng Thi Triển` từ 2 kênh trở lên.

## 17. Tầm Hiệu Lực

Base range thuộc Vũ Khí/Kỹ Năng, không phải Chỉ Số range cố định của nhân vật.

```text
Tầm Hiệu Lực = Tầm Cơ Sở × Π max(0, 1 + Bonus_i)
```

Áp dụng tương ứng cho:

- `Tăng Tầm Đánh`.
- `Tăng Tầm Kỹ Năng`.
- `Tăng Phạm Vi Ảnh Hưởng`.

Với AoE, `% Phạm Vi` tác động lên kích thước tuyến tính được Kỹ Năng định nghĩa (ví dụ bán kính), vì vậy diện tích/thể tích có thể tăng nhanh hơn tỷ lệ phần trăm tuyến tính.

## 18. Trang Bị

Các Chỉ Số có thể xuất hiện trên Trang Bị nếu loại Trang Bị/cơ chế cho phép. Cấp Cơ Sở–Trung Cấp–Thượng Cấp định hướng độ hiếm/quyền năng, không ép mọi Trang Bị vào bảng rarity cứng.

Modifier phải ghi rõ loại:

```text
+500 Giáp
+20% Giáp
+100 Xuyên Giáp
+15% Tỷ Lệ Xuyên Giáp
```

Không dùng `Điểm/%` mơ hồ trên cùng một Chỉ Số.

## 19. Ngoài Phạm Vi v1 / Thiết Kế Tiếp Theo

Các mục sau **không phải lỗ hổng của Hệ Thống Chỉ Số v1**, mà thuộc subsystem hoặc integration khác và sẽ thiết kế sau:

- Công thức chuyển [[THUỘC TÍNH]] thành Chỉ Số cụ thể.
- Chi tiết trạng thái `hiện tại / tối đa`, Phẩm Chất/Độ Tinh Khiết và ngưỡng suy giảm thuộc [[TÀI NGUYÊN]].
- Progression chi tiết của Độ Thuần Thục/Cấp Kỹ Năng.
- Danh sách đầy đủ Phụ Tố và Sức Phá Định Tính cơ sở của từng Phụ Tố.
- Giá trị cân bằng thực tế cho Trang Bị, Kỹ Năng, Nghề Nghiệp, Cảnh Giới...
- Calculator/web hỗ trợ tính pipeline số lớn.
