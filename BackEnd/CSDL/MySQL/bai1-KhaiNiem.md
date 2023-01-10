###### tham khảo link: https://levunguyen.com/co-so-du-lieu-mysql/

### 1: Khái niệm 

# 1. Database Table:
	- là một bảng chứ 1 hoặc nhiều table. mỗi table được định nghĩa bởi tên.
	- table có nhiều cột và dòng. mỗi cột chứ tên trường (là thuộc tính), và mỗi dòng chứa dữ liệu.

# 2. SQL Statement: 
	- là các câu lệnh SQL, dùng để thực hiện các hành động trên Database.
	- câu lệnh ko phân biệt chữ hoa và chữ thường.
	- Câu lệnh SQL chia thành 4 loại

	a. Data Definition Language (DDL): câu lệnh định nghĩa cấu trúc dữ liệu.
		- CREATE 
		- ALTER 
		- DROP 
		- RENAME
		- COMMENT
		---------
		- TRUNCATE => làm trống dữ liệu  (* ko làm mất cấu trúc) 
		- DESCRIBE => hiển thị cấu trúc của 1 bảng
	
	b. Data Manipulation Language (DML): câu lệnh truy vấn , cập nhật và thêm dữ liệu.
		- SELECT
		- INSERT
		- UPDATE
		- DELETE
		- MERGE + USING   => dùng để trộn dữ liệu của 2 bảng.
		- CALL 	=> (* thủ tục khi gọi) 
		- EXPLAIN PLAN
		- LOCK TABALE
		--------------
		- REPLACE => thay đổi dữ liệu 

	c. Data Control Language (DCL): câu lệnh dùng để quản lý Permission(phân quyền) trong CSDL.
		- GRANT	 => gán quyền
		- REVOKE => xóa quyền
	
	d. Transaction Control Language(TCL): câu lệnh dùng cho việc thao tác Transaction trong Database.
		- COMMIT
		- ROLLBACK
		- SAVEPOINT
		- SET TRANSACTION
	
	
	
-----------------note
Tìm hiểu về EXPLAIN trong SQL : https://viblo.asia/p/tim-hieu-ve-explain-trong-sql-vyDZOnvPKwj

