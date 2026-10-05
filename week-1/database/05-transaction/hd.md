# 05 - Transaction

## 1. Transaction là gì?

Transaction là một nhóm thao tác được xem như một đơn vị công việc.

## 2. Khi nào cần gom nhiều thao tác vào một Transaction?

Khi một nghiệp vụ gồm nhiều thay đổi dữ liệu phụ thuộc lẫn nhau.

Ví dụ:
- chuyển tiền;
- đặt đơn hàng và trừ tồn kho;
- mượn sách và cập nhật số lượng còn lại.

## 3. commit

`commit` xác nhận và lưu các thay đổi.

## 4. rollback

`rollback` hủy các thay đổi chưa được commit.

## 5. Ví dụ chuyển tiền

Trừ tài khoản A và cộng tài khoản B phải cùng thành công.

Nếu có lỗi thì rollback toàn bộ transaction.

Xem `screenshots/README.md`.
