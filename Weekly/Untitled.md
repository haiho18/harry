---
type: weekly-review
week: 2026-W48
date: 2026-11-24
tags: [review]
---
# 🔁 Weekly Review — Tuần 48/2026

## 1. Dọn dẹp (≈10 phút)
- [ ] Inbox về 0: xử lý / chuyển / xóa từng note trong `00 Inbox`
- [ ] Đọc lại Daily notes 7 ngày qua, tách ý hay thành note riêng
- [ ] Project nào đã xong → chuyển sang `04 Archive`

n8n hadhiad
### Inbox hiện tại
```dataview
LIST
FROM "00 Inbox"
SORT file.ctime ASC
```

### Daily notes tuần này
```dataview
LIST
FROM "Daily"
WHERE file.day >= date(today) - dur(7 days)
SORT file.day ASC
```

## 2. Rà soát project (≈10 phút)
```dataview
TABLE status AS "Trạng thái", deadline AS "Deadline"
FROM "01 Projects"
WHERE status != "done"
SORT deadline ASC
```
- Project nào đang chậm? Vì sao?
  - 

## 3. Việc quá hạn / tuần tới
```tasks
not done
due before in 7 days
sort by due
```

## 4. Nhìn lại (≈10 phút)
- ✅ Thành quả tuần này:
- 🧱 Điều cản trở:
- 💡 Bài học:

## 5. Tuần tới
- 🎯 3 ưu tiên lớn nhất:
  1. 
  2. 
  3. 
