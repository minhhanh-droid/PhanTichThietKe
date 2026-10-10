# Prompt nhờ AI tạo sơ đồ Activity
Hãy tạo mã Mermaid code cho sơ đồ Activity quy trình Mượn sách của hệ thống Quản lý Thư viện.

# Code Mermaid
```mermaid
stateDiagram-v2
    [*] --> NhapThongTin: Độc giả yêu cầu mượn sách
    NhapThongTin --> KiemTraThe: Thủ thư kiểm tra thẻ độc giả

    state KiemTraThe_Decision <<choice>>
    KiemTraThe --> KiemTraThe_Decision

    KiemTraThe_Decision --> TheKhongHopLe: Thẻ hết hạn / Vi phạm
    TheKhongHopLe --> TuChoi: Báo lỗi & Từ chối mượn
    TuChoi --> [*]

    KiemTraThe_Decision --> KiemTraSach: Thẻ hợp lệ
    KiemTraSach --> KiemTraSach_Decision: Kiểm tra tình trạng sách

    state KiemTraSach_Decision <<choice>>
    KiemTraSach_Decision --> HetSach: Sách đã được mượn hết
    HetSach --> TuChoi

    KiemTraSach_Decision --> TaoPhieuMuon: Sách có sẵn trong kho
    TaoPhieuMuon --> LuuCoSoDuLieu: Ghi nhận phiếu mượn vào hệ thống
    LuuCoSoDuLieu --> TraSachChoDocGia: Bàn giao sách cho độc giả
    TraSachChoDocGia --> [*]: Hoàn tất quy trình