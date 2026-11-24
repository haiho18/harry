<%*
const name = await tp.system.prompt("Tên project");
const status = await tp.system.suggester(["🟢 active", "🟡 planning", "⏸️ on-hold"], ["active", "planning", "on-hold"]);
const deadline = await tp.system.prompt("Deadline (YYYY-MM-DD)", tp.date.now("YYYY-MM-DD", 30));
await tp.file.move("01 Projects/" + name);
-%>
---
type: project
status: <% status %>
start: <% tp.date.now("YYYY-MM-DD") %>
deadline: <% deadline %>
owner: 
stakeholders: []
tags: [project]
---
# <% name %>

## 🎯 Mục tiêu
> Project này xong khi nào? Kết quả cụ thể, đo được là gì?

<% tp.file.cursor() %>

## 📌 Bối cảnh / Lý do
- 

## ✅ Phạm vi
**Trong phạm vi:**
- 

**Ngoài phạm vi:**
- 

## 🗺️ Kế hoạch & mốc
- [ ] Mốc 1 📅 
- [ ] Mốc 2 📅 
- [ ] Bàn giao / nghiệm thu 📅 <% deadline %>

## ⚠️ Rủi ro
| Rủi ro | Khả năng | Ảnh hưởng | Cách xử lý |
|---|---|---|---|
|  |  |  |  |

## 🧭 Nhật ký quyết định
- <% tp.date.now("YYYY-MM-DD") %>: Khởi tạo project.

## 🗓️ Các cuộc họp liên quan
```dataview
TABLE date AS "Ngày", attendees AS "Thành phần"
FROM "Meetings"
WHERE project = this.file.link
SORT date DESC
```

## 🔗 Tài liệu / liên kết
- 
