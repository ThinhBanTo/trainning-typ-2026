# Screenshot - Transaction

## 01-before-transfer.png

```sql
select *
from accounts
order by id;
```

Chụp số dư ban đầu.

## 02-commit.png

Chạy transaction chuyển 100 từ A sang B rồi `commit`.

Chụp số dư sau commit:
- A giảm 100;
- B tăng 100.

## 03-before-rollback.png

Bắt đầu transaction khác, trừ 50 từ A nhưng chưa commit.

Chụp số dư bên trong transaction.

## 04-after-rollback.png

Chạy `rollback`, rồi:

```sql
select *
from accounts
order by id;
```

Chụp số dư đã quay về trạng thái trước transaction.
