---
type: system
status: frozen
version: 2
scope: attributes
tags:
  - ideaverse/system/attribute
---

# THUỘC TÍNH

> [!ABSTRACT] Source of Truth
> Đây là nguồn định nghĩa chính thức cho **Hệ Thống Thuộc Tính v2** của Ideaverse. Bản đồ subsystem: [[HỆ THỐNG THUỘC TÍNH & CHỈ SỐ]]. Decision log: [[HỆ THỐNG THUỘC TÍNH v2]].

## 1. Phân Loại

### 1.1. Thuộc Tính Cơ Bản

- [[Sức Mạnh]]
- [[Thể Chất]]
- [[Nhanh Nhẹn]]
- [[Tinh Thần]]

Thuộc Tính Cơ Bản có thể tăng bằng các phương thức tăng trưởng thông thường được hệ thống cho phép, gồm level, Điểm Thuộc Tính Tự Do, rèn luyện, Công Pháp, Nghề Nghiệp, Thiên Phú, vật phẩm hoặc cơ chế tương đương.

Bốn Thuộc Tính Cơ Bản có thể nhận Hồi Báo Thí Luyện khi [[HỆ THỐNG NGHỀ NGHIỆP|Nghề Nghiệp]] Chuyển. **Không** đổi đơn vị hoặc thêm hậu tố bậc Chuyển vào tên Thuộc Tính.

### 1.2. Thuộc Tính Đặc Biệt

- [[Ngộ Tính]]
- [[Mị Lực]]
- [[Vận Khí]]

Thuộc Tính Đặc Biệt không tăng bằng Điểm Thuộc Tính Tự Do hoặc tăng trưởng level thông thường. Chúng chỉ thay đổi bởi phương thức đặc biệt/hiếm hoặc một mechanic ghi rõ ngoại lệ.

Thuộc Tính Đặc Biệt không nhận Hồi Báo Thí Luyện theo mặc định; chỉ tăng bằng mechanic đặc biệt được phép.

---

## 2. Quy Chuẩn Giá Trị

### 2.1. Thang Tuyến Tính

Thuộc Tính sử dụng **thang tuyến tính** trong cùng một bậc biểu diễn.

- `0`: hoàn toàn không có khả năng tương ứng ở lớp đo đó.
- `0 < x < 1`: phạm vi dưới cực hạn tự nhiên của người thường.
- `1`: **cực hạn tự nhiên của người thường** đối với Thuộc Tính tương ứng.
- `> 1`: vượt cực hạn người thường.
- **Không có hard cap** cho Thuộc Tính.
- Giá trị rất lớn có thể viết bằng scientific notation, ví dụ `1e10`, `3e50`, `1e100`.

Đối với bốn Thuộc Tính Cơ Bản, `~0.5` là mốc tham chiếu gần đúng cho một người trưởng thành khỏe mạnh bình thường. Đây là mốc tham chiếu, không phải giá trị bắt buộc cho mọi cá thể.

`1` là chuẩn tham chiếu của **người thường**, không phải universal cap. Chủng tộc hoặc sinh vật khác có thể sinh ra với Base `> 1`.

> [!IMPORTANT]
> Tuyến tính của Thuộc Tính không bắt buộc Chỉ Số dẫn xuất, xác suất hoặc subsystem sử dụng nó phải tuyến tính.

### 2.2. Base và Effective

- **Base:** giá trị nội tại sau mọi tăng trưởng **vĩnh viễn**.
- **Effective:** giá trị thực tế được sử dụng sau modifier tạm thời, trang bị, buff, debuff, trạng thái và mechanic hợp lệ khác.

Thứ tự chuẩn:

```text
Base
→ cộng/trừ Flat Effective
→ nhân các Percentage Modifier độc lập
→ áp quy tắc sàn/dấu của Thuộc Tính
→ Effective
```

Công thức tổng quát:

$$
E_{raw}=(B+\sum F_i)\times\prod_j(1+M_j)
$$

Trong đó:

- `B`: Base hiện tại;
- `Fᵢ`: modifier flat chỉ tác động Effective;
- `Mⱼ`: modifier tỷ lệ viết dưới dạng số thập phân, ví dụ `+20% = 0.2`, `-30% = -0.3`.

Các nguồn `%` **multiplicative**, không cộng gộp thành một `%` duy nhất.

Ví dụ:

```text
Base Sức Mạnh = 10
+2 Sức Mạnh Effective
+20% Sức Mạnh
+50% Sức Mạnh

Effective = (10 + 2) × 1.2 × 1.5 = 21.6
```

Tăng trưởng vĩnh viễn như Điểm Thuộc Tính Tự Do, rèn luyện, đột phá hoặc vật phẩm thực sự cải tạo bản thể phải sửa **Base**, không được lưu như modifier Effective.

### 2.3. Quy Tắc Giá Trị Âm

| Thuộc tính | Base âm | Effective âm | Quy tắc |
|---|:---:|:---:|---|
| Sức Mạnh | Không | Không | Effective cuối cùng sàn tại `0`. |
| Thể Chất | Không | Không | Effective cuối cùng sàn tại `0`. |
| Nhanh Nhẹn | Không | Không | Effective cuối cùng sàn tại `0`. |
| Tinh Thần | Không | Không | Effective cuối cùng sàn tại `0`. |
| Ngộ Tính | Không | Có | Base `>= 0`; modifier có thể làm Effective `< 0`. |
| Mị Lực | Có | Có | Giá trị âm biểu thị xu hướng gây bài xích/xa lánh thay vì hấp dẫn. |
| Vận Khí | Có | Có | Giá trị âm biểu thị thiên hướng bất lợi trong sự kiện vốn có xác suất. |

---

## 3. Điểm Thuộc Tính Tự Do

### 3.1. Phạm Vi & Quy Đổi

- Chỉ cộng trực tiếp vào bốn Thuộc Tính Cơ Bản.
- **1 Điểm Thuộc Tính Tự Do = +1 Base** bất kể đã Chuyển bao nhiêu lần.
- Tên Thuộc Tính luôn là `Sức Mạnh`, `Thể Chất`, `Nhanh Nhẹn`, `Tinh Thần`, không thêm `I–X`.
- Điểm đã phân bổ trước một lần Chuyển nằm trong Base và nhận Hồi Báo Thí Luyện cùng Base đó. Điểm phân bổ sau lần Chuyển không được hồi tố nhân thưởng của lần Chuyển đã hoàn tất.

Ví dụ:

```text
Sức Mạnh Base = 10
+1 Điểm Thuộc Tính Tự Do trước Chuyển → Base = 11
Thí Luyện IV (×100)                 → Base = 1100

Nếu giữ điểm lại và cộng sau Chuyển:
Base = 10 × 100 + 1 = 1001
```

### 3.2. Nguồn Nhận

- Nghề Nghiệp phẩm chất cao nhất độc hữu Nhân Vật Chính: `+10` Điểm Thuộc Tính Tự Do/level.
- Nghề Nghiệp của nhân vật khác: tối đa `+5` điểm/level.
- Vật phẩm cho Điểm Thuộc Tính Tự Do tồn tại nhưng **cực kỳ hiếm**.
- Lộ trình nhận điểm cụ thể theo Nghề Nghiệp vẫn **IN DESIGN**; không tự động suy ra từ bản quy tắc Thuộc Tính này.

---

## 4. Chuyển và Hồi Báo Thí Luyện

- Nghề Nghiệp có **10 lần Chuyển** (`I–X`), nhưng đó là **bậc Nghề Nghiệp**, không phải bậc/đơn vị của Thuộc Tính.
- Mỗi lần Chuyển chọn một trong bốn cấp Thí Luyện. Hồi Báo áp dụng đồng thời lên Base của bốn Thuộc Tính Cơ Bản.
- Không có **Chiết Xuất**, `K`, Hệ Số Chiết Xuất Tích Lũy, giá trị Equivalent, hay biểu diễn `Sức Mạnh I`, `Sức Mạnh II`.

| Cấp Thí Luyện | Hồi Báo `R` |
|---|---:|
| I | `×2` |
| II | `×5` |
| III | `×10` |
| IV | `×100` |

$$
B_{\mathrm{sau}}=B_{\mathrm{truoc}}\times R
$$

Hồi Báo làm tăng **Base thật**, không chỉ thay đổi đơn vị hiển thị. Nếu có nhiều lần Chuyển, dùng chính Base sau mỗi lần Chuyển làm đầu vào cho lần kế tiếp, cộng mọi tăng trưởng hợp lệ xảy ra giữa các lần. Ví dụ Base `10` qua hai Thí Luyện `×5` và `×10`, không có thay đổi khác, sẽ thành `500`.

Thí Luyện không tự nhân Thuộc Tính Đặc Biệt, không tự nhân Chỉ Số hoặc Tài Nguyên đã tồn tại. Chỉ Số được **tính lại từ Thuộc Tính Effective mới** theo bảng chuyển đổi của mục 5, rồi cộng các nguồn độc lập và áp modifier Chỉ Số tương ứng.

> [!CAUTION] Cân bằng
> Nếu đạt Thí Luyện IV cả 10 lần, chỉ riêng phần thưởng có thể nhân Base ban đầu lên `100^10 = 1e20`. Đây là hệ quả chủ ý của lựa chọn không Chiết Xuất, không phải một giá trị đã được kiểm chứng cân bằng.

---

## 5. Chuyển Đổi Thuộc Tính → Chỉ Số/Tài Nguyên

### 5.1. Nguyên Tắc

- Chỉ bốn **Thuộc Tính Cơ Bản Effective** tham gia chuyển đổi mặc định; ba Thuộc Tính Đặc Biệt không tham gia.
- **Chỉ Số Cơ Sở** có thể chuyển đổi theo tỷ lệ `1 Thuộc Tính → y Chỉ Số` tùy đơn vị đích.
- **Chỉ Số Trung Cấp** được chọn lọc có tỷ lệ `10 Thuộc Tính → 1 đơn vị Chỉ Số` (`z=10`, `k=1`); giữ giá trị thập phân, **không** lấy `floor` theo từng mốc.
- **Chỉ Số Thượng Cấp không có chuyển đổi mặc định hoặc trực tiếp từ Thuộc Tính.** Chúng chỉ đến từ Nghề Nghiệp, Thiên Phú, Kỹ Năng, Công Pháp, Trang Bị, Huyết Mạch hay nguồn khác ghi rõ.
- Không chuyển đổi Thuộc Tính trực tiếp thành **Chỉ Số xác suất** (Tỷ Lệ Chí Mạng, Tỷ Lệ Đón Đỡ...), Hút Máu, `% Tăng Sát Thương` theo Loại/tag, hay **Tỷ Lệ Hồi Phục `% Tối Đa/s`**.
- Công thức này xác định *đóng góp mặc định* của Thuộc Tính. Các nguồn độc lập và mechanic tăng hệ số chuyển đổi vẫn có thể tác động, nhưng phải ghi rõ mục tiêu và thứ tự xử lý; không được áp cùng một đóng góp hai lần.

Với `A_i` là **Effective** của Thuộc Tính tương ứng và `c_{i,s}` là hệ số tại bảng:

$$
\mathrm{Contribution}_{s}=\sum_i A_i\,c_{i,s}
$$

$$
S_{\mathrm{pre},s}=\mathrm{Contribution}_{s}+\mathrm{Other}_{s}
$$

Sau đó mới áp modifier theo [[CHỈ SỐ]]; **không nhân lặp** một buff Thuộc Tính vào Chỉ Số lần nữa. Khi Effective thay đổi, phần dẫn xuất được tính lại theo giá trị mới, không mặc định sửa Base vĩnh viễn.

### 5.2. Bảng Chỉ Số Cơ Sở — Mặc Định v2

| Thuộc Tính | Cứ +1 Effective tạo ra | Đơn vị |
|---|---|---|
| **Sức Mạnh** | `+10 Công Vật Lý` | Điểm |
| **Thể Chất** | `+100 Sinh Mệnh Lực Tối Đa`; `+100 Thể Lực Tối Đa`; `+5 Giáp`; `+10 Định Tính Tối Đa` | Điểm |
| **Nhanh Nhẹn** | `+2 Tốc Độ Đánh`; `+8 Tốc Độ Di Chuyển` | đòn/s; m/s |
| **Tinh Thần** | `+10 Công Pháp Thuật`; `+100 Tinh Lực Tối Đa`; `+5 Kháng Phép`; `+10 Định Tính Tối Đa` | Điểm |

`Định Tính Tối Đa` nhận đồng thời đóng góp `10 × Thể Chất + 10 × Tinh Thần`; không chỉ chọn một phía.

Không có chuyển đổi mặc định từ Thuộc Tính sang **Hồi Phục flat** hoặc **Tỷ Lệ Hồi Phục % Tối Đa/s**. Hồi phục có thể được cấp bởi nguồn riêng. Điều này không cấm một mechanic cụ thể có công thức hồi phục rõ ràng, nhưng không được hiểu rằng mọi Thuộc Tính đều tự cấp hồi phục.

### 5.3. Bảng Chỉ Số Trung Cấp — Mặc Định v2

| Thuộc Tính | Cứ +10 Effective tạo ra | Đơn vị |
|---|---|---|
| **Sức Mạnh** | `+1 Xuyên Giáp` | Điểm |
| **Thể Chất** | `+1 Giá Trị Vật Lý Kháng Tính` | Giá trị Kháng `R` |
| **Nhanh Nhẹn** | `+1 Chính Xác` và `+1 Né Tránh` | Điểm |
| **Tinh Thần** | `+1 Xuyên Kháng Phép` và `+1 Giá Trị Pháp Thuật Kháng Tính` | Điểm; giá trị Kháng `R` |

Ví dụ `Nhanh Nhẹn = 15 Effective` → `+1.5 Chính Xác` và `+1.5 Né Tránh` trước các nguồn khác; **không** làm tròn thành `+1`.

`+1 Giá Trị Kháng` là `+1` đơn vị đầu vào `R` của công thức Kháng tiệm cận tại [[CHỈ SỐ#3.3. Mô Hình Kháng Tiệm Cận]], **không** có nghĩa giảm đúng `1%` sát thương. Các nguồn Kháng độc lập vẫn được xử lý theo quy tắc stacking đã frozen; không cộng toàn bộ nguồn thành một phần trăm hiệu lực.

Không chuyển trực tiếp các Chỉ Số Trung Cấp còn lại bằng bảng mặc định. Nguồn riêng muốn bổ sung hiệu ứng phải định nghĩa rành mạch, không suy diễn tự động từ tên Thuộc Tính.

### 5.4. Năng Lượng Tối Đa

`Năng Lượng` là nhóm Tài Nguyên có nhiều pool riêng; **không** tự sinh một pool chỉ vì Tinh Thần tăng. Đối với mỗi pool đã mở khóa và có liên kết với Tinh Thần:

$$
E_{\mathrm{max,pool}}=100\times T_{\mathrm{Effective}}\times C_{\mathrm{compatible}}
$$

- `C_tương thích = 0`: không có đóng góp từ Tinh Thần; **không** đồng nghĩa pool bị xóa.
- `C_tương thích = 1`: hệ số chuẩn của một pool tương thích đã mở khóa.
- `C_tương thích > 0` khác `1`: do Công Pháp, Nghề Nghiệp, Chủng Tộc, Thiên Phú hoặc mechanic sở hữu; không có giới hạn cứng toàn hệ thống.
- Một cá thể có thể có nhiều pool, mỗi pool có `C_tương thích` riêng. Các pool độc lập không tự chuyển lượng hiện tại cho nhau.
- Pool không tương thích/không mở khóa **không** nhận dung lượng hoặc trạng thái mới từ công thức này.

Giá trị **hiện tại** của Tài Nguyên thuộc [[TÀI NGUYÊN]], không phải Thuộc Tính. Khi Tối Đa thay đổi do Effective, không tự thêm lượng hiện tại; nếu vượt giới hạn mới thì xử lý theo quy tắc pool tại [[TÀI NGUYÊN]].

### 5.5. Chỉ Số Không Được Chuyển Đổi Mặc Định

- Mọi Chỉ Số **Thượng Cấp**.
- Các Chỉ Số dạng **xác suất** và `Kháng Chí Mạng` (phán định xác suất).
- `Hút Máu Đòn Đánh`, `Hút Máu Kỹ Năng` và các chỉ số Hút Máu khác.
- Mọi `% Tăng Sát Thương` theo Loại/tag.
- `Tỷ Lệ Hồi Phục <Tài Nguyên>` và `Tỷ Lệ Hồi Phục Định Tính` (% Tối Đa/s).

`Chính Xác/Né Tránh` là **Điểm**, không phải xác suất trực tiếp, nên được chuyển đổi theo mục 5.3. Phân biệt tương tự với Giá Trị Kháng `R`.

---

## 6. Quy Đổi Giữa Các Power System

Các power system (Tu Tiên, Tây Huyễn, Hắc Khoa Kỹ, phó bản nguyên tác...) ánh xạ về **cùng một thang Thuộc Tính**, không có đơn vị theo bậc Chuyển hoặc Equivalent. Không xóa lore và mechanic bản địa.

Bảng ở mục 5 là **chuẩn mặc định Ideaverse**. Nếu một Nghề Nghiệp, Công Pháp, Kỹ Năng hoặc Chủng Tộc có hệ số khác, nó phải ghi rõ **đóng góp nào bị thay thế/bổ sung, áp dụng trước hay sau conversion**, và tránh nhân/cộng trùng một nguồn. Không mặc định mọi build dùng các hệ số riêng khác nhau như v1.

---

## 7. Frozen Boundary — v2

Đã khóa: danh sách 7 Thuộc Tính; chuẩn `0/~0.5/1/>1`; Base/Effective; không hard cap; Điểm Tự Do `+1 Base`; 10 Chuyển; Hồi Báo Thí Luyện `×2/×5/×10/×100` **không Chiết Xuất**; tên Thuộc Tính không thêm hậu tố; chuyển đổi Cơ Sở theo bảng và Trung Cấp `10→1` có thập phân; loại trừ Thượng Cấp, xác suất, Hút Máu, tăng sát thương và hồi phục `%/s`; quy tắc tương thích Năng Lượng.

Lịch sử thiết kế cũ: [[HỆ THỐNG THUỘC TÍNH v1]] **đã bị thay thế**. Phần Chiết Xuất trong v1 chỉ tồn tại như hồ sơ lịch sử, không còn hiệu lực canonical.
