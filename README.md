# Bài 1 : Loại bỏ rủi ro lưu trữ cục bộ trong dự án nhóm

## Phần 1: Phân tích hậu quả của "Thảm họa dữ liệu truyền thống"
1. **Mất dữ liệu vĩnh viễn:** Thao tác nhấn `Ctrl+S` sau khi lỡ tay xóa code làm mất dữ liệu vĩnh viễn do không có cơ chế lưu vết trên máy cục bộ.
2. **Xung đột phiên bản (Version Chaos):** Việc đặt tên file thủ công (`v1`, `v2_final`) và trao đổi qua Zalo gây nhầm lẫn phiên bản và khó khăn khi ghép nối code.
3. **Phụ thuộc phần cứng (Single Point of Failure):** Dữ liệu chỉ nằm trên máy cá nhân, rủi ro mất trắng toàn bộ thành quả nếu máy tính hỏng hóc hoặc mất nguồn.

## Phần 2: Quy trình Hybrid Workflow & Khôi phục bằng Version History
1. **Đồng bộ tự động (Delta Sync):** Đặt thư mục dự án vào Google Drive/OneDrive để hệ thống tự động đồng bộ ngầm lên đám mây theo thời gian thực trong khi vẫn viết code trên máy cục bộ.
2. **Khôi phục qua Version History:** Khi xảy ra sự cố ghi đè, chỉ cần truy cập giao diện đám mây, chọn **Version History** và nhấn **Restore** để lấy lại code cũ trong 1 cú click.
3. **Quản lý mã nguồn chuẩn hóa:** Thay thế việc gửi file qua Zalo bằng Git & GitHub để quản lý lịch sử thay đổi (`commit`, `push`) minh bạch và an toàn tuyệt đối.
