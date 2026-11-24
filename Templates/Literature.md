<%*
const title = await tp.system.prompt("Tên sách / bài viết / video");
const kind = await tp.system.suggester(["📚 Sách", "📰 Bài viết", "🎬 Video", "🎧 Podcast", "🎓 Khóa học"], ["book", "article", "video", "podcast", "course"]);
const author = await tp.system.prompt("Tác giả", "");
const url = await tp.system.prompt("Link (nếu có)", "");
await tp.file.move("03 Resources/Literature/" + title);
-%>
---
type: literature
source_type: <% kind %>
author: <% author %>
url: <% url %>
date_read: <% tp.date.now("YYYY-MM-DD") %>
status: reading
rating: 
tags: [literature]
---
# <% title %>

> **Tác giả:** <% author || "—" %> · **Nguồn:** <% url ? "[link](" + url + ")" : "—" %>

## 🧠 Tóm tắt bằng lời của tôi (3–5 câu)
<% tp.file.cursor() %>

## ✨ Ý chính / trích dẫn đáng giữ
- 

## 🔗 Liên hệ với những gì tôi đã biết
- Liên quan tới [[ ]] vì...

## 🛠️ Áp dụng được gì vào công việc / cuộc sống
- [ ] 

## 🌱 Ý tưởng tách ra thành Permanent note
- [[ ]]
