#################### https://levunguyen.com/database/2020/05/09/cac-ham-tong-hop-trong-database/

$1. Các hàm tổng hợp trong SQL

a. Count - trả về số lượng, dùng để đếm số lượng bản ghi
    SELECT COUNT(*) 
    FROM employee_tbl ;

b. Sum  - trả về tổng, dùng để tính tổng của một trường
    SELECT SUM(daily_typing_pages) 
    FROM employee_tbl;

c. Avg  - trả về giá trị trung bình
    SELECT AVG(daily_typing_pages) 
    FROM employee_tbl;

d. Min  - trả về giá trị nhỏ nhất
    SELECT AVG(daily_typing_pages)
    FROM employee_tbl;

e. Max  - trả về giá trị lớn nhất
    SELECT id, name, MAX(daily_typing_pages)
    FROM employee_tbl GROUP BY name;

f. limit - lấy số lượng dòng, lấy số lượng bảng ghi, ko lấy tất cả
    SELECT * FROM Customers
    WHERE Country='Germany'
    LIMIT 3; 

