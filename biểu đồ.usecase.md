# Prompt nhờ AI tạo sơ đồ Use Case
Hãy tạo mã Mermaid code cho sơ đồ Use Case của hệ thống Quản lý Thư viện.

# Code Mermaid
```mermaid
graph TD
    SinhVien([Sinh vien / Doc gia])
    ThuThu([Thu thu / Quan tri])

    subgraph HeThongQuanLyThuVien [He thong Quan ly Thu vien]
        UC1(Dang nhap / Dang xuat)
        UC2(Tim kiem sach)
        UC3(Muon sach)
        UC4(Tra sach)
        UC5(Quan ly danh muc sach)
        UC6(Quan ly doc gia)
        UC7(Thong ke bao cao)
    end

    SinhVien --> UC1
    SinhVien --> UC2
    SinhVien --> UC3
    SinhVien --> UC4

    ThuThu --> UC1
    ThuThu --> UC2
    ThuThu --> UC5
    ThuThu --> UC6
    ThuThu --> UC7