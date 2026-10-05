# 01 - SQL cơ bản

## 1. Tạo CSDL cho bài toán cụ thể

Bài toán: **Quản lý thư viện**.

Các bảng chính:
- `authors`: tác giả;
- `books`: sách;
- `members`: bạn đọc;
- `loans`: phiếu mượn;
- `loan_items`: chi tiết sách trong phiếu mượn.

## 2. DDL

DDL dùng để định nghĩa và thay đổi cấu trúc cơ sở dữ liệu.

Demo trong `ddl.sql`:
- `create table`;
- `alter table`;
- `drop table`.

Ngoài ra có:
- `primary key`;
- `foreign key`;
- `unique`;
- `not null`;
- `check`.

## 3. DML

Demo trong `dml-query.sql`:
- `select`;
- `insert`;
- `update`;
- `delete`.

## 4. Query

Demo trong `query.sql`:
- `where`;
- `inner join`;
- `left join`;
- `right join`;
- `group by`;
- `having`;
- `order by`.

`where` lọc dữ liệu thô theo từng hàng.

`group by` gom các hàng thành từng nhóm.

`having` lọc các nhóm sau khi đã tính toán tổng hợp.

## 5. Aggregate Functions

Demo trong `aggregate.sql`:
- `count`;
- `sum`;
- `avg`;
- `min`;
- `max`.

Lưu ý:

```text
count(*)      -> đếm tất cả hàng
count(column) -> bỏ qua null ở column
```

## Output cần chứng minh

- database có dữ liệu mẫu;
- chạy được `join`;
- chạy được `group by`;
- có đủ các nhóm lệnh theo yêu cầu.

Xem `screenshots`.
