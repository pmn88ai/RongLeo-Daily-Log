🧠 Daily Log — Nhật ký công việc cá nhân
📌 Giới thiệu
Daily Log là web app giúp bạn ghi lại toàn bộ công việc hàng ngày như một hệ thống “trí nhớ thứ hai”.
Không chỉ là ghi chép, app được thiết kế để:
• nhớ bạn đã làm gì
• nhớ bạn đã gặp ai
• nhớ việc nào chưa xong
• và giúp bạn tìm lại mọi thứ nhanh chóng
🎯 Mục tiêu
• Ghi nhanh, không friction
• Tìm lại dễ dàng
• Dùng được trên mọi thiết bị
• Không cần cài đặt phức tạp
⚙️ Công nghệ
• HTML + CSS + Vanilla JS (1 file duy nhất)
• Supabase (database + sync)
• LocalStorage (fallback khi offline)
🧩 Tính năng chính
📅 1. Timeline theo ngày
• Mỗi ngày chia 2 phiên: 
• ☀️ Sáng
• 🌙 Tối
• Hiển thị toàn bộ công việc theo timeline
✍️ 2. Ghi nhanh (Quick Add)
• Nhập tiêu đề + nội dung
• Chọn: 
• người gặp
• tag
• loại công việc
• mood
• Tự động detect phiên (sáng/tối)
👤 3. Liên kết với danh bạ
• Chọn người từ bảng contacts
• Lưu: 
• contact_id
• name
👉 Cho phép:
• xem lịch sử làm việc với từng người
• filter theo người
🔍 4. Tìm kiếm
Tìm theo:
• nội dung
• người
• tag
• follow-up
📌 5. Follow-up tracker
Tự động gom:
• tất cả việc có follow_up
• chưa hoàn thành (status = open)
😊 6. Mood tracking
Ghi lại trạng thái:
• 😊 vui
• 😐 bình thường
• 😤 căng
• 😴 mệt
• 🤩 hứng
📊 7. People view
• Xem danh sách người đã gặp
• Sắp xếp theo số lần xuất hiện
• Click → xem toàn bộ lịch sử
🔄 8. Sync đa thiết bị
• Dữ liệu lưu trên Supabase
• Dùng được: 
• điện thoại
• máy tính
💾 9. Fallback offline
• Nếu Supabase lỗi: → tự động dùng localStorage
📤 10. Export / Import
• Xuất dữ liệu JSON
• Import lại (có validate)
🌙 11. Dark mode
• Toggle light / dark
• Lưu local
🗄️ Database
Table: daily_logs
Các field chính:
• date, time, session
• title, content
• people (jsonb)
• tags (text[])
• type
• follow_up
• status
• mood
🔗 Liên kết hệ thống
App này được thiết kế để hoạt động cùng:
• contacts (danh bạ)
👉 tạo thành hệ:
🧠 Memory System
🚀 Cách sử dụng
1. Setup database
• Vào Supabase
• SQL Editor
• Chạy script trong file
2. Điền config
Trong index.html:
const CONFIG = { SUPABASE_URL: "...", SUPABASE_ANON_KEY: "...", USER_ID: "RongLeo", APP_ID: "daily_log" } 
3. Mở file
• Mở trực tiếp index.html
• Hoặc deploy lên Vercel
⌨️ Phím tắt
• Ctrl/Cmd + K → mở nhanh form ghi
🧠 Triết lý thiết kế
App này không phải:
❌ nhật ký truyền thống
Mà là:
✅ hệ thống ghi log công việc có thể truy vấn
🧩 Roadmap (tương lai)
Phase 2
• AI parse input tự nhiên
Phase 3
• AI search: 
• “lần cuối gặp A”
Phase 4
• Analytics: 
• gặp ai nhiều nhất
• làm gì nhiều nhất
🐉 Ghi chú
• Thiết kế tối ưu cho 1 người dùng
• Không over-engineer
• Ưu tiên: nhanh, gọn, dùng được ngay
🎯 Kết luận
Daily Log =
🧠 “bộ nhớ công việc cá nhân”
Nếu dùng đều mỗi ngày, bạn sẽ:
• không quên việc
• không quên người
• không bị mất context
