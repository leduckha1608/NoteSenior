################## https://levunguyen.com/database/2020/05/05/rang-buoc-du-lieu-trong-database/

$ các rằng buộc trong sql ( Constraint)

1. khái niệm
    Constraint là những quy tắc được áp dụng trên các cột dữ liệu, trên bảng. được sử sụng để kiểm tra tính hợp lệ của dữ liệu đầu vào, đảm bảo tính chính xác và toàn vẹn dữ liệu.

2. Not Null:    => đánh dấu, trường ko được phép null

3. Unique:      => đánh dấu, trường này ko được phép trùng lặp

4. Khóa chính(Primary key)   => khóa chính, dữ liêu duy nhất, luôn có 1 trường là khóa chính trong table

5. khóa phụ(Foreign key)     => khóa phu, khóa tham chiếu dùng để tham chiếu tới một table khác

6. Check()      => kiểm tra điều kiện nhập, thỏa mãn điều kiện mới được nhập dữ liệu vào table

7. Default      => gán giá trị mặc định khi ko khai báo

8. Index        => đánh dấu chỉ mục cho table. giúp tìm kiếm thông tin dễ dàng hơn.

9. Auto Increment => AUTO_INCREMENT, từ khóa giúp giá trị của trường trong bảng tự tăng. có thể mặc định hoặc gán giá trị tăng


-----------------------Note
nên tìm hiểu thêm về Index: 
https://viblo.asia/p/su-dung-index-trong-sql-query-1ZnbRlPQR2Xo
https://codelearn.io/sharing/index-trong-database