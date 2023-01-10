###     Inner class - lớp lồng nhau

### 1. Inner class
--> là 1 lớp được khai báo in class or interface khác. thường được sử dụng để nhóm các lớp và interface có 1 cách logic lại với nhau.

    * ưu điểm của inner class
        + biểu diễn cho 1 kiểu đặc biệt của mối quan hệ trong đó là nó có thể truy cập các thành viên dữ liệu method của lớp ngoài bao gồm cả private
        + sử dụng giúp code dễ đọc, dễ bảo trì vì nó nhóm các lớp và interface 1 cách logic vào 1 nơi.
        + tiết kiệm code

    * Các kiểu lớp lồng nhau
        + lồng no-static: member inner class, Annomynous inner class, local inner class
        + lồng static: Nested class, nested interface

    * Member inner class 
    --> một lớp được tạo trong 1 lớp và năm ngoài method
        + Hoạt động nội bộ của member inner class.
        --> trình biên dịch tạo ra 2 file class, và tên của lớp trong là "Outer$Inner"
            - muốn tạo ra lớp trong, phải tạo trước lớp ngoài.
        + Code nội bộ được tạo bởi trình biên dịch
            - các member inner class có thể tham chiếu lớp ngoài

    * Annomymous inner class
    --> lớp được tạo ra để implements interface hoặc extends class 
        + một lớp ko có tên gọi, được gọi là lớp vô danh hay annonymous inner class. 
            - được sử dụng khi bạn muốn ghi đè method của class hoặc interface.

        + có thể tạo ra bằng 
            - Class hoặc abstract 
            - Interface

        + Hoạt động của anonymous với class được tạo ra nhưng tên được quyết định bởi trình biên dịch
            - đối tượng được tạo ra va tham chiếu bằng biến tham chiếu của lớp ngoài.

        + hoạt động của anonymous inner class với interface => y chang anonymous của class, vì trình biên dịch tự tạo là class anonymous.

    * Local inner class
    --> một lớp được tạo ra trong method. nếu bạn gọi method thì bạn phải khởi tạo luôn class bên trong method chứ nó.

    * static nested class 
    --> một lơp static được tạo ra trong lớp
        + chỉ có thể truy cập các thành viên static của lớp ngoài
        + ko thể truy cập các thành viên và method non-static 

    * nested interface
    --> 1 interface được tạo ra trong 1 interface.
        + phải là public
        + Interface lồng nhau được khai báo static một cách hiển nhiên
        