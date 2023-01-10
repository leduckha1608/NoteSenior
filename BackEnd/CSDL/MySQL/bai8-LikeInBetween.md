########## https://levunguyen.com/database/2020/05/10/su-dung-toan-tu-like-trong-database/

### 1. Like
--> được sử dụng trong mệnh đề where, tìm các dữ liệu dựa trên cú pháp cho trước

    *   2 toán tử trong like là '%' và'_' gồm các trường hợp:
        +   a%  --> tìm giá trị bắt đầu bằng chữ cái a
        +   %a  --> tìm giá trị có chữ cái kết thúc là a
        +   %a% --> tìm chữ cái có giá trị a
        +   _a% --> tìm giá trị có chữ cái thứ 2 là a
        +   a__% --> chữ đầu tiên là a và tối thiểu có 3 chữ cái
        +   a%z    --> bắt đầu bằng chữ a và kết thúc là chữ z
    * exam:
    Select * from Customers
    where CustomersName like '%kha';

### 2. In
---> được sử dụng trong mệnh đề Where, để kiểm tra nhiều giá trị.
    * exam:
        Select * from Customers
        where name In ('kha','bang','thanh');
### 3. Between
---> được dùng để kiểm tra điều kiện trong một khoảng.
    * exam:
        Select * from Customers
        where age Between 10 and 20;