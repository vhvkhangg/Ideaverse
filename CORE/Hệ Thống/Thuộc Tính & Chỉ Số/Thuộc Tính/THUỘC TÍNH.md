# THUỘC TÍNH

> [!ABSTRACT] Source of Truth
> Đây là nguồn định nghĩa chính thức cho **hệ thống Thuộc Tính** của Ideaverse. Bản đồ subsystem: [[HỆ THỐNG THUỘC TÍNH & CHỈ SỐ]].

## 1. Phân Loại

### 1.1. Thuộc Tính Cơ Bản

Các thuộc tính có thể tăng bằng phương thức tăng trưởng thông thường như lên cấp, Điểm Thuộc Tính Tự Do, rèn luyện hoặc cơ chế phổ thông tương đương.

- [[Sức Mạnh]]
- [[Thể Chất]]
- [[Nhanh Nhẹn]]
- [[Tinh Thần]]

Bốn Thuộc Tính Cơ Bản chịu cơ chế **Chiết Xuất Thuộc Tính** khi Nghề Nghiệp Chuyển.

### 1.2. Thuộc Tính Đặc Biệt

Các thuộc tính không tăng bằng phương thức thông thường. Chúng chỉ thay đổi thông qua điều kiện, cơ duyên, năng lực, vật phẩm, trạng thái hoặc phương thức đặc thù được hệ thống cho phép.

- [[Ngộ Tính]]
- [[Mị Lực]]
- [[Vận Khí]]

Thuộc Tính Đặc Biệt **không** chịu Chiết Xuất Thuộc Tính theo Chuyển Nghề.

## 2. Quy Chuẩn Giá Trị

### 2.1. Thang Tuyến Tính

Giá trị Thuộc Tính sử dụng **thang tuyến tính**.

- Trong cùng một thuộc tính, chênh lệch giá trị biểu thị chênh lệch tuyến tính về đại lượng chuẩn hóa của thuộc tính đó.
- `1` là **mốc cực hạn tự nhiên của người thường** đối với thuộc tính tương ứng.
- Giá trị `> 1` biểu thị mức đã vượt cực hạn người thường.
- Giá trị rất lớn có thể viết bằng scientific notation, ví dụ `1e10`, `3e50`.

> [!IMPORTANT]
> Thang Thuộc Tính tuyến tính không đồng nghĩa mọi **chỉ số dẫn xuất** hoặc xác suất đều phải tuyến tính. Ví dụ `Vận Khí: 2` không mặc định có nghĩa mọi xác suất tốt đều tăng gấp đôi; công thức tác động cụ thể thuộc về cơ chế sử dụng Vận Khí.

### 2.2. Giá Trị Cơ Sở và Giá Trị Hiệu Lực

- **Giá Trị Cơ Sở (Base):** giá trị nội tại hoặc đã được tăng trưởng vĩnh viễn của cá thể.
- **Giá Trị Hiệu Lực (Effective):** giá trị thực sự được sử dụng sau khi áp dụng modifier, buff, debuff, trang bị, trạng thái và các hiệu ứng hợp lệ khác.

Công thức tổng quát chưa bị khóa; từng subsystem có thể quy định cách modifier tác động miễn không làm thay đổi định nghĩa của Base và Effective.

### 2.3. Giá Trị Âm

| Thuộc tính | Base âm | Effective âm | Quy tắc |
|---|:---:|:---:|---|
| Sức Mạnh | Không | Không | Sàn tại `0`. |
| Thể Chất | Không | Không | Sàn tại `0`. |
| Nhanh Nhẹn | Không | Không | Sàn tại `0`. |
| Tinh Thần | Không | Không | Sàn tại `0`. |
| Ngộ Tính | Không | Có | Base `>= 0`; modifier có thể làm Effective `< 0`. |
| Mị Lực | Có | Có | Giá trị âm biểu thị xu hướng gây bài xích/xa lánh thay vì hấp dẫn. |
| Vận Khí | Có | Có | Giá trị âm biểu thị thiên hướng bất lợi trong các sự kiện có yếu tố xác suất. |

## 3. Chiết Xuất Thuộc Tính

### 3.1. Phạm Vi

Chiết Xuất Thuộc Tính chỉ áp dụng cho bốn Thuộc Tính Cơ Bản:

- Sức Mạnh
- Thể Chất
- Nhanh Nhẹn
- Tinh Thần

Cơ chế gắn với **10 lần Chuyển của Nghề Nghiệp**, tương ứng các bậc `I` đến `X`.

### 3.2. Cách Ghi

Không Chuyển:

```text
Sức Mạnh: x
```

Sau Chuyển I:

```text
Sức Mạnh I: x
```

Sau Chuyển II:

```text
Sức Mạnh II: x
```

Tiếp tục tương tự tới:

```text
Sức Mạnh X: x
```

Bậc Chuyển là một phần của **tên hiển thị thuộc tính**, không viết theo dạng `Sức Mạnh: x I`.

### 3.3. Hệ Số Chiết Xuất

Gọi hệ số chiết xuất cố định là `K`.

- Cùng **một hệ số `K`** được sử dụng cho mọi lần Chuyển từ I đến X.
- Giá trị cụ thể của `K` **chưa được chốt**.
- Khi tăng một bậc Chuyển, giá trị hiển thị của thuộc tính được chia cho `K`.
- Chiết xuất là phép đổi cấp biểu diễn; tại thời điểm chiết xuất, nó không tự làm nhân vật yếu đi.

Ví dụ ký hiệu:

```text
Sức Mạnh: A
→ Chuyển I
Sức Mạnh I: A / K
```

```text
Sức Mạnh I: B
→ Chuyển II
Sức Mạnh II: B / K
```

Với bậc Chuyển `r` (`0 ≤ r ≤ 10`), giá trị quy đổi về cấp chưa Chuyển là:

```text
Giá trị quy đổi = Giá trị hiển thị × K^r
```

Trong đó `r = 0` là chưa Chuyển.

> [!NOTE]
> Điều kiện để Nghề Nghiệp được Chuyển và giá trị cụ thể của `K` thuộc phần thiết kế Nghề Nghiệp, chưa freeze tại đây.

## 4. Quy Đổi Giữa Các Power System

Mọi power system mà MC gặp — Tu Tiên, Tây Huyễn, Hắc Khoa Kỹ, hệ thống của phó bản nguyên tác... — được **quy đổi về cùng lớp Thuộc Tính chuẩn của Ideaverse** để so sánh.

Quy đổi không xóa hệ thống bản địa. Một nhân vật vẫn có thể giữ Hồn Lực, Mana, Linh Lực, Racial Class, cảnh giới hoặc cơ chế nguyên tác; lớp Thuộc Tính chỉ cung cấp chuẩn đo chung xuyên thế giới.

## 5. Danh Sách Thuộc Tính

### Cơ Bản

- [[Sức Mạnh]]
- [[Thể Chất]]
- [[Nhanh Nhẹn]]
- [[Tinh Thần]]

### Đặc Biệt

- [[Ngộ Tính]]
- [[Mị Lực]]
- [[Vận Khí]]

## 6. Chưa Freeze

- Giá trị cụ thể của hệ số chiết xuất `K`.
- Cách nhận và quy đổi Điểm Thuộc Tính Tự Do thành Giá Trị Thuộc Tính.
- Công thức modifier chi tiết.
- Công thức chuyển Thuộc Tính thành các Chỉ Số dẫn xuất.
