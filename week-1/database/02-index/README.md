# 02 - Index

## 1. Index là gì? Tại sao cần?

Index là cấu trúc dữ liệu giúp database tìm bản ghi nhanh hơn, có thể hình dung như mục lục của một cuốn sách.

Khi không có index phù hợp, database có thể phải quét nhiều hoặc toàn bộ bảng.

Khi có index phù hợp, PostgreSQL có thể tìm vị trí dữ liệu nhanh hơn.

## 2. Khi nào nên đánh Index?

Thường cân nhắc với cột thường xuyên xuất hiện trong:
- `where`;
- `join ... on`;
- `order by`;
- điều kiện tìm kiếm có tính chọn lọc tốt.

## 3. Khi nào không nên đánh Index?

Không nên tạo index tràn lan vì:
- tốn dung lượng lưu trữ;
- `insert`, `update`, `delete` phải cập nhật thêm index;
- bảng nhỏ có thể không cần thêm index;
- một số cột có quá ít giá trị khác nhau có thể không mang lại lợi ích đáng kể.

## 4. Thực hành

Chạy `index-demo.sql`.

Dùng:

```sql
explain (analyze, buffers)
```

để so sánh cùng một query trước và sau khi tạo index.

Xem `screenshots/README.md`.
