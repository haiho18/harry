<%*
const topic = await tp.system.prompt("Chủ đề cuộc họp");
const project = await tp.system.prompt("Thuộc project nào? (để trống nếu không)", "");
const today = tp.date.now("YYYY-MM-DD");
await tp.file.move("Meetings/" + today + " " + topic);
-%>
---
type: meeting
date: <% today %>
time: <% tp.date.now("HH:mm") %>
project: <% project ? '"[[' + project + ']]"' : "" %>
attendees: []
tags: [meeting]
---
# 🗓️ <% topic %>

**Ngày:** [[<% today %>]] · **Project:** <% project ? "[[" + project + "]]" : "—" %>

## 🎯 Mục tiêu cuộc họp
- <% tp.file.cursor() %>

## 📝 Nội dung chính
- 

## ✔️ Quyết định
- 

## 📌 Việc cần làm
- [ ] Việc — @người phụ trách 📅 YYYY-MM-DD
- [ ] 

## ❓ Vấn đề còn mở
- 
