# Ideaverse

Obsidian vault dùng để xây dựng canon, hệ thống sức mạnh, worldbuilding, cốt truyện và database thực thể cho **Ideaverse**.

## Kiến trúc

- `CORE/`: canon hiện tại của truyện.
- `CORE/Hệ Thống/`: luật, cơ chế, phân cấp và ontology chung.
- `CORE/Danh Mục/`: database các thực thể cụ thể như kỹ năng, công pháp, trang bị, huyết mạch...
- `CORE/Nhân Vật/`: hồ sơ nhân vật tập trung, không nhân đôi theo nơi cư trú.
- `CORE/Lãnh Địa/`: subsystem độc quyền của nhân vật chính; giữ ở cấp `CORE/` vì quy mô lớn để tránh cây thư mục quá sâu.
- `CORE/Thế Giới/Phó Bản/`: các thế giới nguyên tác mà MC thực sự tiến vào.
- `IDEAS/`: ý tưởng chưa canon.
- `REFERENCE/`: tư liệu tham khảo, không phải canon.
- `SANDBOX/`: thử nghiệm, nội dung AI hoặc bản nháp chưa được duyệt.
- `TEMPLATES/`: template dùng để tạo note mới; không phải canon.

## Quy ước dữ liệu

Một khái niệm chỉ có **một nguồn sự thật chính**:

- Rule đặt ở `Hệ Thống/`.
- Instance cụ thể đặt ở `Danh Mục/`.
- Hồ sơ nhân vật chỉ mô tả nhân vật và liên kết tới các instance mà nhân vật sở hữu.
- Nhân vật thuộc phó bản vẫn có hồ sơ trong `Nhân Vật/`; note phó bản và Lãnh Địa liên kết tới hồ sơ đó thay vì tạo bản sao.
- Hai nhân vật khác nhau có thể trùng tên; khi đó phải giữ thành hai note riêng và dùng **path-qualified wikilink** để tránh liên kết mơ hồ. Không gộp nhân vật chỉ vì trùng tên.

## Git

Repository nên để **Private** trong giai đoạn sáng tác. File trạng thái workspace cục bộ của Obsidian được bỏ qua bằng `.gitignore`, còn phần cấu hình ổn định trong `.obsidian/` có thể được version-control.
