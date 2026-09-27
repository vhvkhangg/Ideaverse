---

aliases:

- Sức Mạnh Huấn Luyện
    
- Lực Lượng Huấn Luyện  
    type: skill  
    category: kỹ-năng-thông-dụng  
    quality: Tuyệt Cao Vô Thượng  
    level: vô-hạn  
    owner:
    
- Nhân vật chính  
    status: bản-nháp  
    tags:
    
- he-thong-suc-manh
    
- ky-nang
    
- suc-manh
    
- nhan-vat-chinh
    

---

> [!info] Thông tin cơ bản
> 
> - **Loại:** Kỹ năng thông dụng
>     
> - **Phẩm chất hiện tại:** Tuyệt Cao Vô Thượng
>     
> - **Cấp tối đa:** Vô hạn
>     
> - **Phương thức nâng cấp:** Tiêu hao Điểm Giết Quái
>     
> - **Số đặc tính tối đa:** 5
>     
> - **Điều kiện sử dụng:** Không giới hạn chức nghiệp
>     
> - **Người sở hữu duy nhất phẩm chất Tuyệt Cao Vô Thượng:** Nhân vật chính
>     

## Giới thiệu

**Sức Mạnh Huấn Luyện** là kỹ năng thông dụng cho phép người sở hữu không ngừng rèn luyện và cường hóa thuộc tính **Sức Mạnh**.

Kỹ năng này không yêu cầu chức nghiệp, huyết mạch, chủng tộc hoặc phương thức chiến đấu cụ thể. Bất kỳ sinh vật nào đáp ứng điều kiện học tập đều có thể sở hữu phiên bản thông thường của kỹ năng.

Tuy nhiên, chỉ riêng nhân vật chính có thể sử dụng **Điểm Giết Quái** để liên tục nâng cấp kỹ năng, đột phá giới hạn phẩm chất và cuối cùng tiến hóa kỹ năng đến phẩm chất độc nhất:

> **Tuyệt Cao Vô Thượng**

Ở phẩm chất này, cấp độ của kỹ năng không còn tồn tại giới hạn trên.

---

# I. Cơ chế nâng cấp

## 1. Nâng cấp kỹ năng

Nhân vật chính có thể tiêu hao **Điểm Giết Quái** để nâng cấp **Sức Mạnh Huấn Luyện**.

Mỗi lần nâng cấp:

- Cấp kỹ năng tăng thêm `1`.
    
- Hiệu quả cơ sở của kỹ năng được tăng cường.
    
- Những đặc tính đã mở khóa được tính lại theo cấp kỹ năng hiện tại.
    
- Chi phí nâng cấp tăng dần theo cấp độ và phẩm chất kỹ năng.
    

> [!note] Quy tắc hồi tố  
> Khi một đặc tính mới được mở khóa, cấp đặc tính được tính trực tiếp từ cấp hiện tại của kỹ năng.
> 
> Nhân vật chính không cần nâng kỹ năng lại từ đầu để cường hóa đặc tính vừa nhận được.

## 2. Thăng phẩm kỹ năng

Khi đáp ứng điều kiện thăng phẩm, nhân vật chính có thể tiêu hao Điểm Giết Quái và vật liệu đặc thù để nâng phẩm chất của kỹ năng.

Mỗi lần thăng phẩm:

- Mở khóa `1` đặc tính mới.
    
- Tăng hệ số phát triển của hiệu quả cơ sở.
    
- Có thể bổ sung quy tắc đặc biệt cho kỹ năng.
    
- Không làm mất cấp kỹ năng hiện tại.
    

|Lần thăng phẩm|Đặc tính được mở khóa|
|--:|---|
|Thăng phẩm lần 1|Lực Đạo Chuyển Hóa|
|Thăng phẩm lần 2|Bá Lực Gia Trì|
|Thăng phẩm lần 3|Cự Lực Bội Tăng|
|Thăng phẩm lần 4|Phá Giáp Trực Chỉ|
|Thăng phẩm lần 5|Vạn Lực Phá Pháp|

> [!warning] Chưa xác định  
> Tên của các phẩm chất trung gian sẽ được bổ sung sau khi hệ thống phẩm chất chung của thế giới được hoàn thiện.

---

# II. Hiệu quả cơ sở

## 1. Gia tăng Sức Mạnh

Mỗi cấp kỹ năng cung cấp:

```text
+10 Sức Mạnh
```

Công thức:

```text
Sức Mạnh cộng thêm = Cấp kỹ năng × 10
```

Ví dụ:

|Cấp kỹ năng|Sức Mạnh cộng thêm|
|--:|--:|
|1|10|
|10|100|
|50|500|
|100|1.000|
|1.000|10.000|

## 2. Gia tăng Sức Mạnh Phán Định

Mỗi cấp kỹ năng cung cấp:

```text
+0,2% Sức Mạnh Phán Định
```

Công thức:

```text
Sức Mạnh Phán Định cộng thêm = Cấp kỹ năng × 0,2%
```

**Sức Mạnh Phán Định** không trực tiếp tham gia tính toán sát thương.

Chỉ số này chỉ được sử dụng trong những tình huống yêu cầu tiến hành phán định dựa trên thuộc tính Sức Mạnh, bao gồm:

- Đáp ứng điều kiện thuộc tính để sử dụng trang bị.
    
- Đáp ứng điều kiện học tập kỹ năng.
    
- Đáp ứng điều kiện chuyển chức hoặc tiến giai.
    
- Tính toán sinh mệnh dựa trên Sức Mạnh.
    
- Tính toán sức chịu tải.
    
- Phán định phá hủy, đẩy lùi, áp chế hoặc vật lộn.
    
- Những hiệu quả đặc biệt ghi rõ sử dụng Sức Mạnh Phán Định.
    

Công thức:

```text
Sức Mạnh Phán Định
= Sức Mạnh thực tế × (1 + tỷ lệ Sức Mạnh Phán Định)
```

Ví dụ:

```text
Sức Mạnh thực tế: 1.000
Sức Mạnh Phán Định cộng thêm: 20%

Sức Mạnh Phán Định
= 1.000 × 1,2
= 1.200
```

Nhân vật vẫn chỉ có `1.000` Sức Mạnh khi tính sát thương, nhưng được xem là có `1.200` Sức Mạnh khi tiến hành các loại phán định phù hợp.

---

# III. Đặc tính kỹ năng

## Đặc tính 1: Lực Đạo Chuyển Hóa

> Sức mạnh thuần túy của người sở hữu được chuyển hóa thành lực công kích với hiệu suất vượt xa sinh vật thông thường.

### Hiệu quả

Mỗi `1` cấp kỹ năng:

```text
+0,1 hệ số chuyển đổi Sức Mạnh thành Tấn Công Vật Lý
```

Cấp đặc tính:

```text
Cấp Lực Đạo Chuyển Hóa
= floor(Cấp kỹ năng ÷ 10)
```

Hệ số chuyển đổi:

```text
Hệ số chuyển đổi cuối cùng
= Hệ số chuyển đổi cơ sở + Cấp đặc tính × 0,1
```

Ví dụ, hệ số chuyển đổi cơ sở của nhân vật là:

```text
1 Sức Mạnh → 1 Tấn Công Vật Lý
```

Khi kỹ năng đạt cấp `100`:

```text
Cấp đặc tính = 100 ÷ 10 = 10
Hệ số cộng thêm = 10 × 0,1 = 1

1 Sức Mạnh → 2 Tấn Công Vật Lý
```

### Quy tắc

- Chỉ tăng hiệu suất chuyển đổi từ Sức Mạnh sang Tấn Công Vật Lý.
    
- Không trực tiếp tăng thuộc tính Sức Mạnh.
    
- Có thể cộng dồn với hệ số chuyển đổi từ chức nghiệp, huyết mạch, trang bị và thiên phú.
    
- Những hệ số cùng loại được cộng trước khi tính Tấn Công Vật Lý.
    

---

## Đặc tính 2: Bá Lực Gia Trì

> Mỗi phần lực lượng của người sở hữu đều có thể bộc phát uy lực vượt qua giới hạn thông thường.

### Hiệu quả

Mỗi `5` cấp kỹ năng:

```text
+1% Tấn Công Vật Lý
```

Công thức:

```text
Tỷ lệ Tấn Công Vật Lý cộng thêm
= floor(Cấp kỹ năng ÷ 10) × 1%
```

Ví dụ:

|Cấp kỹ năng|Tấn Công Vật Lý cộng thêm|
|--:|--:|
|10|1%|
|50|5%|
|100|10%|
|500|50%|
|1.000|100%|

### Quy tắc

- Tăng Tấn Công Vật Lý cuối cùng sau khi hoàn tất chuyển đổi thuộc tính.
    
- Có hiệu lực với Tấn Công Vật Lý đến từ Sức Mạnh, trang bị, chức nghiệp và những nguồn hợp lệ khác.
    
- Không tăng Công Kích Pháp Thuật.
    
- Không tự động tăng sát thương kỹ năng nếu kỹ năng đó không sử dụng Tấn Công Vật Lý.
    

---

## Đặc tính 3: Cự Lực Bội Tăng

> Sức Mạnh của người sở hữu được khuếch đại toàn diện, khiến mọi nguồn gia tăng Sức Mạnh đều đạt hiệu quả cao hơn.

### Hiệu quả

Mỗi `10` cấp kỹ năng:

```text
+1% Sức Mạnh
```

Công thức:

```text
Tỷ lệ Sức Mạnh cộng thêm
= floor(Cấp kỹ năng ÷ 10) × 1%
```

Sức Mạnh cuối cùng:

```text
Sức Mạnh cuối cùng
= Sức Mạnh trước khuếch đại
× (1 + tổng tỷ lệ tăng Sức Mạnh)
```

### Quy tắc

- Có hiệu lực với Sức Mạnh cơ sở.
    
- Có hiệu lực với Sức Mạnh từ kỹ năng.
    
- Có hiệu lực với Sức Mạnh từ trang bị, chức nghiệp, huyết mạch và thiên phú.
    
- Không khuếch đại Sức Mạnh Phán Định.
    
- Sức Mạnh Phán Định được tính sau khi Sức Mạnh thực tế đã hoàn tất khuếch đại.
    

---

## Đặc tính 4: Phá Giáp Trực Chỉ

> Lực lượng đạt đến cực hạn không còn đơn thuần va chạm với phòng ngự, mà trực tiếp xuyên thấu kết cấu bảo hộ của mục tiêu.

### Hiệu quả

Mỗi `20` cấp kỹ năng:

```text
Bỏ qua 0,5% Giáp
Bỏ qua 5 điểm Giáp
```

Công thức:

```text
Bỏ qua Giáp theo tỷ lệ
= floor(Cấp kỹ năng ÷ 10) × 0,5%
```

```text
Bỏ qua Giáp cố định
= floor(Cấp kỹ năng ÷ 10) × 5
```

### Thứ tự tính toán

Khi nhân vật tấn công mục tiêu:

1. Xác định Giáp ban đầu của mục tiêu.
    
2. Áp dụng hiệu quả bỏ qua Giáp theo tỷ lệ.
    
3. Áp dụng hiệu quả bỏ qua Giáp cố định.
    
4. Dùng lượng Giáp còn lại để tính giảm sát thương.
    

Công thức:

```text
Giáp hữu hiệu
= Giáp ban đầu
× (1 - tỷ lệ bỏ qua Giáp)
- lượng Giáp bỏ qua cố định
```

Giáp hữu hiệu không thể thấp hơn `0`, trừ khi hệ thống sau này bổ sung cơ chế Giáp Âm.

### Ví dụ

```text
Giáp mục tiêu: 2.000
Bỏ qua Giáp: 10%
Bỏ qua Giáp cố định: 100

Giáp hữu hiệu
= 2.000 × 0,9 - 100
= 1.700
```

---

## Đặc tính 5: Vạn Lực Phá Pháp

> Khi lực lượng vượt qua giới hạn của quy tắc thông thường, những phương thức suy giảm tổn thương dựa trên kỹ xảo, thiên phú hoặc quyền năng đều có thể bị cưỡng ép phá vỡ.

### Hiệu quả

Mỗi `50` cấp kỹ năng:

```text
Bỏ qua 1 dòng Giảm Tổn Thương Vật Lý
```

Công thức:

```text
Số dòng có thể bỏ qua
= floor(Cấp kỹ năng ÷ 50)
```

### Khái niệm “một dòng giảm tổn thương”

Mỗi hiệu quả độc lập được xem là một dòng riêng biệt.

Ví dụ, mục tiêu có:

1. Trang bị: Giảm `15%` tổn thương vật lý.
    
2. Thiên phú: Giảm `10%` tổn thương vật lý.
    
3. Kỹ năng bị động: Giảm `20%` tổn thương vật lý.
    
4. Trạng thái phòng thủ: Giảm `30%` tổn thương vật lý.
    

Mục tiêu được xem là có `4` dòng Giảm Tổn Thương Vật Lý.

Nếu nhân vật có thể bỏ qua `2` dòng, hai hiệu quả có giá trị cao nhất sẽ bị vô hiệu hóa đối với đòn tấn công của nhân vật.

Trong ví dụ trên, nhân vật bỏ qua:

- Trạng thái phòng thủ giảm `30%`.
    
- Kỹ năng bị động giảm `20%`.
    

Hai dòng còn lại vẫn có hiệu lực.

### Thứ tự ưu tiên

Đặc tính tự động bỏ qua các dòng theo thứ tự:

1. Dòng có tỷ lệ giảm tổn thương cao nhất.
    
2. Dòng có giá trị giảm cố định cao nhất.
    
3. Nếu hai dòng có giá trị bằng nhau, ưu tiên dòng có thời gian duy trì lâu hơn.
    
4. Nếu vẫn bằng nhau, ưu tiên dòng được kích hoạt trước.
    

### Không được tính là dòng giảm tổn thương

Đặc tính này không bỏ qua:

- Chỉ số Giáp.
    
- Khiên hấp thu sát thương.
    
- Né tránh.
    
- Miễn nhiễm sát thương tuyệt đối.
    
- Trạng thái không thể bị chọn làm mục tiêu.
    
- Quy tắc cốt truyện hoặc quyền năng có cấp bậc tuyệt đối cao hơn kỹ năng.
    
- Hiệu quả chuyển tổn thương sang mục tiêu khác.
    
- Hiệu quả hồi phục sau khi nhận sát thương.
    

Trừ khi một hiệu quả ghi rõ:

```text
Giảm Tổn Thương Vật Lý
```

### Quy tắc dư thừa

Nếu số dòng có thể bỏ qua lớn hơn số dòng giảm tổn thương của mục tiêu:

- Phần dư không chuyển thành xuyên Giáp.
    
- Phần dư không chuyển thành tăng sát thương.
    
- Phần dư không được lưu lại cho lần tấn công tiếp theo.
    

---

# IV. Thứ tự tính toán hoàn chỉnh

Khi tính toán sức chiến đấu của người sở hữu, áp dụng theo thứ tự:

## Bước 1: Tính Sức Mạnh trước khuếch đại

```text
Sức Mạnh trước khuếch đại
= Sức Mạnh cơ sở
+ Sức Mạnh từ cấp độ
+ Sức Mạnh từ trang bị
+ Sức Mạnh từ chức nghiệp
+ Sức Mạnh từ kỹ năng
+ Sức Mạnh từ các nguồn khác
```

## Bước 2: Áp dụng Cự Lực Bội Tăng

```text
Sức Mạnh thực tế
= Sức Mạnh trước khuếch đại
× (1 + tổng tỷ lệ tăng Sức Mạnh)
```

## Bước 3: Tính Sức Mạnh Phán Định

```text
Sức Mạnh Phán Định
= Sức Mạnh thực tế
× (1 + tỷ lệ Sức Mạnh Phán Định)
```

Sức Mạnh Phán Định không tham gia bước tính Tấn Công Vật Lý.

## Bước 4: Tính chuyển đổi Sức Mạnh

```text
Tấn Công Vật Lý từ Sức Mạnh
= Sức Mạnh thực tế
× hệ số chuyển đổi Sức Mạnh
```

## Bước 5: Tính tổng Tấn Công Vật Lý

```text
Tấn Công Vật Lý trước khuếch đại
= Tấn Công Vật Lý từ Sức Mạnh
+ Tấn Công Vật Lý từ trang bị
+ Tấn Công Vật Lý từ chức nghiệp
+ Tấn Công Vật Lý từ các nguồn khác
```

## Bước 6: Áp dụng Bá Lực Gia Trì

```text
Tấn Công Vật Lý cuối cùng
= Tấn Công Vật Lý trước khuếch đại
× (1 + tổng tỷ lệ tăng Tấn Công Vật Lý)
```

## Bước 7: Xử lý phòng ngự của mục tiêu

1. Bỏ qua các dòng Giảm Tổn Thương Vật Lý bằng **Vạn Lực Phá Pháp**.
    
2. Bỏ qua Giáp theo tỷ lệ bằng **Phá Giáp Trực Chỉ**.
    
3. Bỏ qua Giáp cố định.
    
4. Tính Giáp hữu hiệu.
    
5. Tính sát thương vật lý cuối cùng.
    

---

# V. Ví dụ hoàn chỉnh

Giả sử nhân vật có:

```text
Sức Mạnh cơ sở: 1.000
Cấp Sức Mạnh Huấn Luyện: 100
Hệ số chuyển đổi cơ sở: 1 Sức Mạnh → 1 Tấn Công Vật Lý
Không có nguồn Tấn Công Vật Lý khác
```

## 1. Hiệu quả cơ sở

```text
Sức Mạnh từ kỹ năng
= 100 × 10
= 1.000
```

```text
Sức Mạnh trước khuếch đại
= 1.000 + 1.000
= 2.000
```

## 2. Cự Lực Bội Tăng

Ở cấp `100`:

```text
Tăng Sức Mạnh = 10%
```

```text
Sức Mạnh thực tế
= 2.000 × 1,1
= 2.200
```

## 3. Sức Mạnh Phán Định

Ở cấp `100`:

```text
Sức Mạnh Phán Định cộng thêm
= 100 × 0,2%
= 20%
```

```text
Sức Mạnh Phán Định
= 2.200 × 1,2
= 2.640
```

Nhân vật có:

- `2.200` Sức Mạnh thực tế.
    
- `2.640` Sức Mạnh Phán Định.
    

## 4. Lực Đạo Chuyển Hóa

Ở cấp `100`:

```text
Hệ số chuyển đổi cộng thêm
= 10 × 0,1
= 1
```

Hệ số cuối cùng:

```text
1 Sức Mạnh → 2 Tấn Công Vật Lý
```

Tấn Công Vật Lý từ Sức Mạnh:

```text
2.200 × 2
= 4.400
```

## 5. Bá Lực Gia Trì

Ở cấp `100`:

```text
Tăng Tấn Công Vật Lý = 10%
```

```text
Tấn Công Vật Lý cuối cùng
= 4.400 × 1,1
= 4.840
```

## 6. Phá Giáp Trực Chỉ

Ở cấp `100`:

```text
Bỏ qua 5% Giáp
Bỏ qua 50 Giáp
```

## 7. Vạn Lực Phá Pháp

Ở cấp `100`:

```text
Bỏ qua 2 dòng Giảm Tổn Thương Vật Lý
```

## Kết quả

Tại cấp kỹ năng `100`, nhân vật nhận được:

```text
+1.000 Sức Mạnh
+20% Sức Mạnh Phán Định
+1 hệ số chuyển đổi Sức Mạnh → Tấn Công Vật Lý
+10% Sức Mạnh
+10% Tấn Công Vật Lý
Bỏ qua 5% Giáp
Bỏ qua 50 Giáp
Bỏ qua 2 dòng Giảm Tổn Thương Vật Lý
```

---

# VI. Mô tả hiển thị rút gọn

> [!example] Sức Mạnh Huấn Luyện  
> **Phẩm chất:** Tuyệt Cao Vô Thượng  
> **Cấp:** 100  
> **Loại:** Kỹ năng thông dụng
> 
> **Hiệu quả cơ sở**
> 
> - Tăng `1.000` Sức Mạnh.
>     
> - Tăng `20%` Sức Mạnh Phán Định.
>     
> 
> **Đặc tính**
> 
> - **Lực Đạo Chuyển Hóa:** Tăng `1` hệ số chuyển đổi Sức Mạnh thành Tấn Công Vật Lý.
>     
> - **Bá Lực Gia Trì:** Tăng `10%` Tấn Công Vật Lý.
>     
> - **Cự Lực Bội Tăng:** Tăng `10%` Sức Mạnh.
>     
> - **Phá Giáp Trực Chỉ:** Bỏ qua `5%` và `50` điểm Giáp.
>     
> - **Vạn Lực Phá Pháp:** Bỏ qua `2` dòng Giảm Tổn Thương Vật Lý.
>     
> 
> **Nâng cấp:** Có thể sử dụng Điểm Giết Quái để tiếp tục tăng cấp.