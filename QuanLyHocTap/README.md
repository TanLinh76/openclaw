<div align="center">

# 📚 QUẢN LÝ HỌC TẬP CÁ NHÂN

### ✨ Học tập có kế hoạch — Theo dõi tiến độ — Chinh phục mục tiêu

<p>
  <strong>Ứng dụng hỗ trợ quản lý hành trình học tập của bạn</strong><br>
  Xây dựng bằng Python và Streamlit, với trợ lý AI tùy chọn.
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Streamlit-App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
  <img src="https://img.shields.io/badge/AI-Optional-7C3AED?style=for-the-badge&logo=openai&logoColor=white" alt="AI tùy chọn">
  <img src="https://img.shields.io/badge/Language-Tiếng%20Việt-16A34A?style=for-the-badge" alt="Tiếng Việt">
</p>

</div>

---

## 🌟 Giới thiệu

**Quản lý học tập cá nhân – Bản E** là ứng dụng giúp người học tập trung các công việc học tập vào một nơi: theo dõi bài tập, quản lý thời hạn, xem thống kê tiến độ và sử dụng trợ lý học tập khi cần.

Mục tiêu của dự án là giúp việc học **rõ ràng hơn, chủ động hơn và dễ theo dõi hơn** thông qua giao diện trực quan.

> 🎯 **Thông điệp dự án:** Lập kế hoạch tốt hơn hôm nay để tiến bộ từng ngày.

## 🧭 Các chức năng chính

| 🧩 Phân hệ | 💡 Mục đích |
|---|---|
| 📘 Quản lý học tập | Tập trung thông tin và hoạt động học tập ở một nơi |
| ✅ Bài tập & hạn nộp | Theo dõi công việc, trạng thái và các thời hạn quan trọng |
| 🗓️ Lập kế hoạch | Hỗ trợ sắp xếp công việc theo mức độ ưu tiên |
| 📊 Thống kê tiến độ | Quan sát tình hình học tập để biết phần nào cần cải thiện |
| 🤖 Trợ lý AI (tùy chọn) | Hỗ trợ giải đáp và lập kế hoạch học tập khi đã cấu hình dịch vụ AI |
| 🔌 Tích hợp OpenClaw (tùy chọn) | Kết nối Gateway nếu môi trường của bạn đã được thiết lập |

## 🖥️ Công nghệ sử dụng

- **Python** — xử lý logic ứng dụng.
- **Streamlit** — xây dựng giao diện web.
- **Pandas** — hỗ trợ xử lý và trình bày dữ liệu.
- **OpenAI SDK / OpenClaw Gateway** — tùy chọn cho tính năng AI.
- **unittest** — kiểm thử các thành phần của ứng dụng.

## 🚀 Cài đặt và chạy trên Windows

### 1. Chuẩn bị môi trường

Cài đặt Python trước, sau đó mở Terminal tại thư mục dự án và chạy:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install --upgrade pip
py -m pip install -r requirements.txt
```

### 2. Cấu hình môi trường

Tạo tệp `.env` từ tệp mẫu:

```powershell
Copy-Item .env.example .env
```

Nếu không sử dụng AI, bạn có thể để trống các khóa AI và sử dụng những chức năng không phụ thuộc dịch vụ đó. Nếu bật AI, hãy mở `.env` và điền cấu hình phù hợp với dịch vụ của bạn.

### 3. Khởi chạy ứng dụng

```powershell
py -m streamlit run hoctap.py
```

Sau khi khởi chạy, mở địa chỉ cục bộ mà Streamlit hiển thị trong Terminal (thường là http://localhost:8501).

> 💡 Trên Windows, bạn cũng có thể dùng tệp `run_app.bat` nếu tệp này có trong thư mục dự án.

## 🧪 Kiểm thử

Chạy toàn bộ bộ kiểm thử bằng:

```powershell
py -m unittest -v test_data_store.py test_assistant.py test_openclaw_client.py test_planner.py test_statistics.py test_app_smoke.py
```

Hoặc dùng `run_tests.bat` / `run_tests.ps1` nếu có sẵn trong thư mục dự án.

## 🗂️ Cấu trúc dự án

```text
QuanLyHocTap/
├── hoctap.py                 # Ứng dụng Streamlit
├── data_store.py             # Lưu trữ và xử lý dữ liệu
├── assistant.py              # Trợ lý học tập
├── openclaw_client.py        # Kết nối OpenClaw (tùy chọn)
├── planner.py                # Hỗ trợ lập kế hoạch
├── statistics_view.py        # Thống kê học tập
├── test_*.py                 # Các bài kiểm thử
├── requirements.txt          # Thư viện cần cài đặt
├── .env.example              # Mẫu cấu hình môi trường
└── .gitignore                # Loại trừ tệp riêng tư và cache
```

## 🔐 Bảo mật & quyền riêng tư

- **Không tải tệp `.env` lên GitHub.**
- Không đưa API key, Gateway token, mật khẩu hoặc thông tin đăng nhập vào mã nguồn.
- Không commit dữ liệu học tập cá nhân hoặc tệp dữ liệu phát sinh trên máy của bạn.
- Chỉ bật tính năng AI khi bạn đã chủ động cấu hình dịch vụ cần thiết.
- Tệp `.env.example` chỉ dùng làm mẫu; hãy kiểm tra trước khi điền thông tin thật.

## 🛣️ Định hướng phát triển

- [x] Tổ chức ứng dụng thành các mô-đun Python.
- [x] Bổ sung bộ kiểm thử cho các thành phần chính.
- [ ] Tiếp tục cải thiện trải nghiệm giao diện và khả năng tiếp cận.
- [ ] Hoàn thiện hướng dẫn triển khai và kiểm tra tích hợp trên từng môi trường.

## 👨‍💻 Dành cho người phát triển

1. Sao chép repository về máy.
2. Tạo môi trường ảo và cài các thư viện trong `requirements.txt`.
3. Tạo `.env` từ `.env.example` nếu cần dùng AI.
4. Chạy ứng dụng và kiểm thử trước khi gửi thay đổi.

---

<div align="center">

### 💙 Cảm ơn bạn đã ghé thăm dự án!

*Học tập hiệu quả bắt đầu từ những bước nhỏ, được thực hiện đều đặn mỗi ngày.*

<sub>📌 Dự án Quản lý học tập cá nhân — nằm trong thư mục riêng của repository OpenClaw.</sub>

</div>
