# Demo Project - Workflow Hàng Ngày

## Checklist Git

# 1️⃣ Cập nhật dự án từ main
git checkout main
git pull origin main

# 2️⃣ Tạo nhánh mới cho công việc hôm nay
git checkout -b <tên-nhánh-mới>
# Ví dụ:
# git checkout -b feature-login
# git checkout -b fix-navbar-bug

# 3️⃣ Làm việc và commit
git add .
git commit -m "Mô tả thay đổi chi tiết"

# 4️⃣ Cập nhật nhánh main trước khi push/merge
git checkout main
git pull origin main
git checkout <tên-nhánh>
git merge main    # hoặc git rebase main

# 5️⃣ Push nhánh làm việc lên remote
git push origin <tên-nhánh>

# 6️⃣ Merge nhánh vào main khi hoàn tất
git checkout main
git merge <tên-nhánh>
# Nếu có conflict, chỉnh sửa file, git add <file>, git commit
git push origin main

# 7️⃣ Dọn dẹp nhánh dư sau merge
git branch -d <tên-nhánh>           # xóa local
git push origin --delete <tên-nhánh> # xóa remote
