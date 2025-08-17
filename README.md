# Demo Project - Git Workflow Hàng Ngày

Hướng dẫn các bước làm việc theo nhóm với Git, từ cập nhật nhánh gốc đến merge vào main.

---

## 1️⃣ Cập nhật nhánh gốc (frontend / backend / data)

```bash
git checkout <frontend|backend|data>
git pull origin <frontend|backend|data>
2️⃣ Tạo nhánh mới cho công việc hôm nay
bash
Copy
Edit
git checkout -b <tên-nhánh-mới>
# Ví dụ:
# git checkout frontend
# git checkout -b feature/frontend-login
3️⃣ Làm việc và commit
bash
Copy
Edit
git add .
git commit -m "Mô tả thay đổi chi tiết"
4️⃣ Cập nhật nhánh gốc trước khi push/merge
bash
Copy
Edit
git checkout <frontend|backend|data>
git pull origin <frontend|backend|data>
git checkout <tên-nhánh-mới>
git merge <frontend|backend|data>
# Hoặc sử dụng rebase:
# git rebase <frontend|backend|data>
5️⃣ Push nhánh làm việc lên remote
bash
Copy
Edit
git push origin <tên-nhánh-mới>
6️⃣ Merge nhánh làm việc vào nhánh gốc khi hoàn tất
bash
Copy
Edit
git checkout <frontend|backend|data>
git merge <tên-nhánh-mới>
git push origin <frontend|backend|data>
7️⃣ Dọn dẹp nhánh dư sau merge
bash
Copy
Edit
git branch -d <tên-nhánh-mới>           # Xóa nhánh local
git push origin --delete <tên-nhánh-mới> # Xóa nhánh remote
8️⃣ Merge vào nhánh main chính
bash
Copy
Edit
git checkout main
git pull origin main
git merge <frontend|backend|data>
git push origin main
✅ Lưu ý:

Luôn kiểm tra tên nhánh và trạng thái trước khi merge.

Nếu có conflict, chỉnh sửa file, git add <file> rồi commit trước khi push.

Tên nhánh phải rõ ràng, tránh trùng lặp.
