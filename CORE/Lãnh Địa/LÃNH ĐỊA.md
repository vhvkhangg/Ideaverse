## 1. Cơ Chế Vận Hành

> [!calculator]- Quy Tắc
>  ![[HỆ THỐNG THIẾT LẬP#3. 🏰 LÃNH ĐỊA]]

## 2. Quản Lý Lãnh Địa

```mermaid
graph LR
    %% --- KHAI BÁO NODE ---
    Root("🏰 Lãnh Địa")

    %% Nhóm
    %% Cơ Cấu Lãnh Địa
    
    
    %% Công Trình Kiến Trúc
    CongTrinhKienTruc("Công Trình\nKiến Trúc")
	    BanMenh("🔮 Bản Mệnh")
		    LinhChuChiTam("💠 Lĩnh Chủ Chi Tâm")
	    HachTam("🏛️ Hạch Tâm")
		    AnhHungDien("⚔️ Anh Hùng Điện")
		    QuanTinhHocVien("📜 Quần Tinh Học Viện")
		    AnhLinhDien("Anh Linh Điện")
		    CanKhonGioiVuc("Càn Khôn Giới Vực")
	    ChienTranh("🏯 Chiến Tranh")
		    KetGioi("Kết Giới")
		    BinhDoanh("⛺ Binh Doanh")
		    TuongThanh("🧱 Tường Thành")
		    ThapPhongVe("🗼 Tháp Phòng Vệ")
	    SanXuat("🌾 Sản Xuất")
		    LinhDien("🌿 Linh Điền")
		    LinhTuyen("Linh Tuyền")
		    
    
    %% Quân Đội
    QuanDoi("Quân Đội")
	    QuanDoan("Quân Đoàn")
    
    %% Anh Hùng
    AnhHung("Anh Hùng")
	    ShalltearBloodfallen("Shalltear Bloodfallen")
	    Sebastian("Sebastian")
	    KhongHiDuyet("Khổng Hi Duyệt")   

    %% --- KẾT NỐI ---
    Root --> BanMenh
    Root --> HachTam
    Root --> ChienTranh
    Root --> SanXuat

    BanMenh --> LCTC
    HachTam --> AHD & QTHV
    ChienTranh --> BD & TT & TPV
    SanXuat --> LD

    %% --- ĐỊNH NGHĨA MÀU SẮC (STYLES) ---
    %% Root: Hồng, chữ đen, viền đậm
    classDef rootStyle fill:#bbf,stroke:#333,stroke-width:4px,color:#000;
    
    %% Category: Xanh nhạt, chữ đen
    classDef catStyle fill:#bbb,stroke:#333,stroke-width:2px,color:#000;
    
    %% Item: Trắng, chữ đen (QUAN TRỌNG: fill:#fff)
    classDef itemStyle fill:#fff,stroke:#333,stroke-width:1px,color:#000;

    %% --- ÁP DỤNG CLASS (QUAN TRỌNG NHẤT) ---
    
    %% 1. Áp dụng cho Root (Vừa là Root style, vừa là Link)
    class Root rootStyle;

    %% 2. Áp dụng cho Nhóm (Chỉ tô màu, không cần link nên không có internal-link)
    class BanMenh,HachTam,ChienTranh,SanXuat catStyle;

    %% 3. Áp dụng cho Item (Vừa là Item style, vừa là Link)
    %% Cú pháp: class [TênNode] [TênClass1],[TênClass2];
    class LCTC,AHD,QTHV,BD,TT,TPV,LD internal-link,itemStyle;
```

## 3. Cấu Trúc Không Gian
> [!info] **Mô Hình: Thập Trùng Thiên**
> Lãnh địa không mở rộng trên một mặt phẳng, mà xếp chồng lên nhau thành tháp không gian.
>
> **Tầng 10: Vĩnh Hằng Thần Đô**
> - **Chủ nhân:** Nơi ở của Lãnh Chúa & Gia quyến.
> - **Kiến trúc:** Một tòa Tiên Cung lơ lửng, xung quanh là biển mây và các vì sao nhân tạo.
> - **Đặc quyền:** Nồng độ năng lượng gấp 10000 lần các tầng Bát Hoang Tinh Vực.
>
> **Tầng 2 ➔ 9: Bát Hoang Tinh Vực**
> - **Cấu trúc:** 8 Lục địa khổng lồ bay xung quanh trục chính (Thần Đô) với tâm là các tinh cầu, mô phỏng quỹ đạo hành tinh.
> - **Chức năng:** Khu vực của Tướng lĩnh, Quân đội tinh nhuệ,  Các chủng tộc cao cấp.
> - - **Đặc quyền:** Nồng độ năng lượng gấp 1000 lần tầng Khởi Nguyên Đại Lục.
>
> **Tầng 1: Khởi Nguyên Đại Lục**
> - **Cấu trúc:** Một siêu lục địa trải dài vô tận làm nền móng.
> - **Chức năng:** Nơi sinh sống của hàng tỷ dân thường, sản xuất nông nghiệp, khai thác tài nguyên cơ bản.