---
status: frozen
version: 1
system: Thuộc Tính
---

# HỆ THỐNG THUỘC TÍNH v1

> [!SUCCESS] FROZEN
> Tài liệu này ghi **decision log** của Hệ Thống Thuộc Tính v1. Source of truth chi tiết: [[THUỘC TÍNH]]. Nếu một quyết định ở đây được mở lại, đổi trạng thái tại [[DESIGN STATUS]] thành `REOPENED` trước khi sửa canonical rule.

## Frozen Decisions

### 1. Danh Sách Thuộc Tính

**Cơ Bản**

- Sức Mạnh
- Thể Chất
- Nhanh Nhẹn
- Tinh Thần

**Đặc Biệt**

- Ngộ Tính
- Mị Lực
- Vận Khí

### 2. Thang Giá Trị

- Thang tuyến tính trong cùng bậc biểu diễn.
- `1` = cực hạn tự nhiên của người thường đối với Thuộc Tính tương ứng.
- Với Thuộc Tính Cơ Bản, `~0.5` là tham chiếu gần đúng cho người trưởng thành khỏe mạnh bình thường.
- Chủng tộc khác có thể sinh ra/trưởng thành với Base `>1`.
- Không có hard cap.
- Cho phép scientific notation.

### 3. Base / Effective

- Base chứa toàn bộ tăng trưởng vĩnh viễn.
- Effective dùng Base + flat modifier rồi nhân các `%` modifier độc lập.

$$
E_{raw}=(B+\sum F_i)\times\prod_j(1+M_j)
$$

- Bốn Thuộc Tính Cơ Bản có Effective floor `0`.
- Ngộ Tính: Base không âm, Effective có thể âm.
- Mị Lực và Vận Khí: Base/Effective có thể âm.

### 4. Điểm Thuộc Tính Tự Do

- Chỉ phân bổ trực tiếp vào Thuộc Tính Cơ Bản.
- `1 điểm = +1 Base` tại bậc Chuyển hiện tại.
- Điểm có trước Chuyển bị xử lý cùng Base qua Hồi Báo + Chiết Xuất.
- Điểm nhận sau Chuyển cộng thẳng vào Base của bậc mới.
- Nghề Nghiệp phẩm chất cao nhất độc hữu MC: `+10` điểm/level.
- Nhân vật khác: tối đa `+5` điểm/level từ Nghề Nghiệp.
- Vật phẩm trao điểm trực tiếp cực kỳ hiếm.

### 5. Chuyển và Chiết Xuất

- 10 Chuyển: `I` → `X`.
- Áp dụng đồng thời cho Sức Mạnh, Thể Chất, Nhanh Nhẹn, Tinh Thần.
- Cách hiển thị: `Sức Mạnh I: x`, không dùng `Sức Mạnh: x I`.

Bốn bậc Thí Luyện:

| Bậc | Hồi Báo `R` | K |
|---:|---:|---:|
| I | `×2` | `2` |
| II | `×5` | `5` |
| III | `×10` | `10` |
| IV | `×100` | `100` |

Quy tắc:

$$
K=R
$$

$$
B_{reward}=B_{before}\times R
$$

$$
B_{after}=\frac{B_{reward}}{K}
$$

Hồi Báo tăng Base thật; Chiết Xuất nén nó sang đơn vị chất lượng cao hơn. Với `K=R`, số hiển thị có thể giữ nguyên nhưng Equivalent tăng theo chất lượng đơn vị mới.

### 6. Hệ Số Chiết Xuất Tích Lũy

Vì mỗi lần Chuyển có thể chọn bậc Thí Luyện khác nhau:

$$
C_r=\prod_{j=1}^{r}K_j
$$

$$
B_{equivalent}=B_{displayed}\times C_r
$$

Không dùng công thức cũ `K^r`.

Hai nhân vật cùng bậc Chuyển và cùng số hiển thị có thể khác Equivalent nếu lịch sử Thí Luyện khác nhau.

### 7. Thuộc Tính → Chỉ Số/Tài Nguyên

Không có conversion table toàn cục.

$$
Contribution=EffectiveAttribute\times C
$$

`C` do Chủng Tộc, Nghề Nghiệp, Công Pháp, Huyết Mạch, Thiên Phú, power system hoặc mechanic sở hữu.

Quan hệ mặc định:

- Sức Mạnh → Công Vật Lý / phát lực / một phần đại lượng vật lý phù hợp.
- Thể Chất → Sinh Mệnh Lực Tối Đa / Thể Lực Tối Đa / hồi phục thể chất.
- Nhanh Nhẹn → Tốc Độ Đánh / Tốc Độ Di Chuyển / Chính Xác / Né Tránh.
- Tinh Thần → Tinh Lực Tối Đa / Năng Lượng phù hợp / Công Pháp Thuật khi power system sử dụng.

### 8. Thuộc Tính Đặc Biệt

- Không nhận Điểm Thuộc Tính Tự Do thông thường.
- Không Chiết Xuất.
- Không mặc định sinh Chỉ Số chiến đấu trực tiếp.
- Ngộ Tính: học/lĩnh ngộ/suy diễn/cải tiến.
- Mị Lực: sức hấp dẫn/ấn tượng, không phải Danh Vọng.
- Vận Khí: chỉ ảnh hưởng các kết quả vốn có xác suất `>0`; không tạo khả năng từ `0`.

### 9. Quy Đổi Xuyên Thế Giới

Mọi power system có thể quy về lớp Thuộc Tính chuẩn của Ideaverse để so sánh nhưng vẫn giữ lore/hệ thống bản địa.

## Ngoài Phạm Vi v1

Các mục sau thuộc subsystem khác và **không phải phần mở của Thuộc Tính v1**:

- exact conversion coefficient của từng build;
- tên lore chính thức của bốn bậc Thí Luyện;
- điều kiện Chuyển/Thí Luyện;
- bảng progression chi tiết của từng Nghề Nghiệp.
