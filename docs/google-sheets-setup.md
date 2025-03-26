# Hướng dẫn tạo Google Sheets Credential trong n8n

A. Tạo Project trong Google Cloud Console
1. Truy cập [Google Cloud Console](https://console.cloud.google.com)
2. Tạo Project mới có tên "N8N Automation"
3. Kích hoạt 2 API cần thiết:
   - [Google Sheets API](https://console.cloud.google.com/apis/library/sheets.googleapis.com)
   - [Google Drive API](https://console.cloud.google.com/apis/library/drive.googleapis.com)

B. Cấu hình OAuth Consent Screen
1. Vào [OAuth consent screen](https://console.cloud.google.com/apis/credentials/consent)
2. Chọn User Type là External
3. Điền thông tin ứng dụng:
   - App name: N8N Automation
   - User support email: email của bạn
   - Developer contact email: email của bạn
4. Thêm Test Users bằng cách click Add Users và thêm email của bạn

C. Tạo OAuth 2.0 Client ID
1. Vào mục [Credentials](https://console.cloud.google.com/apis/credentials)
2. Click Create Credentials, chọn OAuth client ID
3. Chọn Application type là Web application
4. Thêm Authorized redirect URI. Ví dụ:
   - Nếu chạy local: https://localhost:5678/rest/oauth2-credential/callback
   - Nếu dùng hosting: https://your-domain.com/rest/oauth2-credential/callback
5. Click Create để nhận Client ID và Client Secret

D. Cấu hình trong n8n
1. Tạo Credential mới:
   - Chọn Type: OAuth2
   - Chọn Generic OAuth2 API
   - Điền Client ID và Client Secret vừa tạo
2. Click nút "Sign in with Google"
3. Chọn tài khoản Google và cấp quyền truy cập
4. Xác nhận kết nối thành công

Lưu ý quan trọng:
- Email của bạn phải được thêm vào Test Users
- URI phải chính xác, không có khoảng trắng
- Cấp đủ quyền khi Google yêu cầu xác thực
- URI phải trùng khớp với domain n8n bạn đang sử dụng