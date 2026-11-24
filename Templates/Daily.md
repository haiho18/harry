<%*
// Lấy ngày từ tên file (YYYY-MM-DD); nếu tên file không phải ngày thì dùng hôm nay
const parsed = moment(tp.file.title, "YYYY-MM-DD", true);
const day = parsed.isValid() ? parsed : moment();
const thu = ["Chủ nhật", "Thứ Hai", "Thứ Ba", "Thứ Tư", "Thứ Năm", "Thứ Sáu", "Thứ Bảy"][day.day()];
if (!parsed.isValid()) {
  await tp.file.move("Daily/" + day.format("YYYY-MM-DD"));
}
-%>
---
type: daily
date: <% day.format("YYYY-MM-DD") %>
tags: [daily]
---
# <% thu %>, <% day.format("DD/MM/YYYY") %>

<< [[<% day.clone().subtract(1, "day").format("YYYY-MM-DD") %>]] | [[<% day.clone().add(1, "day").format("YYYY-MM-DD") %>]] >>

## 🎯 3 việc quan trọng nhất hôm nay
- [ ] <% tp.file.cursor() %>
- [ ] 
- [ ] 

## 📋 Việc đến hạn / quá hạn
```tasks
not done
due before tomorrow
sort by due
```

## 🗓️ Cuộc họp hôm nay
```dataview
LIST
FROM "Meetings"
WHERE date = this.date
```

## 📝 Ghi chép trong ngày
- 

## 💡 Ý tưởng / điều học được
- 

## 🔁 Cuối ngày
- Đã làm được:
- Vướng mắc:
- Ngày mai cần:
