Hướng dẫn tạo Google Sheets Credential trong n8n

A. Tạo Project trong Google Cloud Console
1. Truy cập: console.cloud.google.com
2. Tạo Project mới "N8N Automation"
3. Kích hoạt API:
   - Google Sheets API: console.cloud.google.com/apis/library/sheets.googleapis.com
   - Google Drive API: console.cloud.google.com/apis/library/drive.googleapis.com

B. Cấu hình OAuth Consent Screen
1. Vào: console.cloud.google.com/apis/credentials/consent
2. Chọn User Type: External
3. Điền thông tin:
   - App name: N8N Automation
   - User support email: email của bạn
   - Developer contact email: email của bạn
4. Thêm Test Users: email của bạn

C. Tạo OAuth 2.0 Client ID
1. Vào: console.cloud.google.com/apis/credentials
2. Click "Create Credentials" → OAuth client ID
3. Application type: Web application
4. Thêm Authorized redirect URI:
   - Local: https://localhost:5678/rest/oauth2-credential/callback
   - Hosting: https://your-domain.com/rest/oauth2-credential/callback
5. Click Create → Lưu Client ID và Client Secret

D. Cấu hình trong n8n
1. Tạo Credential mới:
   - Type: OAuth2
   - Generic OAuth2 API
   - Điền Client ID và Client Secret
2. Click "Sign in with Google"
3. Chọn tài khoản và cấp quyền
4. Xác nhận kết nối thành công

Lưu ý quan trọng:
✓ Email phải có trong Test Users
✓ URI không có khoảng trắng
✓ Cấp đủ quyền khi được yêu cầu
✓ URI phải khớp với domain n8n