# 03 - Pagination

## 1. Tại sao cần phân trang?

Không nên trả về toàn bộ tập dữ liệu lớn trong một lần vì:
- tốn tài nguyên;
- tăng dữ liệu truyền qua mạng;
- giao diện xử lý chậm;
- thời gian phản hồi lớn.

## 2. Offset-based Pagination

```sql
select id, title
from books
order by id
limit 3 offset 3;
```

Công thức:

```text
offset = (page - 1) * page_size
```

### Ưu điểm
- dễ hiểu;
- dễ triển khai;
- có thể nhảy đến trang cụ thể.

### Nhược điểm
- offset lớn có thể chậm;
- dữ liệu thêm/xóa liên tục có thể làm các trang dịch chuyển.

## 3. Cursor-based Pagination

```sql
select id, title
from books
where id > 3
order by id
limit 3;
```

### Ưu điểm
- phù hợp dữ liệu lớn;
- phù hợp load more hoặc infinite scroll.

### Nhược điểm
- khó nhảy thẳng đến trang số N;
- cần giữ cursor trước đó.

> `limit + offset` có trong tài liệu đã gửi. Cursor-based được bổ sung theo đúng yêu cầu Week 1.

Xem `screenshots/README.md`.
