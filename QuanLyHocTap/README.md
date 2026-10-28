# Quản lý học tập cá nhân — Bản E

Ứng dụng quản lý học tập cá nhân dùng Python và Streamlit. Thư mục này là dự án độc lập trong repository OpenClaw; các tệp OpenClaw ở thư mục gốc được giữ nguyên.

## Chạy trên Windows

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r requirements.txt
Copy-Item .env.example .env
py -m streamlit run hoctap.py
```

Mở địa chỉ localhost được in ra trong Terminal.

## Cấu hình AI (tùy chọn)
Chỉnh `.env` trên máy cá nhân. Không đưa API key, token Gateway, `.env` hoặc dữ liệu cá nhân lên GitHub. Xem `.env.example` để biết các biến cấu hình mẫu.

Lưu ý: đặt mã nguồn ứng dụng và các tệp cần thiết trong thư mục này cùng với README.