###  Xử lý ngoại lệ
--> là tình trạng bất thường làm gián đoạn luồng của chương trình.



### 1. Exception handling:  
--> là cơ chế xử lý các lỗi runtime để duy trì luồng bình thường của ứng dụng.

    * Exception: 
        + là tình trạng bất thường
        +  Exception Handing là cơ chế sử lý lỗi runtime
    
    * lợi thế của Exception Handling
        + duy trì luồng bình thường ngay cả khi có trường hợp ngoại lệ làm gián đoạn luồng sử lý
    
    * Checked Exception: là ngoại lệ xảy ra do người dùng, ko thể lường trước được
        + IOException
        + SQLException
        + ClassNotFoundException

    * Unchecked Exception:(RuntimeException) là ngoại lệ xảy ra ở runtime, ngoại lệ có thể tránh được
        + ArithmeticException   / khi chia cho số 0
        + NullPointerException  / khi biến có giá trị null + gọi method
        + numberFormatException     / dữ liệu ko thể fomat thành dữ liệu số
        + IndexOutOfBoundsException
            - ArrayIndexOutOfBoundsException    / giá trị index được gọi ko nằm trong Array
            - StringIndexOutOfBoundsException   / giá trị index được gọi ko nằm trong String

    * Error 
        + StackOverflowError    / thường sảy ra khi sử dụng đệ quy ko kết thúc
        + VirtualMachineError   / khi máy ảo hỏng hoặc hết tài nguyên
        + OutOfMemoryError      / hết vùng nhớ trong bộ nhớ Heap, khi cố gắng tạo Object mà ko gian ko đủ.

### 2. Try-catch

    * Khối try được sử dụng để chứ đoạn mã code có thể xảy ra ngoại lệ. nó phải được khai vào trong phương thức

    * Khối catch là để xử lý các Exception, được sử dụng sau khối Try
        + có thế có 1 hoặc nhiều khối catch
        + vào thời điểm xảy ra ngoại lệ, chử có 1 khối catch được thực thi
        + các khối catch được sắp xếp theo tự từ cụ thể nhất đến chung nhất.

    * Khối try lồng nhau
        + lỗi phát sinh ở 1 phần trong khối lệnh và toàn bộ lênh thì dẫn tới 1 lỗi khác, nên try lồng nhau

    * Khối finally luôn được thực hiện. 
        + được dùng để  chèn lệnh "cleanup" và thực thi các lệnh quan trọng như đóng kết nối, đóng stream...
        + có thể thực hiện ngay cả khi try tồn tại return.
        + 1 try có nhiều catch và 1 finally

    
    * Throw: dùng để ném ra ngoại lệ cụ thể
    * Throws: dùng để thông báo có ngoại lệ
    * Truyền Exception caller => ko được truyển tiếp trong các hàm