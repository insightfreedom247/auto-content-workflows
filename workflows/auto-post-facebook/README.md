# 📘 Tự động đăng bài Facebook từ Google Sheets

<div align="center">
  <img src="images/cover.png" width="800" alt="Workflow Overview"/>
  <br/><br/>
  <p>
    <a href="#🎯-tính-năng"><img src="https://img.shields.io/badge/Tính_năng-4-brightgreen?style=for-the-badge" alt="Features"/></a>
    <a href="#🔧-yêu-cầu"><img src="https://img.shields.io/badge/Yêu_cầu-3-orange?style=for-the-badge" alt="Requirements"/></a>
    <a href="#📝-hướng-dẫn"><img src="https://img.shields.io/badge/Hướng_dẫn-Chi_tiết-blue?style=for-the-badge" alt="Tutorial"/></a>
  </p>
</div>

## 🎯 Tính năng

- 📊 **Đọc dữ liệu từ Google Sheets**
  - Tự động đọc tiêu đề và nội dung từ sheet
  - Hỗ trợ lập lịch đăng bài
  - Theo dõi trạng thái đăng

- 🤖 **Tối ưu nội dung với AI**
  - Sử dụng GPT-4 để cải thiện nội dung
  - Tự động thêm hashtag phù hợp
  - Tối ưu độ dài và format

- 🎨 **Tạo hình ảnh với AI**
  - Sử dụng DALL-E để tạo hình ảnh
  - Tự động điều chỉnh kích thước
  - Tối ưu cho Facebook

- 📱 **Đăng bài tự động**
  - Đăng lên Facebook Fanpage
  - Hỗ trợ đăng hình ảnh
  - Theo dõi trạng thái

## 🔧 Yêu cầu

1. **Google Sheets API**
   - Tài khoản Google Cloud
   - API key và OAuth credentials
   - [Hướng dẫn cài đặt](docs/google-sheets-setup.md)

2. **OpenAI API**
   - API key từ OpenAI
   - Truy cập GPT-4 và DALL-E
   - [Hướng dẫn cài đặt](docs/openai-setup.md)

3. **Facebook Graph API**
   - Facebook Developer Account
   - Page Access Token
   - [Hướng dẫn cài đặt](docs/facebook-setup.md)

## 📝 Hướng dẫn

### 1. Chuẩn bị Google Sheet

- Tạo Google Sheet mới với các cột:
  - A: Tiêu đề
  - B: Nội dung gợi ý
  - C: Thời gian đăng
  - D: Trạng thái

### 2. Cài đặt Workflow

1. Copy file `workflow.json` vào n8n:
```json
{"name":"Auto Post Facebook","nodes":[...]}```

2. Cấu hình các credentials:
   - Google Sheets
   - OpenAI
   - Facebook

3. Cập nhật các biến môi trường:
```env
SHEET_ID=your_sheet_id
FB_PAGE_ID=your_page_id
```

### 3. Chạy thử

1. Thêm dữ liệu test vào Google Sheet
2. Kích hoạt workflow
3. Kiểm tra kết quả trên Facebook

## 📊 Theo dõi

- Cột D trong Google Sheet sẽ hiển thị trạng thái:
  - 🟡 Đang xử lý
  - 🟢 Đăng thành công
  - 🔴 Lỗi

## 🔍 Xử lý lỗi

- Kiểm tra logs trong n8n
- Xác nhận các credentials còn hạn
- [Danh sách lỗi thường gặp](docs/troubleshooting.md)

## 📈 Tối ưu

- Điều chỉnh prompt AI trong node OpenAI
- Thay đổi tần suất chạy workflow
- Thêm node xử lý lỗi

## 🤝 Đóng góp

Mọi đóng góp đều được chào đón! Hãy tạo pull request hoặc issue.