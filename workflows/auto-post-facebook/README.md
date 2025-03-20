# 🤖 Tự động đăng bài Facebook từ Google Sheets

## Tổng quan Workflow
![Workflow Overview](./images/workflow-overview.png)

<div align="center">
  <a href="./images/workflow-detail.png" target="_blank">
    <button style="
      background-color: #4a5568;
      color: white;
      padding: 12px 24px;
      border: none;
      border-radius: 4px;
      font-size: 16px;
      cursor: pointer;
      margin: 20px 0;
    ">
      👀 Xem chi tiết Workflow
    </button>
  </a>
</div>

## 📝 Mô tả
Workflow này tự động hóa việc đăng bài lên Facebook từ dữ liệu trong Google Sheets. Workflow bao gồm các bước:

1. **Schedule Trigger**: Lập lịch chạy tự động
2. **Google Sheets**: Đọc dữ liệu từ sheet
3. **Function**: Xử lý và định dạng dữ liệu
4. **IF**: Kiểm tra điều kiện đăng bài
5. **Facebook**: Đăng bài lên Facebook
6. **Update Sheet**: Cập nhật trạng thái đã đăng

## 🚀 Sử dụng Workflow

<div align="center">
  <button id="copyButton" onclick="copyWorkflow()" style="
    background-color: #37b24d;
    color: white;
    padding: 12px 24px;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
    margin: 20px 0;
  ">
    📋 Copy Workflow
  </button>
</div>

<script>
async function copyWorkflow() {
  try {
    const response = await fetch('workflow.json');
    const json = await response.text();
    await navigator.clipboard.writeText(json);
    
    const button = document.getElementById('copyButton');
    button.textContent = '✅ Đã copy!';
    button.style.backgroundColor = '#2f9e44';
    
    setTimeout(() => {
      button.textContent = '📋 Copy Workflow';
      button.style.backgroundColor = '#37b24d';
    }, 2000);
  } catch (err) {
    console.error('Failed to copy:', err);
  }
}
</script>

## 👤 Tác giả
**Hải Quang**
- 📧 Email: haiquangbh1a1b1c@gmail.com
- 🌐 GitHub: [@insightfreedom247](https://github.com/insightfreedom247)

## 📄 Giấy phép
MIT License - Xem file [LICENSE](../../LICENSE) để biết thêm chi tiết