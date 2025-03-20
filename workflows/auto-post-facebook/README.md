# 🤖 Tự động đăng bài lên Facebook từ Google Sheets

![Workflow Preview](./images/workflow-preview.png)

## 📝 Mô tả
Workflow này tự động hóa quy trình đăng bài lên Facebook Fanpage từ dữ liệu trong Google Sheets. Workflow sẽ:
- Đọc nội dung từ Google Sheets
- Kiểm tra các bài viết chưa đăng
- Tự động đăng lên Facebook Fanpage
- Cập nhật trạng thái trong sheets

## ⚙️ Các bước thực hiện

### 1. Schedule Trigger
- Tự động chạy mỗi ngày vào 9:00 sáng
- Múi giờ: Asia/Ho_Chi_Minh

### 2. Google Sheets
- Đọc dữ liệu từ sheet được chỉ định
- Cấu trúc cột:
  - A: Tiêu đề bài viết
  - B: Nội dung chi tiết
  - C: URL hình ảnh
  - D: Trạng thái đăng

### 3. Function
- Xử lý và định dạng nội dung
- Kết hợp tiêu đề và nội dung
- Chuẩn bị dữ liệu cho Facebook

### 4. IF
- Kiểm tra trạng thái "Chưa đăng"
- Chỉ xử lý các bài viết mới

### 5. Facebook
- Tự động đăng bài lên Fanpage
- Đính kèm hình ảnh từ URL
- Định dạng nội dung đẹp mắt

### 6. Update Sheet
- Cập nhật trạng thái thành "Đã đăng"
- Theo dõi tiến trình đăng bài

## 🚀 Cách sử dụng

1. Click nút "Use Workflow" bên dưới
2. Import workflow vào n8n của bạn
3. Cấu hình:
   - Google Sheets credentials
   - Facebook Page Access Token
   - Sheet ID và Page ID
4. Kích hoạt workflow và tận hưởng!

## 📋 Yêu cầu
- n8n instance
- Google Sheets API access
- Facebook Page Access Token
- Google Sheet theo mẫu

## 🔗 Liên kết
- [Workflow JSON](./workflow.json)
- [Hướng dẫn chi tiết](./docs/setup.md)
- [Mẫu Google Sheet](./templates/sheet-template.xlsx)

## 👨‍💻 Tác giả
- Created by: insightfreedom247
- GitHub: [@insightfreedom247](https://github.com/insightfreedom247)

## 📄 Giấy phép
MIT License - Tự do sử dụng và chỉnh sửa

<div align="center">
  <a href="https://raw.githubusercontent.com/insightfreedom247/auto-content-workflows/main/workflows/auto-post-facebook/workflow.json" style="display: inline-block; padding: 10px 20px; background-color: #28a745; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">
    🔄 Use Workflow
  </a>
</div>