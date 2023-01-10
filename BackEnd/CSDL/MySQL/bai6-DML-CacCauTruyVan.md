
########### https://levunguyen.com/database/2020/05/07/cac-cau-lenh-sql-dml-trong-database/

$ câu truy vấn trong SQL

1. SELECT
    Select * from table_name;

2. INSERT
    Insert Into table_name (column1, column2,...) values (value1, value2,...);

3. UPDATE
    update table_name 
    set column1 = value1, column2 = value2,...
    where [condition];

4. DELETE
    delete table_name where [condition];

5. MERGE + USING   => dùng để trộn dữ liệu của 2 bảng.
    MERGE Bảng_đích
    USING Bảng_nguồn
    ON Điều_kiện_merge
    WHEN MATCHED THEN INSERT|UPDATE|DELETE Xử_lý_khi_so_khớp_điều_kiện_merge
    WHEN NOT MATCHED THEN INSERT|UPDATE|DELETE Xử_lý_khi_không_so_khớp_điều_kiện_merge;

6. CALL 	=> (* thủ tục khi gọi) 
7. EXPLAIN PLAN
8. LOCK TABALE
--------------
9. REPLACE => thay đổi dữ liệu
		 

--------------------------note tham khảo link
    MERGE : nên tìm hiểu kỹ     https://www.sql.edu.vn/microsoft-sql-server/merge/

https://viblo.asia/p/stored-procedure-va-trigger-trong-sql-server-Az45bPV6ZxY

--------------------------*note:
Lệnh MERGE dùng để hỗ trợ thực thi nhiều thao tác cập nhật dữ liệu một cách hiệu quả và 1 thao tác đơn giản:
    - cho phép thực hiện Insert/update/delete trong một câu lệnh duy nhất.
    - nâng cao hiệu suất truy vấn
    - kết thúc phải có dấu ;
    - có mệnh đề MATCHED
        + When MATCHED Then => sử lý khi khới Điều_kiện_merge
        + When Not MATCHED Then => sử lý khi ko khớp Điều_kiện_merge
        + When Not Matched By Target    => nếu Điều_kiện_merge ko khớp, thì thực hiện Target
        + When Not Matched By Source    => nếu Điều_kiện_merge ko khớp, thực hiện Source

Output: dùng để kết xuất dữ liệu liên quan đến lệnh ra màn hình hoặc bảng.
    + Insert: tham chiếu đến dữ liệu mới sau khi thay đổi
    + Deleted: tham chiếu đế dữ liệu cũ trước khi thay đổi
