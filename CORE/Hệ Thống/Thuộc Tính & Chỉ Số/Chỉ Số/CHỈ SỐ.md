# CHỈ SỐ

> [!WARNING] IN DESIGN
> Hệ thống Chỉ Số **chưa freeze**. Nội dung dưới đây được giữ nguyên từ bản thiết kế cũ để làm nguyên liệu cho giai đoạn thiết kế Chỉ Số sau khi Thuộc Tính hoàn tất.

> [!NOTE]- **Hệ Thống Chỉ Số** 
> 
> > [!example]- **1. Chỉ Số Cơ Sở**
> > | Chỉ Số | Đơn Vị | Ý Nghĩa |
> > | :--- | :---: | :--- |
> > | **Sinh Lực (HP)** | Điểm | Về 0 là chết. |
> > | **Pháp Lực (MP)** | Điểm | Năng lượng để dùng ma pháp. |
> > | **Đấu Khí (Qi)** | Điểm |Năng lượng để dùng võ kỹ. |
> > | **Tấn Công Vật Lý** | Điểm | Độ mạnh đòn đánh thường/vũ khí/võ kỹ. |
> > | **Tấn Công Pháp Thuật** | Điểm | Độ mạnh pháp thuật. |
> > | **Giáp** | Điểm | Giảm sát thương vật lý nhận vào. |
> > | **Kháng Phép** | Điểm | Giảm sát thương phép nhận vào. |
> > | **Hồi Sinh Lực** | Điểm/s | Tốc độ hồi sinh lực khi không nhận sát thương. |
> > | **Hồi Pháp Lực** | Điểm/s | Tốc độ hồi pháp lực tự nhiên. |
> > | **Hồi Đấu Khí** | Điểm/s | Tốc độ hồi đấu khí tự nhiên. |
> > | **Tốc Độ Đánh** | Đòn/s | Số lần ra đòn đánh thường/vũ khí trên 1 giây. |
> > | **Tốc Độ Di Chuyển** | m/s | Tốc độ đi lại. |
> > | **Thể Lực** | Điểm | Năng lượng thể chất bị tiêu hao khi chạy, sử dụng kỹ năng,.... |
> > | **Hồi Thể Lực** | Điểm/s | Tốc độ hồi thể lực tự nhiên. |
> > | **Tinh Lực** | Điểm | Năng lượng tinh thần bị tiêu hao khi tập trung để sử dụng kỹ năng. |
> > | **Hồi Tinh Lực** | Điểm/s | Tốc độ hồi tinh lực tự nhiên. |
> > | **Tải Trọng** | Kg | Khối lượng vật phẩm tối đa có thể mang theo. |
> 
> > [!example]- **2. Chỉ Số Trung Cấp**
> > | Chỉ Số | Đơn Vị | Ý Nghĩa |
> > | :--- | :---: | :--- |
> > | **Chính Xác** | % | Tỉ lệ đánh trúng mục tiêu. |
> > | **Né Tránh** | % | Tỉ lệ né đòn đánh, kỹ năng. |
> > | **Tỷ Lệ Chí Mạng** | % | Tỷ lệ xuất hiện đòn đánh gây nhiều sát thương hơn. |
> > | **Sát Thương Chí Mạng** | % | Phần trăm sát thương tăng thêm khi gây chí mạng. |
> > | **Tỷ Lệ Nhược Điểm** | % | Phần trăm phóng đại nhược điểm trên người mục tiêu. |
> > | **Sát Thương Nhược Điểm** | % | Phần trăm sát thương khi đánh trúng nhược điểm. |
> > | **Tỷ Lệ Đón Đỡ** | % | Tỷ lệ đón đỡ đòn chí mạng, nhược điểm. |
> > | **Phá Giáp** | Điểm | Lượng giáp bị bỏ qua khi gây sát thương. | 
> > | **Xuyên Giáp** | % | Phần trăm giáp bị bỏ qua khi gây sát thương. |
> > | **Phá Kháng Phép** | Điểm | Lượng kháng phép bị bỏ qua khi gây sát thương. |
> > | **Xuyên Kháng Phép** | % | Phần trăm kháng phép bị bỏ qua khi gây sát thương. |
> > | **Giảm hồi chiêu** | % | Phần trăm thời gian chờ bị giảm khi hồi kỹ năng. |
> > | **Tốc Độ Thi Pháp** | % | Phần trăm thời gian niệm chú bị bỏ qua khi sử dụng kỹ năng. |
> > | **Hồi Phục Sinh Lực** | %/s | Tốc độ hồi sinh lực theo phần trăm. |
> > | **Hồi Phục Pháp Lực** | %/s | Tốc độ hồi pháp lực theo phần trăm. |
> > | **Hồi Phục Đấu Khí** | %/s | Tốc độ hồi đấu khí theo phần trăm. |
> > | **Hồi Phục Thể Lực** | %/s | Tốc độ hồi thể lực theo phần trăm. |
> > | **Hồi Phục Tinh Lực** | %/s | Tốc độ hồi tinh lực theo phần trăm. |
> > | **Hút Máu** | % | Hồi máu dựa trên lượng sát thương đòn đánh thường gây ra. |
> > | **Hút Máu Kỹ Năng** | % | Hồi máu dựa trên lượng sát thương kỹ năng gây ra. |
> > | **Giảm Thời Gian Khống Chế** | Giây | Giảm thời gian bị khống chế. |
> > | **Giảm Cường Độ Khống Chế** | Cấp | Giảm cường độ khống chế. |
> > | **Sát Thương Nguyên Tố** | Điểm, % | Tăng lượng sát thương nguyên tố (Chủ động). |
> > | **Giảm Sát Thương Nguyên Tố** | Điểm | Giảm lượng sát thương do nguyên tố gây ra. |
> > | **Nguyên Tố Kháng Tính** | % | Giảm phần trăm sát thương nhận vào do nguyên tố gây ra. |
> > | **Vật Lý Kháng Tính** | % | Giảm phần trăm sát thương vật lý nhận vào. |
> > | **Pháp Thuật Kháng Tính** | % | Giảm phần trăm sát thương pháp thuật nhận vào. |
> > | **Cận Chiến Tổn Thương** | Điểm, % | Tăng sát thương cận chiến bản thân gây ra. |
> > | **Viễn Trình Tổn Thương** | Điểm, % | Tăng sát thương tầm xa bản thân gây ra. |
> > | **Giảm/Kháng Sát Thương Cận Chiến** | Điểm, % | Giảm sát thương cận chiến nhận vào. |
> > | **Giảm/Kháng Sát Thương Viễn Trình** | Điểm, % | Giảm sát thương tầm xa nhận vào. |
> 
> > [!example]- **3. Chỉ Số Thượng Cấp**
> > | Chỉ Số | Đơn Vị | Ý Nghĩa |
> > | :--- | :---: | :--- |
> > | **Hút Máu Toàn Phần** | % | Hồi máu dựa trên tất cả lượng sát thương gây ra. |
> > | **Kháng Thời Gian Khống Chế** | %giây | Phần trăm thời gian khống chế bị giảm. |
> > | **Kháng Cường Độ Khống Chế** | %cấp | Phần trăm cường độ khống chế bị giảm. |
> > | **Kháng Khống Chế** | % | Phần trăm thời gian, cường độ khống chế bị giảm. |
> > | **Thời Gian Debuff** | Giây, %giây | Tăng thời gian mục tiêu bị khống chế do bản thân gây ra. |
> > | **Cường Độ Debuff** | Cấp, %cấp | Tăng cường độ khống chế do bản thân gây ra. |
> > | **Giảm/Kháng Thời Gian Debuff** | Giây, %giây | Giảm thời gian bị khống chế. |
> > | **Giảm/Kháng Cường Độ Debuff** | Cấp, %cấp | Giảm cường độ khống chế. |
> > | **Cố Phòng** | Điểm | Lượng tất cả sát thương (Trừ sát thương chuẩn) nhận vào bị giảm. |
> > | **Giảm Tổn Thương** | % | Phần trăm tất cả sát thương (Trừ sát thương chuẩn) nhận vào bị giảm. |
> > | **Phòng Ngự Tuyệt Đối** | Điểm, % | Giảm tất cả sát thương kể cả sát thương chuẩn nhận vào. |
> > | **Thụ Thương Cực Hạn** | % | Lượng sát thương tối đa nhận vào mỗi lần bị gây sát thương. |
> > | **Thụ Kích Hồi Phục** | Điểm, % | Lượng máu hồi phục khi nhận sát thương. |
> > | **Sát Thương Chuẩn** | Điểm, % | Lượng sát thương bỏ qua tất cả phòng ngự, trừ Phòng Ngự Tuyệt Đối do bản thân gây ra. |
> > | **Nhục Thể Tổn Thương** | Điểm, % | Sát thương bỏ qua chỉ số phòng ngự Cơ Sở, Trung Cấp, ăn mòn đấu khí, thể lực do bản thân gây ra. |
> > | **Linh Hồn Tổn Thương** | Điểm, % | Sát thương bỏ qua chỉ số phòng ngự Cơ Sở, Trung Cấp, ăn mòn pháp lực, tinh lực do bản thân gây ra. |
> > | **Giảm/Kháng Nhục Thể Tổn Thương** | Điểm, % | Giảm nhục thể sát thương, giảm độ ăn mòn đấu khí, thể lực nhận vào. |
> > | **Giảm/Kháng Linh Hồn Tổn Thương** | Điểm, % | Giảm linh hồn sát thương, giảm độ ăn mòn pháp lực, tinh lực nhận vào. |
> > | **Tầm Đánh** | m, % | Tầm đánh thường/vũ khí. |
> > | **Tầm Kỹ Năng** | m, % | Tầm thi triển kỹ năng. |
> > | **Phạm Vi Ảnh Hưởng** | m, % | Tăng diện tích đòn đánh, kỹ năng. |
