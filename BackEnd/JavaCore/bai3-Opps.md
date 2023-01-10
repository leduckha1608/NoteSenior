##### OOP object oriented programming
--> OOP ( Object Oriented Programming) là một phương pháp hay mô hình giúp tăng năng suất hiệu, đơn giản hóa, dễ bảo trì.

### 0. lớp và đối tượng
    * Object(đối tượng) 
    --> Object là một thể hiện của class(lớp). Class là môt mẫu thiết kế, còn Object thì là được tạo ra 
        + trạng thái
        + hành vi
        + danh tính ...

    * Class (lớp)
    --> Class là một mẫu thiết kết từ đó tạo ra Object.
        + dữ liệu ( biến)
        + Constructor (hàm khởi tạo)
        + method (hàm)
        + Khối lệnh
        + Class and Interface

    * Các cách khởi tạo đối tượng trong java
        + key new
        + method newInstance()
        + method clone()
        + method factory 

    * đối tượng Annonymous trong java 
    --> đối tượng vô danh, ko có tham chiếu gọi, thường dùng khi chỉ sử dụng đối tượng 1 lần.

### 0.1 Package trong java
--> là một nhóm các kiểu tương tự của các lớp, giao diện và các package con. có package được dựng sẳn, và có package do người dùng tự định nghĩa.
https://niithanoi.edu.vn/package-trong-java.html#1-khai-niem-ve-package-trong-java

    * Lợi thế của việc sử dụng package trong java
        + dễ tìm kiếm và sử dụng class, interface... một cách dễ dành
        + cung cấp bảo vệ truy cập
        + ngăn chặn xung đội khi đặt tên
        + có thể coi là đóng gói dữ liệu ( hoặc ẩn dữ liệu)

    * truy cập Package từ một package khác:
        + import packagename.*
        + import packagename.classname;
        + sử dụng tên đầy đủ.
        ==> nếu import 1 package thì package con của package đó ko được import. thứ tự của chương trình là 
        package -> import -> class. 

### 1. Constructror trong Class:
        + là một dạng đặc biệt của phương thức, sử dụng để khởi tạo đối tượng
        + được gọi ra thời điểm tạo ra đối tượng
        + trả về lớp hiện tại, ko được kế thừa, ko có final

        * constructor default (mặc định)
            + rỗng ko có tham số 
            + nếu ko khai báo thì trình biên dịch cũng tự động tạo constructor default

        * constructor có tham số
        
        * constructor overloading trong java:
        --> có thể tạo nhiều constructor trong class
            + các constructor khác nhau về số lượng tham số và kiểu tham số truyền vào.

### 2. Static trong java (biến tĩnh)
--> được sử dụng chính để 

        * biến static: 
            + được dùng để tham chiếu thuộc tính chung của tất cả các đối tượng
            + Biến static lấy bộ nhớ chỉ 1 lần trong Class Area tại thời gian tải lớp.
            
        * phương thức: thuộc lớp , ko thuộc đối tượng, có thể gọi mà ko cần khởi tạo, có thể truy nhập thay đổi biến Static
            + method static ko thể sử dụng biến non-static hoặc gọi trực tiếp method non-static
            + từ khóa this và super ko thể sử dụng trong ngữ cảnh static

        * khối: gồm nhiều thành viên Static

### 3. Modifiler: 
--> là phạm vi truy cập của biến, phương thức hoặc lớp.

        + private: -> trong lớp
        + default: -> trong cùng package
        + protected: -> ngoài package nhưng phải thừa kế
        + public:  -> truy nhập mọi nơi

### 4. this:
    --> this là từ khóa trong java để tham chiếu đến đối tượng hiện tại
        + tham chiếu tới các biến instance trong lớp hiện tại
        + dùng để sử dụng Constructror, phương thức của lớp hiện tại

### 5. super
    --> super là từ khóa trong java tham chiếu đến lớp cha gần nhất của lớp hiện tại
    --> có thể dùng để gọi hàm trực tiếp của lớp cha

### 5.1 từ khóa final
    --> final được dùng để hạn chế người dùng

    * Biến final:(constant) varible final cannot change value

    * Method final: method final cannot overriding

    * Class final: ko thể kế thừa

    * Biến static final:

### 6. 4 tính chất:
        * kế thừa:
        --> kế thừa là trong đó class con được thừa hưởng tất cả các thuộc tính và phương thức của class cha.
            Object là cha của mọi class.

        * Đóng gói:
        --> đóng gói là ấn giấu thông tin dữ liệu ko liên quan, chỉ cho phép truy cập những thông tin cần thiết.
                + nhằm giảm độ phức tạp
                + bảo vệ trạng thái bên trong của đối tượng
                + ẩn dấu các biến biểu diễn trạng thái của đối tượng
                + mọi hành động sẻ được xác nhận thông qua phương thức


        * Trừu tượng: (Abstract)
        --> tính trừu tượng là ẩn các chi tiết tiết trình triển khai chỉ hiện thị các tính năng tới người dùng. 
            gồm Interface và Abstract Class

        * Đa hình: 
        --> gồm Đa hình runtime (lúc thực thi) và compile (lúc biên dịch).
            + Đa hình lúc runtime là quá trình phương thức được ghi đè trong thời gian thực thi.
            + phương thức ghi đè thông qua biến tham chiếu của lớp cha
            + khởi tạo đối tượng hoặc ép kiểu đối tượng class cha bằng định dạng của class con, thì có thể sử dụng phương thức của class con.
            + overide và overloading => 2 tính chất đa hình


### 7. Interface:
        + là một bản thiết kế của lớp, ko thể khởi tạo, ko chứa Constructror
        + các phương thức đều là no body
        + có thể thừa kế nhiều interface khác, từ khóa kế thừa là implement
        + interface phải là public
        
### 8. Abstract:
        + tập chung vào đối tượng, ẩn các chi tiết thực hiện, chỉ hiển thi tính năng tới người dùng
        + các phương thức rỗng, ko thể khởi tạo 
        + Class và Abstract Class sử dụng từ khóa là extend

### 8.1 Extend & implement
    + Extend: là kế thừa toàn bộ, gồm nội dung và hình thức
    + implement: là kế thừa hình thức
    

### 9. lớp Object
--> là cha của mọi class.
    + hữu ích khi sử dụng để tham chiếu bất kỳ đối tượng nào mà chưa biết kiểu dữ liệu
    + cung cấp cách xử lý chung cho các đối tượng ( so sánh, cloned, notified...)

    * các phương thức trong Object
        + getClass():   trả về đối tượng class hiện tại
        + hashCode():   trả về hashcode cho đối tượng hiện tại (là một chuỗi số để thực hiện hàm băm)
        + equals(obj):  so sánh
        + clone():      tạo ra class bản sao, hạn chế dùng new
        + notify():     đánh thức luồng, đợi trình giám sát hiện tại của đối tượng
        + notifyAll():  đánh thức tất cả các luồng
        + wait():       làm cho Thread hiện tại đợi trong khoảng thời gian là mili giây cụ thể, tới khi thread khác thông báo
        + finalize():   gọi Grabage Collector trước khi đối tượng bị dọn rác.

    
### 10. Object cloning:
--> là các để tạo ra 1 bản sao chính xác của đối tượng bị clone.
    + phương pháp này tiết kiệm tác vụ xử lý bổ sung để tạo ra một bản sao chính xác của đối tượng. thay vì dùng new sẻ mất nhiều tiến trình để thực hiện.
    
    * để sử dụng cloning cần:
        + class implements Cloneable
        + ghi đè lại method clone()

### 11. equals() và hashCode()

    * method equals():
    --> dùng để so sánh 2 đối tượng về mặt ngữ nghĩa(bằng các so sánh các thành viên dữ liệu). khác với việc so sánh == là so sánh về mặt kỹ thuật(tham chiếu tới địa chỉ vùng nhớ)
        + có thể ghi đè lại hàm equals()

    * hashCode():
    --> trả về một chuỗi số nguyên, sẻ được sử dụng bởi Collection dự trên bảng băm như Hashtable, HashSet, HashMap để lưu trữ các đối tượng trong các container nhỏ gọi là nhóm.

    * Các bước định vị 1 phần tử trong bảng băm:
        + nhận giá trị mã băm của phần tử bằng method hashCode()
        + tìm nhóm thích hợp được liên kết với mã băm
        + bên trong nhóm, tìm phần tử chính xác để so sánh

    * Các quy tắc của equals và hashcode.
        + khi method equals được ghi đè thì hashcode cũng bị ghi đè.
        + 2 đối tượng bằng nhau thì mã băm cũng bằng nhau
        + 2 đối tượng có mã băm khác nhau thì ko bằng nhau.


### 12. Array(mảng)
--> Array là một tập hợp các phần tử cùng kiểu dữ liệu được lưu trữ gần nhau trong bộ nhớ
    + các phần tử có  kiểu dữ liệu giống nhau
    + các phần tử có số lượng cố định
    + được đánh chỉ số thứ tự, bắt đầu là số 0
    
    * Các kiểu mảng: mảng 1 chiều, mảng 2 chiều

    * khởi tạo: có thể khởi tạo  Array rỗng có kích thước ban đầu, hoặc có thể khởi tạo luôn giá trị ban đầu. số lượng phần tử là cố định bất biến.

    * truy nhập phần tử: dùng chỉ số index của phần tử, khi duyệt các phần tử trong mảng có thể dùng for, for-each

    * các method:
        + birarySearch(Object[] arrayX, Object key) --> trả về vị trí của key trong mảng arrayX, nếu ko có trả về số âm.
        + equals()
        + fill(int[] a, int val) --> gán mỗi phần tử của a là val
        + sort(Object[] a)  --> sắp xếp mảng theo thứ tự tăng dần

### 13. Wrapper trong java
--> cung cấp một cơ chế chuyển đổi kiểu dữ liệu từ nguyên thủy thành đối tượng và ngược lại.
        
    * Autoboxing: là quá trình trong đó trình biên dịch Java tự động chuyển đổi kiểu dữ liệu căn bản thành các đối tượng Wrapper của chúng.
        + khi một method chờ đợi được truyền vào là 1 kiểu Wrapper mà giá trị được truyền lại là kiểu dữ liệu cơ bản.
        + khi gán giá trị kiểu dữ liệu căn bản cho đối tượng thuộc lớp Wrapper
        + khi làm việc với Collection

    * Unboxing: là quá trình mà trong đó trình biên dịch Java tự động chuyển đối đối tượng Wrapper thành kiểu dữ liệu cơ bản của nó.
        + khi phương thức chờ đợi là kiệu dữ liệu cơ bản mà giá trị truyền lại là kiểu Wrapper.
        + khi gán giá trị
        + khi xử lý với các lớp tập hợp

### 14. Pass by value and Pass by reference ( truyền giá trị và tham chiếu)
--> trong Java: kiểu dữ liệu nguyên thủy là giá trị ô nhớ, còn kiểu dữ liệu đối tượng thì sẻ ghi nhớ vùng nhớ và tham chiếu đến. vậy nên tham chiếu chỉ suất hiện với đối tượng.

    * Pass by value (truyền giá trị)
    --> khi kiểu dữ liệu truyền là kiểu nguyên thủy

    * Pass by reference (truyền tham chiếu)
    --> khi kiểu dự liệu là kiểu đối tượng

### 15. Instanceof
--> là toán tử kiểm tra kiểu đối tượng của biến. 