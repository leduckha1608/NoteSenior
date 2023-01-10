################ https://viettuts.vn/java

## 1 câu điều kiện + vòng lặp 
    + If (nếu) ,  else (ngược lại), else if (ngược lại nếu):
        --> điều kiện If trả về giá trị true thì câu lệnh bên trong được thực hiện.
        --> Esle gắn liền với if gần nhất, hoặc có thể gồm if - else if - else if - else if ... - else. 
    + switch- case: 
        -->  

## 2 String trong java
--> String cung cấp thao tác thực hiện với chuỗi. 
    + có tính đối tượng, so sánh tính toán, biểu diễn chuỗi.
    + khởi tạo bằng new hoặc nháy kép
    + String được lưu vào vùng nhớ đặc biệt (Pool) gọi là hằng số chuỗi => giúp tiết kiệm vùng nhớ
    + String có tính bất biến

    * String Buffer:
        + được sử dụng để tạo ra chuỗi có thể thay đổi được (do String bị hạn chế tính bất biến)
        + có tính đồng bộ, luồng an toàn

    * String Builder:
        + giống Buffer là có thể thay đổi
        + ko có tính đồng bộ , có thể truy nhập đồng thời
    
    * một số phương thức của String:

## 3 hướng đối tượng
--> OOP ( Object Oriented Programming) là một phương pháp hay mô hình giúp tăng năng suất hiệu, đơn giản hóa, dễ bảo trì.
    * Constructror trong Class:
        + là một dạng đặc biệt của phương thức, sử dụng để khởi tạo đối tượng
        + được gọi ra thời điểm tạo ra đối tượng
        + trả về lớp hiện tại, ko được kế thừa, ko có final

    * Static trong java (biến tĩnh)
        + biến: được dùng để tham chiếu thuộc tính chung của tất cả các đối tượng
        + phương thức: thuộc lớp , ko thuộc đối tượng, có thể gọi mà ko cần khởi tạo, có thể truy nhập thay đổi biến Static
        + khối: gồm nhiều thành viên Static

    * Modifiler: 
    --> là phạm vi truy cập của biến, phương thức hoặc lớp.
        + private: -> trong lớp
        + default: -> trong cùng package
        + protected: -> ngoài package nhưng phải thừa kế
        + public:  -> truy nhập mọi nơi

    * this:
    --> this là từ khóa trong java để tham chiếu đến đối tượng hiện tại
        + tham chiếu tới các biến instance trong lớp hiện tại
        + dùng để sử dụng Constructror, phương thức của lớp hiện tại

    * super
    --> super là từ khóa trong java tham chiếu đến lớp cha của lớp hiện tại

    * 4 tính chất:
        + kế thừa:
            --> kế thừa là trong đó class con được thừa hưởng tất cả các thuộc tính và phương thức của class cha.
            Object là cha của mọi class.

        + Đóng gói:
            --> đóng gói là ấn giấu thông tin dữ liệu ko liên quan, chỉ cho phép truy cập những thông tin cần thiết. mục đích nhằm giảm độ phức tạp

        + Trừu tượng: (Abstract)
            --> tính trừu tượng là ẩn các tri tiết bên trong chỉ hiện thị các tính năng tới người dùng.
            gồm Interface và Abstract Class

        + Đa hình: 
        --> gồm Đa hình runtime (lúc thực thi) và compile (lúc biên dịch).
            + Đa hình lúc runtime là quá trình phương thức được ghi đè trong thời gian thực thi.
            + phương thức ghi đè thông qua biến tham chiếu của lớp cha
            + khởi tạo đối tượng hoặc ép kiểu đối tượng class cha bằng định dạng của class con, thì có thể sử dụng phương thức của class con.
            + overide và overloading => 2 tính chất đa hình


    * Interface:
        + là một bản thiết kế của lớp, ko thể khởi tạo, ko chứa Constructror
        + các phương thức đều là no body
        + có thể thừa kế nhiều interface khác, từ khóa kế thừa là implement
        + interface phải là public
        
    * Abstract:
        + tập chung vào đối tượng, ẩn các cài đặt chi tiết, chỉ hiển thi tính năng tới người dùng
        + các phương thức rỗng, ko thể khởi tạo 
        + Class và Abstract Class sử dụng từ khóa là extend
    
## 4 Xử lý ngoại lệ
--> là tình trạng bất thường làm gián đoạn luồng của chương trình.
    * Checked Exception: là ngoại lệ xảy ra do người dùng, ko thể lường trước được
    * Unchecked Exception: là ngoại lệ xảy ra ở runtime, ngoại lệ có thể tránh được
    * Error 

    * Try-catch: 
        + Khối try được sử dụng để chứ đoạn mã code có thể xảy ra ngoại lệ. nó phải được khai vào trong phương thức
        + Khối catch là để xử lý các Exception, được sử dụng sau khối Try
        + Khối finally luôn được thực hiện. 
        + 1 try có nhiều catch và 1 finally

    * Throw: dùng để ném ra ngoại lệ cụ thể
    * Throws: dùng để thông báo có ngoại lệ

    * Exception handing:  ????

## 5 Collections
--> Collections cung cấp một kiến trúc để lưu trữ và thao tác với các nhóm đối tượng. 
--> Collection là hệ thống cấp bậc Collection.

    * List:
    --> có chỉ số index, có thể chèn, sửa, xóa dựa trên chỉ số index.
        + có chứ các phần tử trùng lặp
        + duy trì thứ tự
        + ko đồng bộ
        * ArrayList => thao tác chậm, vì cần dịch chuyển
            + là một mảng động
        * LinkedList => thao tác nhanh, vì ko cần dịch chuyển 
            + Doubly Linked List: danh sách liên kết đôi (1 phần tử sẻ biết thằng đứng trước và đứng sau nó)


    * Set:
    --> ko chứa các phần tử trùng lặp
        + phần tử chứ giá trị là duy nhất, ko trùng lặp
        + Set sẻ lưu giá trị ở HashMap, với value là key của hashMap, nên mỗi giá trị của Set là duy nhất

        * HashSet: => cơ chế là hàm băm (nhanh), nhưng ko duy trì thứ tự
        * LinkedHashSet: cho phép 1 ptu null, duy trì thứ tự chèn`
        * TreSet: Duy trì thứ tự tăng dần.

    * Map:
    --> dữ liệu được lưu dưới dạng (key + value) , key là duy nhất.
        * HashMap:  ko duy trì thứ tự
        * LinkedHashMap: duy trì thứ tự
        * TreeMap: duy trì thứ tự tăng dần
        * HashTable: ko cho giá trị null, ko đồng bộ

    * Enum:
        + EnumMap
        + EnumSet

## 6 Đa luồng
--> Đa luồng trong java là tiến trình thực hiện nhiều luồng đồng thời 
    + tiết kiệm thời gian 
    + các luồng ko bị ảnh hưởng lẫn nhau.

    * vòng đời Thread:
        + new: khời tạo 
        + Runnable: trình biên dịch
        + Running: trình lên lịch và chọn thread 
        + Non-Runnable (blocked): thread vẫn sống nhưng ko được chọn
        + Terminated: ko run() thoát
        + ---------- một số phương thức lớp Thread
        + run()
        + start()
        + sleep()
        + join()
        + getPriority() => trả về mức độ ưu tiên
        + setPriority() => thay đổi mức độ ưu tiên
        + getName() 
        + setName()
        + currentThread() => trả về thread đang được thực thi
        + getId()
        + getState()    => trả về trạng thái
        + isAlive()     => kiểm tra thread còn sống hay ko
        + yield()       => cho phép thread tạm dừng để thread # thực thi
        + suspend()     => hoãn các thread, ko dùng nữa
        + resume()      => tiếp tục thread đang bị hoãn
        + stop()
        + isDaemon()    => kiểm tra nếu thread là một luồng hiểm
        + setDaemon()   => đánh dấu thread là môt luồng hiểm hoặc luồng người dùng
        + interrupt()   => ngắt thread
        + isInterrupt() => kiểm tra thread đã bị ngắt
        + interrupted() => kiểm tra nếu thread hiện tại bị ngắt
        + ------------ 
        + mức độ ưu tin của thread: 
            - min = 1, mặc định = 5, max = 10
            - setPriority: dùng để sét mức độ ưu tiên

        + luồng hiểm (thread Daemon): 
            - luồng gom rác, gom các tài nguyên ko sử dụng để giải phóng bộ nhớ.
            - luồng được đánh dấu bởi phương thực setDaemon(true).
        + thread pool: 
            - gồm nhóm các thread đang chờ đợi công việc, để tái sử dụng nhiều lần. 
            - tiết kiệm thơi gian, ko cần khởi tạo thread mới
            - khởi tạo + call:
                ExecutorService executor = Executors.newFixedThreadPool(5);
                executor.execute(worker);

    * Synchronization:
        - đồng bộ là khả năng kiểm soát nhiều luồng đến bất kỳ nguồn tài nguyên chia sẻ.
        - sychronized  => khối đồng bộ
        - Deadlock     => là bế tắc trong luồng, xảy ra khi cả 2 luồng đều đang chờ đợi giải phóng khóa

## 7 tính năng mới

--------------------
## 8 java JDBC

## Hibernate:
--> là một giải pháp ORM ( Object Relational Mapping) mã nguồn mở, gọn nhẹ. giúp đơn giản hóa việc thao tác với csdl

    * lớp persistent 

    * Session: 

#### ------------------- tham chiếu và tham trị trong java

+ tham trị là dành cho các kiểu dữ liệu nguyên thủy
+ tham chiếu dành cho các kiểu dữ liệu đối tượng.