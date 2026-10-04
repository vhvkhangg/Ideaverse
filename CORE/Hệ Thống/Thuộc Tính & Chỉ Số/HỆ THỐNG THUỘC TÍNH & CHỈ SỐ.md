# HỆ THỐNG THUỘC TÍNH & CHỈ SỐ

> [!ABSTRACT] Source of Truth Map
> Đây là **bản đồ tổng** của subsystem Thuộc Tính & Chỉ Số. Quy tắc chi tiết nằm tại note source of truth tương ứng. Bản đồ hệ thống cấp cao hơn: [[HỆ THỐNG THIẾT LẬP]].

## Thuộc Tính

- [[THUỘC TÍNH]] — source of truth **FROZEN v1** cho Hệ Thống Thuộc Tính.
- **Cơ Bản:** [[Sức Mạnh]], [[Thể Chất]], [[Nhanh Nhẹn]], [[Tinh Thần]].
- **Đặc Biệt:** [[Ngộ Tính]], [[Mị Lực]], [[Vận Khí]].
- Decision log: [[HỆ THỐNG THUỘC TÍNH v1]].

## Chỉ Số

- [[CHỈ SỐ]] — source of truth **FROZEN v1** cho Hệ Thống Chỉ Số.
- [[CHỈ SỐ CƠ SỞ]] — các đại lượng nền tảng.
- [[CHỈ SỐ TRUNG CẤP]] — các đại lượng chuyên biệt và modifier chiến đấu.
- [[CHỈ SỐ THƯỢNG CẤP]] — các đại lượng hiếm/can thiệp layer sâu.
- Decision log: [[HỆ THỐNG CHỈ SỐ v1]].

## Tài Nguyên

- [[TÀI NGUYÊN]] — source of truth **FROZEN v1** cho trạng thái `hiện tại / tối đa`, Năng Lượng, Phẩm Chất, Độ Tinh Khiết và ngưỡng suy giảm.
- Chỉ Số sở hữu `<Tài Nguyên> Tối Đa`, hồi phục và modifier liên quan; Giá Trị Hiện Tại thuộc Hệ Thống Tài Nguyên.
- Decision log: [[HỆ THỐNG TÀI NGUYÊN v1]].

## Ranh Giới Hệ Thống

```text
Thuộc Tính
→ thông qua Hệ Số Chuyển Đổi của build/subsystem
→ Chỉ Số / giới hạn Tài Nguyên
→ Tài Nguyên quản lý giá trị hiện tại
```

Không có bảng conversion toàn cục cố định từ Thuộc Tính sang Chỉ Số.

---

> [!NOTE] Quy tắc kiến trúc
> File này chỉ đóng vai trò bản đồ. Không lặp lại định nghĩa chi tiết của Thuộc Tính, Chỉ Số hoặc Tài Nguyên tại đây.
