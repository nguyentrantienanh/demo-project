<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Demo Project - Git Workflow Hàng Ngày</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      color: #333;
      line-height: 1.6;
      padding: 20px;
    }
    h1 {
      color: #007acc;
      text-align: center;
    }
    h2 {
      color: #007acc;
      margin-top: 30px;
    }
    pre {
      background: #eee;
      padding: 10px;
      border-left: 4px solid #007acc;
      overflow-x: auto;
      border-radius: 5px;
    }
    .step {
      background: #fff;
      padding: 15px 20px;
      margin: 15px 0;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    .step-number {
      font-weight: bold;
      color: #fff;
      background: #007acc;
      padding: 5px 10px;
      border-radius: 50%;
      display: inline-block;
      margin-right: 10px;
    }
  </style>
</head>
<body>

  <h1>Demo Project - Git Workflow Hàng Ngày</h1>

  <div class="step">
    <span class="step-number">1</span>
    <strong>Cập nhật nhánh gốc (frontend / backend / data)</strong>
    <pre>
git checkout &lt;frontend|backend|data&gt;
git pull origin &lt;frontend|backend|data&gt;
    </pre>
  </div>

  <div class="step">
    <span class="step-number">2</span>
    <strong>Tạo nhánh mới cho công việc hôm nay</strong>
    <pre>
git checkout -b &lt;tên-nhánh-mới&gt;

# Ví dụ:
# git checkout frontend
# git checkout -b feature/frontend-login
    </pre>
  </div>

  <div class="step">
    <span class="step-number">3</span>
    <strong>Làm việc và commit</strong>
    <pre>
git add .
git commit -m "Mô tả thay đổi chi tiết"
    </pre>
  </div>

  <div class="step">
    <span class="step-number">4</span>
    <strong>Cập nhật nhánh gốc trước khi push/merge</strong>
    <pre>
git checkout &lt;frontend|backend|data&gt;
git pull origin &lt;frontend|backend|data&gt;
git checkout &lt;tên-nhánh-mới&gt;
git merge &lt;frontend|backend|data&gt;
# Hoặc git rebase &lt;frontend|backend|data&gt;
    </pre>
  </div>

  <div class="step">
    <span class="step-number">5</span>
    <strong>Push nhánh làm việc lên remote</strong>
    <pre>
git push origin &lt;tên-nhánh-mới&gt;
    </pre>
  </div>

  <div class="step">
    <span class="step-number">6</span>
    <strong>Merge nhánh làm việc vào nhánh gốc khi hoàn tất</strong>
    <pre>
git checkout &lt;frontend|backend|data&gt;
git merge &lt;tên-nhánh-mới&gt;
git push origin &lt;frontend|backend|data&gt;
    </pre>
  </div>

  <div class="step">
    <span class="step-number">7</span>
    <strong>Dọn dẹp nhánh dư sau merge</strong>
    <pre>
git branch -d &lt;tên-nhánh-mới&gt;           # xóa local
git push origin --delete &lt;tên-nhánh-mới&gt; # xóa remote
    </pre>
  </div>

</body>
</html>
