# 04 - Locking

## 1. Tại sao cần Lock?

Khi nhiều transaction cùng đọc và sửa một bản ghi, có thể xảy ra xung đột dữ liệu.

Ví dụ: sách chỉ còn 1 bản nhưng hai transaction cùng thực hiện mượn.

## 2. Optimistic Locking

Không khóa row ngay khi đọc.

Dùng cột `version` để phát hiện dữ liệu đã bị transaction khác thay đổi.

Nếu update với version cũ không còn khớp, PostgreSQL trả về `update 0`.

### Khi nên dùng
- đọc nhiều;
- ghi ít;
- conflict hiếm.

## 3. Pessimistic Locking

Khóa row trước bằng:

```sql
select ...
for update;
```

Transaction khác muốn khóa cùng row phải chờ.

### Khi nên dùng
- conflict dễ xảy ra;
- tồn kho;
- đặt chỗ;
- tài chính.

## 4. So sánh

| Tiêu chí | Optimistic | Pessimistic |
|---|---|---|
| Giả định | conflict hiếm | conflict dễ xảy ra |
| Khóa ngay khi đọc | không | có |
| Khi conflict | phát hiện khi update | chờ lock |
| Phù hợp | CRUD thông thường | tồn kho, đặt chỗ, tài chính |


Xem `screenshots/README.md`.
