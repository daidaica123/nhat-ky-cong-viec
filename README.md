# Nhật ký công việc — bản Cloudflare Pages

Trang tĩnh theo dõi giờ làm hằng ngày: tổng quan cả kỳ, từng ngày, theo mảng và theo task.

- Mã nguồn dựng trang nằm ở máy: `D:\Nhat ky cong viec\_build\` (không đưa lên repo).
- Dữ liệu lấy từ file Excel `Nhat ky cong viec_v2.xlsx`. Trang chỉ chứa khung giờ và tên task,
  không chứa nội dung chi tiết từng việc.

## Cập nhật mỗi ngày

1. Thêm ngày mới vào file Excel.
2. `python _build\build_html.py` để dựng lại `public\index.html`.
3. `python _build\deploy.py` để đẩy lên repo. Cloudflare tự phát hành sau vài chục giây.

## Cloudflare Pages

Create → Connect to Git → chọn repo này. Build command để trống, Build output directory là `public`.

Trang công khai với người có link. `robots.txt` và thẻ `noindex` chặn công cụ tìm kiếm.
Muốn chặn hẳn thì bật Cloudflare Access.
