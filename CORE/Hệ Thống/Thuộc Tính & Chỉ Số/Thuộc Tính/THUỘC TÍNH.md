---
type: system
status: frozen
version: 1
scope: attributes
tags:
  - ideaverse/system/attribute
---

# THUỘC TÍNH

> [!ABSTRACT] Source of Truth
> Đây là nguồn định nghĩa chính thức cho **Hệ Thống Thuộc Tính v1** của Ideaverse. Bản đồ subsystem: [[HỆ THỐNG THUỘC TÍNH & CHỈ SỐ]]. Decision log: [[HỆ THỐNG THUỘC TÍNH v1]].

## 1. Phân Loại

### 1.1. Thuộc Tính Cơ Bản

- [[Sức Mạnh]]
- [[Thể Chất]]
- [[Nhanh Nhẹn]]
- [[Tinh Thần]]

Thuộc Tính Cơ Bản có thể tăng bằng các phương thức tăng trưởng thông thường được hệ thống cho phép, gồm level, Điểm Thuộc Tính Tự Do, rèn luyện, Công Pháp, Nghề Nghiệp, Thiên Phú, vật phẩm hoặc cơ chế tương đương.

Bốn Thuộc Tính Cơ Bản chịu **Chiết Xuất Thuộc Tính** khi [[HỆ THỐNG NGHỀ NGHIỆP|Nghề Nghiệp]] Chuyển.

### 1.2. Thuộc Tính Đặc Biệt

- [[Ngộ Tính]]
- [[Mị Lực]]
- [[Vận Khí]]

Thuộc Tính Đặc Biệt không tăng bằng Điểm Thuộc Tính Tự Do hoặc tăng trưởng level thông thường. Chúng chỉ thay đổi bởi phương thức đặc biệt/hiếm hoặc một mechanic ghi rõ ngoại lệ.

Thuộc Tính Đặc Biệt **không** chịu Chiết Xuất theo Chuyển Nghề.

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

### 3.1. Phạm Vi

Điểm Thuộc Tính Tự Do chỉ phân bổ trực tiếp vào bốn Thuộc Tính Cơ Bản.

### 3.2. Quy Đổi

**1 Điểm Thuộc Tính Tự Do = +1 Base** của Thuộc Tính tại **bậc Chuyển hiện tại**.

Ví dụ chưa Chuyển:

```text
Sức Mạnh: 10
+1 Điểm Thuộc Tính Tự Do
→ Sức Mạnh: 11
```

Ví dụ ở Chuyển III:

```text
Sức Mạnh III: 10
+1 Điểm Thuộc Tính Tự Do
→ Sức Mạnh III: 11
```

Một điểm nhận sau Chuyển III có giá trị ở **đơn vị Sức Mạnh III**, không quy ngược thành `+1` của bậc chưa Chuyển.

### 3.3. Thời Điểm Nhận Điểm và Chiết Xuất

- Điểm đã cộng **trước Chuyển** trở thành một phần của Base hiện tại và bị xử lý cùng toàn bộ Base khi Thí Luyện + Chiết Xuất.
- Điểm nhận **sau Chuyển** cộng trực tiếp `+1 Base` ở bậc Chuyển mới.

### 3.4. Nguồn Nhận

Phân phối Điểm Thuộc Tính Tự Do thuộc quyền sở hữu của [[HỆ THỐNG NGHỀ NGHIỆP]]. Cross-system constraint đã chốt:

- Nghề Nghiệp phẩm chất cao nhất, độc hữu của Nhân Vật Chính: `+10` Điểm Thuộc Tính Tự Do mỗi level.
- Nhân vật khác: Nghề Nghiệp tối đa `+5` Điểm Thuộc Tính Tự Do mỗi level.
- Vật phẩm trực tiếp trao Điểm Thuộc Tính Tự Do tồn tại nhưng **cực kỳ hiếm**.

Exact distribution của từng Nghề Nghiệp vẫn thuộc thiết kế Nghề Nghiệp, không phải công thức Thuộc Tính.

---

## 4. Chuyển, Thí Luyện và Chiết Xuất Thuộc Tính

### 4.1. Phạm Vi

Cơ chế chỉ áp dụng cho:

- Sức Mạnh
- Thể Chất
- Nhanh Nhẹn
- Tinh Thần

Nghề Nghiệp có **10 lần Chuyển**, tương ứng bậc `I` đến `X`. Khi một lần Chuyển hoàn tất, cả bốn Thuộc Tính Cơ Bản được xử lý cùng lúc.

### 4.2. Cách Hiển Thị

```text
Sức Mạnh: x
Sức Mạnh I: x
Sức Mạnh II: x
...
Sức Mạnh X: x
```

Bậc Chuyển là một phần của tên hiển thị. Không dùng dạng `Sức Mạnh: x I`.

### 4.3. Bậc Thí Luyện

Mỗi lần Chuyển có bốn bậc Thí Luyện kỹ thuật. Tên lore riêng có thể được bổ sung trong Hệ Thống Nghề Nghiệp sau này.

| Bậc Thí Luyện | Hồi Báo `R` | Hệ Số Chiết Xuất `K` |
|---:|---:|---:|
| I | `×2` | `2` |
| II | `×5` | `5` |
| III | `×10` | `10` |
| IV | `×100` | `100` |

Quy tắc v1 dùng:

$$
K=R
$$

Điều này khiến Thí Luyện khó hơn không làm số hiển thị phình ra vô hạn; phần Hồi Báo được giữ lại dưới dạng **chất lượng của đơn vị Thuộc Tính sau Chiết Xuất**.

### 4.4. Trình Tự Chuyển

Gọi:

- `B_before`: Base ở bậc hiện tại ngay trước Chuyển;
- `R`: Hồi Báo của bậc Thí Luyện;
- `K`: Hệ Số Chiết Xuất tương ứng.

Bước 1 — Hồi Báo tăng thẳng vào Base:

$$
B_{reward}=B_{before}\times R
$$

Bước 2 — Chiết Xuất sang đơn vị bậc mới:

$$
B_{after}=\frac{B_{reward}}{K}
$$

Vì `K = R` trong v1:

$$
B_{after}=B_{before}
$$

**Con số hiển thị có thể giữ nguyên, nhưng sức mạnh không giữ nguyên.** Một đơn vị ở bậc mới mang giá trị quy đổi lớn hơn theo `K` của Thí Luyện vừa hoàn thành.

Ví dụ:

```text
Sức Mạnh: 10
Thí Luyện IV: ×100

Hồi Báo:
10 × 100 = 1000 Base cũ

Chiết Xuất K = 100:
1000 / 100 = 10

→ Sức Mạnh I: 10
```

`Sức Mạnh I: 10` ở ví dụ trên tương đương `1000` đơn vị Sức Mạnh chưa Chuyển.

### 4.5. Hệ Số Chiết Xuất Tích Lũy

Vì `K` có thể khác ở từng lần Chuyển, không dùng công thức cũ `K^r`.

Gọi:

$$
C_r=\prod_{j=1}^{r}K_j
$$

`Cᵣ` là **Hệ Số Chiết Xuất Tích Lũy** sau `r` lần Chuyển.

Giá trị quy đổi về đơn vị chưa Chuyển:

$$
B_{equivalent}=B_{displayed}\times C_r
$$

Ví dụ lịch sử Thí Luyện:

```text
Chuyển I:  ×2
Chuyển II: ×10
Chuyển III: ×100
```

thì:

```text
C₃ = 2 × 10 × 100 = 2000
```

Nếu:

```text
Sức Mạnh III: 12
```

thì:

```text
Equivalent chưa Chuyển = 12 × 2000 = 24000
```

> [!IMPORTANT]
> Hai nhân vật cùng `Sức Mạnh III: 12` chưa chắc mạnh tương đương nếu lịch sử Thí Luyện khác nhau. Khi cần so sánh tuyệt đối, phải dùng `Hệ Số Chiết Xuất Tích Lũy` hoặc giá trị Equivalent.

### 4.6. Ý Nghĩa Chiết Xuất

Chiết Xuất là **đổi đơn vị/chất lượng biểu diễn**, không phải nerf. Hồi Báo của Thí Luyện được áp dụng trước; Chiết Xuất chỉ nén giá trị về thang đọc được ở bậc mới.

Không có hard cap cho Base trước hoặc sau Chuyển.

---

## 5. Quan Hệ Thuộc Tính → Chỉ Số và Tài Nguyên

### 5.1. Không Có Universal Conversion Table

Ideaverse **không** dùng bảng toàn cục kiểu:

```text
1 Sức Mạnh = 10 Công Vật Lý
1 Thể Chất = 100 Sinh Mệnh Lực Tối Đa
```

Thay vào đó, mỗi subsystem/build định nghĩa **Hệ Số Chuyển Đổi** của riêng nó.

Với một đóng góp đơn:

$$
Contribution=EffectiveAttribute\times C
$$

Với nhiều Thuộc Tính cùng đóng góp:

$$
DerivedBase=\sum_i(EffectiveAttribute_i\times C_i)+OtherSources
$$

`Cᵢ` có thể được quyết định bởi:

- Chủng Tộc;
- Nghề Nghiệp;
- Công Pháp;
- Huyết Mạch;
- Thiên Phú;
- hệ thống sức mạnh của thế giới/phó bản;
- trạng thái hoặc mechanic đặc biệt khác.

### 5.2. Quan Hệ Mặc Định

Đây là **hướng đóng góp mặc định**, không phải độc quyền hay tỷ lệ cố định.

| Thuộc Tính | Các Chỉ Số/Tài Nguyên thường liên quan |
|---|---|
| **Sức Mạnh** | Công Vật Lý, khả năng phát lực, một phần Thể Lực hoặc Chỉ Số vật lý nếu build quy định. |
| **Thể Chất** | Sinh Mệnh Lực Tối Đa, Thể Lực Tối Đa, hồi phục thể chất, độ bền cơ thể. |
| **Nhanh Nhẹn** | Tốc Độ Đánh, Tốc Độ Di Chuyển, Chính Xác, Né Tránh và các đại lượng vận động phù hợp. |
| **Tinh Thần** | Tinh Lực Tối Đa, các Năng Lượng phù hợp, Công Pháp Thuật trong hệ thống phù hợp và khả năng vận hành tinh thần. |

Thuộc Tính chỉ là **một nguồn đóng góp**. Chỉ Số/Tài Nguyên còn có thể nhận giá trị từ Nghề Nghiệp, Công Pháp, Trang Bị, Thiên Phú, Huyết Mạch và các subsystem khác.

### 5.3. Thuộc Tính Đặc Biệt

Mặc định [[Ngộ Tính]], [[Mị Lực]] và [[Vận Khí]] **không sinh Chỉ Số chiến đấu trực tiếp theo một conversion table**.

- Ngộ Tính được subsystem học tập/lĩnh ngộ/cải tiến sử dụng.
- Mị Lực được subsystem xã hội/ấn tượng sử dụng.
- Vận Khí điều chỉnh trọng số của kết quả vốn đã có xác suất `> 0`; không tạo kết quả có xác suất `0`.

Một mechanic cụ thể có thể chuyển chúng thành Chỉ Số nếu ghi rõ ngoại lệ.

---

## 6. Quy Đổi Giữa Các Power System

Mọi power system mà MC gặp — Tu Tiên, Tây Huyễn, Hắc Khoa Kỹ, hệ thống phó bản nguyên tác... — được quy đổi về cùng lớp Thuộc Tính chuẩn của Ideaverse để so sánh.

Quy đổi không xóa hệ thống bản địa. Nhân vật vẫn giữ Mana, Hồn Lực, Linh Lực, Racial Class, Cảnh Giới hoặc mechanic nguyên tác; lớp Thuộc Tính chỉ là chuẩn đo xuyên thế giới.

Khi so sánh nhân vật ở các bậc Chuyển/lịch sử Thí Luyện khác nhau, sử dụng **Equivalent** sau khi tính Hệ Số Chiết Xuất Tích Lũy.

---

## 7. Frozen Boundary

Hệ Thống Thuộc Tính v1 đã khóa:

- danh sách và phân loại Thuộc Tính;
- chuẩn `0 / ~0.5 / 1 / >1` và không hard cap;
- Base/Effective và modifier multiplicative;
- Điểm Thuộc Tính Tự Do `+1 Base` tại bậc hiện tại;
- 10 Chuyển;
- bốn bậc Thí Luyện `×2 / ×5 / ×10 / ×100`;
- `K = 2 / 5 / 10 / 100` tương ứng;
- công thức Hồi Báo → Chiết Xuất → Equivalent;
- mô hình conversion coefficient sang Chỉ Số/Tài Nguyên;
- vai trò của ba Thuộc Tính Đặc Biệt.

Exact coefficient của từng Nghề Nghiệp/Công Pháp/Chủng Tộc và tên lore của các bậc Thí Luyện thuộc subsystem sở hữu chúng, không phải phần mở của Thuộc Tính v1.
