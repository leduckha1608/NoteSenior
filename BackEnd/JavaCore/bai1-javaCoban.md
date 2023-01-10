#####   https://viettuts.vn/java

### 1. Java là gì:
    * Java là một ngôn ngữ lập trình hiện đại, bậc cao và hướng đối tượng, bảo mật mạnh mẽ. 
    * Java là một Platform.
        ==> Platform: bất cứ môi trường phần cứng hoặc phần mềm nào đó có 1 chương trình chạy thì được hiểu là một Platfrom.

    * java được dùng để làm gì: 
        + Web app
        + Desktop app
        + Mobile app
        + ... nhúng, game, AI...
    

### 2. Các tính năng của Java
--> Java có rất nhiều tính năng nổi bật. 

    * Simple ( đơn giản):
        + cú pháp đơn giản
        + gỡ bỏ nhiều đặc điểm gây rối và hiếm khi sử dụng: con trỏ, nạp chồng toán tử...
        + ko cần có các đối tượng mà ko được tham chiếu, bộ dọn rác sẻ tự động làm.

    * Object Oriented (hướng đối tượng):
    --> tổ chức phần mềm dưới dạng kết hợp của nhiều loại đối tượng khác nhau, trong đó có sự kết hợp chặt chẽ giữa dữ liệu và hành vi.
        + 

    * Platform Indepedent (nền tảng độc lập):
    --> Java cung cấp software-bare platform 
        + JRE (Java Runtime Environment)
        + API (Application Programming Interface)
        ==> Java được biên dịch bởi Compiler (trình biên dịch) và được truyển thành Bytecode. Bytecode là code độc lập nên tảng nên có thể chạy ở nhiều nền tảng khách nhau.

    * Secured (bảo mật):
        + ko có con trỏ tường minh
        + chương trình bên trong là máy ảo
        + Classloader: thêm sự bảo mật bằng việc phân chia package cho các class của hệ thống file trên local mà từ đó chúng được import với file nguồn.
        + Bytecode Vertifier: kiểm tra các đoạn code để tìm ra các phần code ko hợp lệ mà có thể truy cập trái phép với các đối tượng 
        + Security Manager: quyết định xem nguồn resource nào mà 1 lớp có thể truy cập chẳng hạn như có quyền đọc ghi tới local disk.

    * Robust (mạnh mẽ):
    --> Java có sử dụng trình quản lý bộ nhớ mạnh mẽ.
        + Garbage Collection (trình tự động dọn rác):
        + Exception Handling: sử lý ngoại lệ  

    * Architecture-neutral (kiến trúc tập chung):

    * Portable (Khả chuyển):
    --> bytecode của java có thể mang đi nhiều nền tảng khác nhau mà vẫn chạy bình thường nên nói java có tính Portale (khả chuyển)

    * Dynamic (năng động):

    
    * Interpreted (thông dịch):
    * High Preformance (hiệu suất cao):
        + hiệu suất Java nhanh hơn kể từ khi thông dịch thành bytecode, nhưng chậm hơn so với một số ngôn ngữ biên dịch.

    * Multi-thread (đa luồng):
        + giúp tạo ứng dụng phân tán. RMI và EJB được sử dụng để tạo ứng dụng này. cho phép truy cập các file bằng cách gọi các phương thức từ bất kỳ thiết bị nào trên internet.

    * Distributed (phân tán):

### 3. Cài đặt môi trường Java
### 4. thiết lập Path cho java

### 5. JDK, JRE và JVM
    * JVM ( Java Virtual Machine)
    --> JVM là một thiết bị ảo (trừu tượng) có thể giúp máy tính chạy các chương trình java. nó cung cấp môi trường runtime mà trong đó Java bytecode có thể thực thi.
        + nhiệm vụ:
            - tải code
            - kiểm tra code
            - thực thi code
            - cung cấp môi trường runtime
        + cấu trúc:
            - Classloader: là một hệ thống con của JVM được sử dụng để tại class file.
            - Class(method) Area: lưu trữ cấu trúc mỗi lớp, như hằng, trường, dữ liệu phương thức, code phương thức...
            - Heap: khu vực dữ liệu runtime trong đó đối tượng được cấp phát
            - Stack: lưu trữ các Frame. Nó giữ các biến cục bộ và các kết quả cục bộ, và thực hiện một phần nhiệm vụ trong việc trả về phương thức.
                + mỗi thread có một vùng nhớ Stack riêng, được khởi tạo cùng thời điểm với thread
                + mỗi Frame mới được tạo mỗi khi một phương thức được triệu hồi và kết thúc khi hủy
            - Program Counter Register: chứa địa chỉ của lệnh JVM hiện tại được thực thi.
            - Native method stack: là vùng nhớ chứa mã bytecode của các ngôn ngữ khác Java
            - Execution Engine: gồm
                + Virtual Processor ( bộ xử lý ảo)
                + Interpreter ( trình thông dịch)
            - JIT (Just-In Time): biên dịch các thành phần bytecode mà có cùng tính năng tại cùng một thời điểm, giảm thời gian cần thiết để biên dịch 

    * JRE   ( Java runtime environment)
    --> là gói phần mềm cung cấp các thư viện của java, cùng với JVM (máy ảo), và các thành phần # để chạy ứng dụng java

    * JDK   ( Java Development Kit)
    --> gồm JRE và development tool.

### 6. Biến trong Java
--> biến là tên của một vùng nhớ gồm ( local, instance, static)

    * Biến local: 
    --> 
        + biến được khai báo trong method, constructor, hoặc trong các block
        + biến được tạo bên trong method , constructor, block sẻ bị hủy khi kết thúc.
        + ko sử dụng access modifier
        + Các biến được lưu trên vùng nhớ stack
        + cần khởi tạo giá trị mặc định, ko khởi tạo sẻ bị lỗi biên dịch.

    * Biến instance (biến toàn cục):
    -->
        + khai báo bên trong Class, bên ngoài method, constructor, block.
        + biến instance được lưu trong vùng nhớ heap.
        + biến được tạo khi đối tượng được tạo bằng từ khóa new, và bị hủy khi đối tượng hủy.
        + có thể sử dụng biến instance trong method, constructor, block nhưng phải thông qua một đối tượng cụ thể
        + sử dụng acccess modifier, trạng thái mặc định là default
        + biến instance có giá trị mặc định của kiểu dữ liệu nên ko cần khởi tạo trước khi sử dụng
    
    * Biến static
    --> 
        + biến static được khai báo trong class với từ khóa 'static', ở phía ngoài phương thức, constructor và block.
        + biến static là biến duy nhất của class, ko phụ thuộc vào số lượng đối tượng của lớp
        + biến static được lưu trữ trong bộ nhớ static riêng. được khởi tạo khi chương trình bắt đầu khởi chạy và phát hủy khi kết thúc chương trình.
        + giá trị mặc định của biến static phụ thuộc vào kiểu dữ liệu.
        + biến được truy nhập thông qua class chứa ko, ko phải là đối tượng
        + phương thức static có thể truy nhập biến static.

### 7. Các kiểu dữ liệu
--> kiểu dữ liệu được chia thành nguyên thủy và đối tượng 

    * Kiểu Primitive ( kiểu dữ liệu nguyên thủy)
        Boolean, Char, Byte, Short, Int, Long, Float, Double

    * Kiểu Non-Primitive ( kiểu dữ liệu đối tượng)
        String, Array, Object...


### 8. Type casting (ép kiểu)
--> ép kiểu trong Java là việc gán giá trị biến từ kiểu dữ liệu này bằng kiểu dữ liệu khác.

    * Widening (nới rộng)
        + làm tròn theo kiểu dữ liệu có kích thước lớn hơn.
        + kiểu biến đổi này ko làm mất thông tin 
        + byte -> short -> int -> long -> float -> double

    * narowwing (thu hẹp)
        + làm tròn theo kiểu dữ liệu có kích thước nhỏ hơn.
        + kiểu biến đổi này làm mất thông tin 
        + double -> float -> long -> int -> short -> byte
        
### 9. Các toán tử
--> toán tử trong java là những ký hiệu được sử dụng để thực hiện một chức năng nào đó.

    * toán tử số học 
    --> thực hiện các tính toán số học ở dạng số.
        Cộng (a+b), trừ (a-b), nhân (a*b), chia (a\b), lấy dư (a%b), tăng dần (a++), giảm dần (--), cộng gán (a+=2), trừ gán (b-=5), nhân gán (c*=4), chia gán (d/=2), lấy dư gán (e%3=4).

    * toán tử bit 
    --> thực hiện các tao tác trên từng bit riêng biệt trong các kiểu dữ liệu nguyên thủy. trả về bit
    
        + NOT (~)
            phép bù, A sai thì bù của A đúng,   NOT 0011 =1100
        + AND (&)   
            A and B đúng khi cả A và B đúng,    0101 AND 0011 = 0001
        + OR  (|)
            A OR B đúng khi A đúng, B đúng hoặc cả A và B đúng.     0101 OR 0011 = 0111
        + Exclusive OR (^)
            A ^ B đúng khi, chỉ A đúng hoặc chỉ B đúng.
        + dịch phải (>>)
            dịch chuyển phải.   nếu sử dụng thanh ghi 8bit  10010111 >> = 11001011
        + dịch trái (<<)
            dịch chuyển trái.   nếu sử dụng thanh ghi 8bit  10010111 << = 00101111
    
    * toán tử quan hệ
    --> trả về giá trị boolean, đúng hoặc sai
        + == so sánh bằng, != so sánh khác, > lớn hơn, < nhỏ hơn, >= lớn hơn hoặc bằng, <= nhỏ hơn hoặc bằng

    * toán tử logic
        +   &&: A && B đúng khi cả A và B đúng
        +   ||: A || B đúng khi A đúng hoặc B đúng
        +   ^:  A ^ B đúng khi chỉ có A đúng hoặc chỉ có B đúng.
        +   !: A ! phủ định của A.   

    * toán tử điều kiện
        <expression1>    ?   <expression2>  :   <expression3>

    * toán tử gán (=) 
    --> dùng để gán giá trị cho biến

    * thứ tự ưu tin của các toán tử
        + phép tăng ++ phép giảm --
        + phép nhân * phép chia / phép lấy dư %
        + phép dịch chuyển bit >> , << , >>>
        + phép so sánh >, <, <=, >=, ==, !=
        + phép logic 
        + phép điều kiện
        + phép gán số học =, *=, /=, +=, -=

### 10. hệ thống Unicode:
    --> Unicode là một kiểu mã hóa ký tự chuẩn quốc tế, được hần hết các ngôn ngữ văn bản trên thế giới sử dụng
        + trong Unicode mỗi ký tự chiếm 2byte
        + trị nhỏ nhất là '\u0000' và lớn nhất là '\uFFFF'
        

### ---------------------------- tìm hiểu nâng cao--------------------
    * cơ chế dọn rác trong java:

    * Platform: là một môi trường ( cứng hoặc mềm) mà một hoặc nhiều chương trình có thể chạy trên nó.
        + software-based: dự trên phần mềm
        + hardware-based: dựa trên phần cứng

    * Bytecode là lý do khiến java là nền tảng độc lập. Byte code là tập các lệnh cho JVM (máy ảo Java), hoạt động tương tự trình biên dịch.

    * Bytecode hoạt động:
        + Source code -> Compiler -> Bytecode -> JVM -> Machine Code.

    * RMI in java: 
    --> Remote method Invocation: là một kỹ thuật cài đặt các đối tượng phân tán trong java. RMI là một phần của bộ J2SDK và là hàm thư viện hỗ trợ các lời gọi từ xa và trả về giá trị cho các ứng dụng toán phân tán.
    https://viblo.asia/p/java-rmi-va-ung-dung-phan-tan-don-gian-OEqGj50KM9bL
    https://viblo.asia/p/gioi-thieu-ve-java-rmiremote-method-invocation-XogBG2xrRxnL

    * EJB in java:
    --> EJB là 1 thành phần nằm ở phía server-side của 1 ứng dụng web hoặc có thể hiểu là 1 thành phần trong kiến trúc Java EE.
    https://coffeeprogrammingblog.wordpress.com/2016/11/26/gioi-thieu-ve-ejb-trong-java/

    * nên học lại các kiểu dữ liệu và chuyển đổi dữ liệu


