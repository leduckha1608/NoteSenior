########### https://levunguyen.com/database/2020/05/09/cac-ham-tong-hop-trong-database/

### 1 Index
--> Đánh dấu chỉ mục, lưu dữ liệu dưới dạng đặc biệt (key + value).  cho phép truy xuất tìm kiếm nhanh hơn.
    + Khóa chính là luôn là 1 dạng Index. 
    + chỉ nên đánh index những trường thường được sử dụng để tìm kiếm, tránh trường ít tìm kiếm và có giá trị null
    + cân nhắc đánh index 1 trường, hoặc 1 nhóm trường
    + index mặc định luôn là Btree

    * index B-tree
        - giá trị tăng dần từ trái sang phải, có thể sử dụng với các biểu thức so sánh, tối ưu được 'Order By'
    * index Hash Index ( hàm băm)
        - hàm băm, có thể sử dụng toán tử =, <> . ko tối ưu 'Order by'.
    * index R-tree *** tìm hiểu sau
=> nhược điểm: đánh index là giảm tốc độ thêm sử xóa

### 2 Trigger
--> là một đoạn code được vận hành dựa vào điều kiện xảy ra. thường được dùng để trèn vào sự kiện ( thêm, sửa, xóa) của một bảng đặc biệt mà ảnh hưởng đến sự đồng nhất của các bảng #
    * ưu điểm: 
        - khả năng bắt lỗi business ở mức cơ sở dữ liệu.
        - có thể sử dụng trigger thay thế việc thực hiện các công việc hẹn giờ.
        - hiệu quả khi được sử dụng để kiểm soát những thay đổi dữ liệu trong bảng 
    * nhược điểm:
        - chỉ mở rộng một phần, ko thể thay thế hoàn toàn công việc kiểm tra tính hợp lệ của dữ liệu.
        - Trigger chạy ngầm ở trong csdl, ko hiển thị ở tầng giao diện. Khó kiểm soát
        - tăng lượng công việc trên csdl nên làm chậm
### 3 View
--> View là một đoạn lệnh truy vấn đã được viết sẳn và lưu trong csdl. 1 view gồm một select cho ta thấy kết quả như một table, nhưng nó dữ liệu tổng hợp của nhiều bảng được truy xuất ra.
    * lợi ích
        + hạn chế truy cập các table cụ thể, chỉ cho xem qua view
        + hạn chế truy cập column của table. khi truy cập view bạn ko thể column nào mà view truy nhập (có thể dùng đại diện as cho column)
        + liên kết column từ nhiều table thành một view
        + trình bày các thông tin tổng hợp như (SUM, Count, Avg, min, max..)


### 4 Stored Procedures
--> Stored procedures là một tập hợp câu lệnh T-SQL thành một nhóm đơn vị xử lý logic và được lưu trữ trên database server. giống việc tạo một funtion và sử dụng lại


*khởi tạo
    CREATE PROCEDURE SelectAllCustomers @City nvarchar(30), @PostalCode nvarchar(10)
    BEGIN
    SELECT * FROM Customers WHERE City = @City AND PostalCode = @PostalCode
    END;
* dùng 
    CALL SelectAllCustomers @City = 'London', @PostalCode = 'WA1 1DP'; 

### 5 Grants => quyền

### 6 Transaction 
--> là tiến trình thực hiện các nhóm câu lệnh trong SQL. các câu lệnh này được thực thi một cách tuần tự độc lập. Một Transaction thành công khi tất cả các câu lệnh thành công, khi đó tất cả các thay đổi dữ liệu được thực hiện được lưu và csdl
    * Commit: lưu lại thay đổi
    * Rollback: quay lại thực hiện trước khi thay đổi
    * SavePoint: tạo điểm để Rollback.
    * Set Transaction: đặt tên cho Transaction.
    * Release SavePoint: xóa điểm SavePoint.

### 7 MERGE + USING   
--> dùng để trộn dữ liệu của 2 bảng.
    MERGE Bảng_đích
    USING Bảng_nguồn
    ON Điều_kiện_merge
    WHEN MATCHED THEN INSERT|UPDATE|DELETE Xử_lý_khi_so_khớp_điều_kiện_merge
    WHEN NOT MATCHED THEN INSERT|UPDATE|DELETE Xử_lý_khi_không_so_khớp_điều_kiện_merge;

    Mệnh MERGE dùng để hỗ trợ thực thi nhiều thao tác cập nhật dữ liệu một cách hiệu quả và 1 thao tác đơn giản:
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


### 8 Joins 
--> là phép kết nối dữ liệu từ nhiều bảng với nhau

    - Inner Join: trả về tất cả các hàng khi đó, điều kiện join có ở cả 2 Bảng 
    - Left Join:   trả về tất cả các dòng từ bảng bên trái và các dòng đúng từ bảng bên phải
    - Right Join:
    - full Join:

### 9 Group by and Having
--> Group by nhóm các dòng cùng giá trị.
    where: là câu điều kiện đối chiếu với từng dòng
    having: là câu điều kiện đối chiếu với từng nhóm, có thể kết hợp với các mệnh đề tổng hợp

### 10 Order by
--> dùng để sắp xếp thứ tự tăng dần hoặc giảm dần

-----------------------
### Inject trong SQL
--> là kỹ thuật lợi dụng lỗ hổng về câu truy vấn để tấn công.

    * gây ra :
        + lộ thông tin dữ liệu khách hàng
        + ảnh hương sấu đến City
        + 
    * cách tấn công: 
        + dự vào thông tin đăng nhập, hacker sẻ chèn vào câu lệnh Select.

### cách phòng chống:
    + lọc dữ liệu người dùng
    + ko cộng chuỗi tạo SQL
    + ko hiển thị Exception
    + phần quyền trong database
    + luôn có backup.

### tăng tốc trong sql:
    + giới hạn kết quả trả về
    + chỉ lấy dữ liệu cần thiết
    + truy vấn ko nên phức tạp  
    + dùng điều kiện thích hợp