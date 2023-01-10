 https://www.tutorialspoint.com/cobol/cobol_program_structure.htm

### 1. Cobol  Enviroment setup

### 2. program Structure
-->  Program -> Divisions -> sections -> paragraphs -> sentence -> statements -> characters

    * Sections: là khu vực quản lý logic chương trình. mỗi Sections gồm nhiều paragraphs

    * Paragraphs: là phần chia nhỏ của một phần hoặc bộ phận. là tên do người dùng xác định hoặc tên được xác định từ trước.

    * sentences: là kết hợp của một hoặc nhiều câu. các câu chỉ xuất hiện trong bộ phận thủ tục. một câu phải kết thúc bằng 1 khoảng thời gian

    * statements:  là các câu lệNh trong Cobol có ý nghĩa xử lý

    * characters: hệ thống cấp phát cú pháp mà 

    * Divisions:(bộ phận) một chương trình Cobol gồm 4 phần

        + Identification Division: nhận biết

        + Environment Division: môi trường
            - Configuration section: cung cấp thông tin hệ thống mà program viết
                -- Source computer: hệ thống sử dụng trình biên dịch
                -- Object computer: hệ thống sử dụng để thực thi chương 

            - Input-Output section: cung cấp thông tin các tệp được sử dụng in program
                -- File control: cung cấp thông tin của bộ dữ liệu ngoài được sử dụng in program.
                -- IO control: cung cấp thông tin các tập tin sử dụng in program


        + Data Division: chia dữ liệu dùng để định nghĩa các biến biến sử dụng in program
            - File section: sử dụng để xác định cấu trúc bản ghi
            - Working-Storage section: khai báo biến tạm thời và cấu trúc tệp được sử dụng
            - Local-Storage section: biến local
            - Linkage section: sử dụng để mô tả tên của một chương trình bên ngoài

        + Procedure Division: (thủ tục) phân chi thủ tục để sử dụng hàm logic in program. bao gồm các câu lệnh thực thi.




### 3. Basic Sytax
    * Character Set:
        + chữ cái A-Z, a-z
        + chữ số 0-9
        + toán tử +,-,*,/,%
        + ...
    * Coding Sheet
        + 

### 4. Data Types (phân chia dữ liệu)
--> phân chia dữ liệu đượC sử dụng để xác đỊnh các biến được sử dụng in a program. gồm các thuật ngữ. 

    Level Number    Data Name   Picture Clause  Value Clause
    01              ToTal       PIC9(5)         Value '123'

    * Data name: (Tên dữ liệu)   được xác định in Bộ phận dữ liệu trước khi sử dụng khai báo

    * Level Number:    
        + 01:           Record description entry
        + 02 to 49:     Group and Elementary items
        + 66:           Rename Clause items
        + 77:           Items which cannot be sub-divided
        + 88:           Condition name entry


    * Picture Clause
    -->     Data type - Sign - Decimal point position - length

        + Symbols:
             9 Numeric  (số)
             A Alphabetic   (chữ cái)
             X Alphanumeric ( chữ và số)
             V Implicit Decimal (số thập phân tiềm ẩn)
             S Sign     (dấu hiệu)
             P Assumed Decimal  (số thập phân giả định)


    * Value Clause
    --> mệnh đề giá trị là một mênh đề tuỳ chọn được sử dụng để khởi tạo các mục dữ liệU.

### 4.1 Basic Verbs (động từ)
--> Input/ output verbs được sử dụng để lấy dữ liệu người dùng và hiện thị đầu ra của chương trình

    * Input/Output Verbs 
        +Accept verb:
        --> được sử dụng để lấy dữ liệu. nếu chương trình đang chấp nhận dữ liệu từ người dùng thì nó chần chuyển qua JCL.
            - syntax:   ACCEPT WS-STUDENT-NAME
                        ACCEPT WS-DATE FROM SYSTEM-DATE                

        +Display Verb
        --> được sử dụng để hiển thị một cobol
            - syntax:  "hello: " DISPLAY WS-STUDENT

    * Initialize Verb
    --> từ khởi tạo được sử dụng để tạo nhóm hoặc 1 mục cơ bản.
    
        + được viết trong PROCEDURE DIVISION , thường dùng với REPLACING
        + syntax:   INITIALIZE WS-ID REPLACING NUMERIC DATA BY 123.

    * Move Verb:
    --> dùng để sao chép dữ liệu từ nguồn sang đích.
        + syntax:   MOVE 123 to MS-NUM1
                    MOVE MS-NUM1 to MS-NUM2

    * Add Verb 
    --> dùng để cộng 2 hoặc nhiều số trả về kết quả 
        + syntax:   ADD A B TO C D

                    ADD A B C TO D GIVING E

                    ADD CORR WS-GROUP1 TO WS-GROUP2  // gián trường tên giống nhau 

    * Subtract Verb 
    --> dùng để thực hiện phép từ 2 hoặc nhiều số 
        + syntax:   SUBTRACT A B FROM C D

                    SUBTRACT A B C FROM D GIVING E

                    SUBTRACT CORR WS-GROUP1 TO WS-GROUP2

    * Multiply Verb
    --> dùng để nhân 2 hoặc nhiều số
        + syntax:   MULTIPLY A BY B C

                    MULTIPLY A BY B GIVING E

    * Divide Verb
    --> dùng để chia 
        + syntax:   DIVIDE A INTO B

                    DIVIDE A BY B GIVING C REMAINDER R
    
    * Compute Statement
    --> được dùng để tính toán , áp dụng các phép tính toán học


### 4.2 Data layout
--> bố cục là mô tả về việc sử dụng từng trường và các giá trị trong đó.

    * Redefines Clause (xác định mệnh đề)

    * Renames Clause (tên mệnh đề)

    * Usage Clause  (điều khoản sử dụng)

    * Copybooks     (sách sao chép)

### 5. Conditional Statements (câu lệnh điều kiện)
--> Các câu lệnh điều kiện được sử dụng để thay đổi luồng chương trình thực thi

    * IF condition statement
        + IF ELSE END-IF
    
    * Relation condition (điều kiện quan hệ)
        Equal to (=)
        Greater than (>)
        Less than (<)
        Greater than or Equal (>=)
        Less than or equal (<=)
        Positive (tích cực) / Negative (từ chối) / Zero (0)

    * Sign Condition (dấu hiệu điều kiện)
        [IS] điều kiện thoả mản
            - WS-NUM IS NUMERIC (khi WS-NUM đúng kiểu dữ liệu là NUMERIC )  
        [NOT]  khi điều kiện không thoả mãn

    * Class condition ( lớp quan hệ)
        + Các kiểu loại Class condition
            - NUMRIC    
            - ALPHABETIC
            - ALPHABETIC-LOWER
            - ALPHABETIC-UPPER

    * Condition-Name Codition
    --> điều kiện là tên do người dùng định nghĩa. Nó chứ 1 tập hợp các giá trị chỉ định bởi người dùng. mặc định level number là 88. 
        - 88 [Condition-Name] value [is, Are] [literal] [thru literal]
        


    * Negated Condition ( phủ định quan hệ) 
        + IF NOT


    * Combined Condition ( kết hợp )
        + AND , OR

### 6. Loop Statements
--> các tác vụ được thực hiện lặp.

    * Perform Thru  (lặp lại số các câu lệnh 1 lần)
    --> được sử dụng để thực hiện một chuỗi lặp từ giá trị đầu đến cuối 1 lần
        + syntax:   PREFORM PARAGRAPH1 THRU PARAGRAPH2

    * Perform Until (lặp đến khi nào)
        + các mã code sẽ được thực hiện đến khi nào điều kiện là trả về đúng.
        + syntax: 
            - perform A-para Unil count = 5.
            - perform A-para With Test Before Until count = 5.
            - perform A-para With Test After Until count = 5.

    * Perform  Times (thực hiện số lần chỉ định)
        + syntax:
            - preform A-para 5 times.


    * Perform  Varying (thực hiện đến khi nào đúng)
        + syntax: 
            preform A-para Varying a from 1 by 1 until A = 5.

    * Go To Statement 
    --> thay đổi luồng thực hiện của chương trình.

### 7. String Handling
--> các câu lệnh trong Cobol được sử dụng để thực hiện nhiều thao tác chứ năng chuỗi. 

    * Inspect 
    --> tự động kiểm tra được sử dụng để đếm  hoặc thay thế các ký tự trong chuỗi.

        + Tallying (dùng để đếm)
            - syntax:   
                        INSPECT input-string
                        TALLYING output-count FOR ALL CHARACTERS
                        => giá biến output-count = giá trị số lượng ký tự của input-string

        + Replacing (thay thế)
            - syntax:   INSPECT input-string REPLACING ALL char1 BY char2.
            => hiểu là trong chuỗi input-string thì thay thế chuỗi con char1 bằng chuỗi con char2 

    * String 
    --> là một động từ dùng để nối các chuỗi
            + syntax: 
                        STRING ws-string1 DELIMITED BY SPACE 
                        ws-string2 DELIMITED BY SIZE
                        ws-string3 DELIMITED BY 'a'
                        INTO ws-result
                        WITH POINTED ws-count 
                        ON OVERFLOW DISPLAY mess1
                        NOT ON OVERFLOW DISPLAY mess2
                        END-STRING.
            => String sẻ gộp 3 chuỗi ws-string1, ws-string2, ws-string3 và gán vào ws-result. gán tổng độ dài vào ws-count. và kiểm tra với độ dài mảng ws-result, để trả về thông báo mess1 hoặc mess2.
            => BY SPACE, BY SIZE, BY 'a' là điều kiện cắt chuỗi.
            => mess1 , mess2 là những thông báo có thể thiếu.

    * Unstring
    --> dùng để tách chuổi thành nhiều chuỗi nhỏ hơn 
            + syntax:
                        UNSTRING ws-string DELIMUTED BY SPACE 
                        INTO ws-string 1, ws-string2
                        WITH POINTER ws-count
                        ON OVERFLOW DISPLAY mess1
                        NOT ON OVERFLOW DISPLAY mess2
                        END-UNSTRING.



### 8. Table Processing (sử lý bảng)
--> Mảng là một cấu trúc dữ liệu tuyến tính và tập các mục kiểu dữ liệu riêng lẽ cùng loại. Các mục dữ liệu của 1 bảng được sắp xếp bên trong.

    * Table Declaration trong Data Division. mệnh đề được sử dụng để định nghĩa một bảng. cấp bậc được đánh số từ 02 - 49
        + syntax:   
            01 ws-table
                05 ws-abc5 PIC A(10) OCCURS 3 TIMES
        => bằng ws-table có 10 đối tượng ws-abc
    
    * two-dimensional Table
        + syntax:
            01 ws-table
                05 ws-abc5 PIC A(10) OCCURS 3 TIMES.
                    10 ws-abc10-1 A(10). 
                    10 ws-abc10 PIC (10) OCCURS 2 TIMES.
    
    * Subscript
    --> các phần tử riêng lẻ của bảng được truy cập bằng cách sử dụng chỉ số index.
        + syntax:   
                WORKING-STORAGE SECTION.
                    01 WS-TABLE.
                        05 WS-A OCCURS 3 TIMES.
                            10 WS-B PIC A(2).
                            10 WS-C OCCURS 2 TIMES.
                                15 WS-D PIC X(3).
                ---được sử dụng--- 
                DISPLAY 'WS-A(1)   : ' WS-A(1).
                DISPLAY 'WS-C(1,1) : ' WS-C(1,1).
                DISPLAY 'WS-C(1,2) : ' WS-C(1,2).
                DISPLAY 'WS-A(2)   : ' WS-A(2).
         => có thể gọi WS-C(1,2) để gọi giá trị tại địa chỉ [1,2]  

    * Index 
    --> các phần thử được truy nhập bằng cách đánh chỉ mục gán INDEXED BY
        + syntax:
                01 WS-TABLE.
                    05 WS-A PIC A(10) OCCURS 10 TIMES INDEXED BY I.
        => chỉ số I được đánh số theo mảng

    * Set Statement
    --> câu lệnh Set được sử dụng để thay đối giá trị chỉ mục, động từ Set được dùng để khởi tạo, tăng hoặc giảm chỉ mục. được dùng để tìm kiếm và tìm kiếm tất cả các phần tử trong bảng.  
        + syntax:   SET I J TO 4
                    SET I TO J
                    SET I J UP BY 1
                    SET J DOWN BY 2

    * Search 
    --> phương pháp tìn kiếm tuyến tính, dùng để tìm các phần tử bên trong bảng.
        + syntax:
                SET I TO 1.
                SEARCH WS-A
                    AT END DISPLAY 'not M'
                    WHEN WS-A(I)='M'
                    DISPLAY 'M true'
                END-SEARCH.  
        => tìm kiếm bảng WS-A, tới hết mà ko thấy thì hiển thị 'not M ' còn nếu có thì in câu lệnh 'M true'.

    * Search All
    --> một phương pháp tìm kiếm nhị phân được sử dụng để tìm các phần tử bên trong 
        + syntax:
                SEARCH ALL WS-RECORD
                AT END DISPLAY 'RECORD NOT FOUND'
                WHEN WS-NUM(I) = 93
                DISPLAY 'RECORD FOUND '
                DISPLAY WS-NUM(I)
                DISPLAY WS-NAME(I)

### 9. File Handling
--> là những thuật ngữ cơ bản, để hiểu việc xử lý tệp trong Cobol

        * Field (trường)
            --> trường được sử dụng để chỉ ra dữ liệu được lưu trữ về 1 phần tử. gồm các thuộc tính, đại diện cho 1 yếu tố duy nhất.
            +  Primary key
            +  Secondary keys
            +  Descriptors ( các trường mô tả thực thể)

        * Record (bản ghi)
            --> bản ghi là một tập hợp các trường được sử dụng để mô tả thực thể.

        * Physical Record
            --> bản ghi vật lý

        * Logical Record
            --> bản ghi logic, là bản ghi có thể xử lý tại bất kỳ thời điểm nào

        * File
            --> là tập hợp các bản ghi

### 10. File Organization (tổ chức file)
    * Sequential file organization (tổ chức file tuần tự)
    --> bản ghi được lưu trữ và truy cập theo thứ tự tuần tự.
        + được đọc tuần tự, nếu muốn đọc bản ghi thứ 10 phải đọc 9 bản ghi trước
        + được viết tuần tự, bản ghi mới ko chèn vào giữa, và phải chèn vào cuối
        + ko thể xoá,ko thay đối kích thước, ko thay đổi thứ tự
        + có thể đè khi độ dài là giống nhau.

        + syntax:   INPUT-OUTPUT SECTION.
                    FILE-CONTROL.
                    SELECT file-name ASSIGN TO dd-name-jcl
                    ORGANIZATION IS SEQUENTIAL

    * Indexed sequential file organization (tổ chức file tuần tự có chỉ mục)
    --> được lập chỉ mục gồm các bản ghi có thể truy cập tuần tự hoặc trực tiếp.

        + gồm 2 phần:
            - Data File chứa các bản ghi trong lược đồ tuần tự
            - Index File chứa khoá chính và địa chỉ của nó trong tệp dữ liệu

        + tính chất:
            - Các bản ghi có thể đọc theo thứ tự tuần tự
            - có thể truy cập ngẫu nhiên nếu biến khoá chính
            - chỉ mục được sắp xếp duy trình ko lên quan đến giá trị khó và vị trí bản ghi trong tệp
            - chỉ mục thay thế cũng có thể được tạo để tìm nạp các bản ghi

        + syntax:
            INPUT-OUTPUT SECTION.
            FILE-CONTROL.
                SELECT file-name ASSIGN TO dd-name-jcl
                ORGANIZATION IS INDEXED
                RECORD KEY IS primary-key
                ALTERNATE RECORD KEY IS rec-key
            

    * Relative file organization (tổ chức tệp tương đối)
    --> Tệp tương đối bao gồm các bản ghi được sắp xếp tương đối
        
        + tính chất:
            + các bản ghi có thể đọc tuần tự và cũng được lập chỉ mục
            + có thể truy nhập bằng các từ khó tương đối. (khoá biểu thị vị trí bản ghi so với địa chỉ bắt đầu của tệp)
            + các bản ghi có thể chèn bằng khoá tương đối ( địa chỉ tương đối được tính bằng khó tương đối)
            + tệp cung cấp quyền ưu cập nhanh nhất vào các bản ghi
            + nhược điểm là các bản ghi trung gian nếu bị thiếu cũng sẻ chiếm dung lượng.

        + syntax:
                INPUT-OUTPUT SECTION.
                FILE-CONTROL.
                    SELECT file-name ASSIGN TO dd-name
                    ORGANIZATION IS RELATIVE
                    RELATIVE KEY IS rec-key


### 11. File Access Mode (chế độ truy cập file)
--> Đối với mỗi sơ đồ các tổ chức tệp, có thể sử dụng các chế độ truy cập khác nhau

    * Sequential Access (truy cập tuần tự)
    --> chế độ truy cập là tuần tự 
        + đối với tệp tuần tự: các bản ghi được truy cập theo thứ tự chúng chèn vào
        + đối với tệp được lập chỉ mục: tham số sử dụng để tìm nạp bản ghi là các giá trị khoá của bản ghi
        + đối với các tập tương đối: các khoá bản ghi tương đối được sử dụng để truy xuất các bản ghi
        + syntax:
            ENVIRONMENT DIVISION.
            INPUT-OUTPUT SECTION.
            FILE-CONTROL.
                SELECT file-name ASSIGN TO dd-name
                ORGANIZATION IS SEQUENTIAL
                ACCESS MODE IS SEQUENTIAL
	
	
            ENVIRONMENT DIVISION.
            INPUT-OUTPUT SECTION.
            FILE-CONTROL.
                SELECT file-name ASSIGN TO dd-name
                ORGANIZATION IS INDEXED
                ACCESS MODE IS SEQUENTIAL
                RECORD KEY IS rec-key1
                ALTERNATE RECORD KEY IS rec-key2

		
            ENVIRONMENT DIVISION.
            INPUT-OUTPUT SECTION.
            FILE-CONTROL.
                SELECT file-name ASSIGN TO dd-name
                ORGANIZATION IS RELATIVE
                ACCESS MODE IS SEQUENTIAL
                RELATIVE KEY IS rec-key1


    * Random Access ( truy cập ngẫu nhiên) // để note sau
    * Dynamic Access ( truy cập tự động)    // để note sau

### 12. File Handling Verbs
--> Các động từ xử lý tệp được sử dụng thực hiện các thao tác khác nhau trên tệp. 

    * Open verb
    --> thao tác thực hiện đầu tiên được thực hiện để mở file
        + syntax: OPEN "mode" file-name

        + từ khoá:
            - Input: chế độ đầu vào được sử dụng cho các tệp hiện có
            - Output: chế độ đầu ra được sử dụng để chèn các bản ghi vào tệp.
            - Extend: chế độ mở rộng được sử dụng để nối thêm các bản ghi.
            - I/O: được sử dụng để đọc và ghi các bản ghi của 1 tệp


    * Read verb
    --> động từ đọc được sử dụng để đọc các bản ghi tệp, chức năng của Read để tìm nạp các bản ghi từ 1 tệp. 
        + Syntax:

    * Write verb
    --> động từ ghi được sử dụng để chèn các bản ghi vào 1 tệp. sau khi bản ghi được ghi, nó ko còn sản trong bộ nhớ đệm, nên trước khi chèn các bản ghi, hãy di chuyển các giá trị vào bộ nhớ đệm

    * Rewrite verb (viết lại)
    * Delete
    * Start
    * Close
### 13. Subroutines (chương trình con)
--> chương trình con Cobol là chương trình có thể biên dịch và độc lập nhưng ko thể thực thi độc lập.

    * Call verb
    --> động từ được sử dụng để chuyển hướng điều khiển từ chương trình này sang chương trình khác. 
        + Các ràng buộc chương trình:
            - phần tử liên kết phải được xác định trong chương trình được gọi.
            - chia thủ tục sử dụng danh sách các biến được truyền từ chương trình gọi và thứ tự phải giống nhua đề cập nhât trong gọi tự động
            - câu lệnh thoát chương trình phải được sử dụng trong chương trình gọi lại để điều kiển trở lại.
        + Các tham số có thể truyền giữa các chương trình theo 2 cách:
            - By Reference
            - By Content

    * Call By Reference
    --> Nếu giá trị của các biến trong chương trình được gọi bị sử đổi thì giá trị mới của chúng sẻ phản ánh trong chương trình gọi.

    * Call by Content 
    --> Nếu giá trị của các biến trong chương trình được gọi bị sửa đổi, thì giá trị mới của chúng ta ko phản ánh trong chương trình gọi.

    * Types of Call 
        - Static call:
        - Dynamic call:

### 14. internal Sort (sắp xếp nội bộ)
--> sắp xếp dữ liệu trong 1 tệp, hoặc hợp nhất các tệp. có thể sắp xếp theo tăng dần hoặc giảm dần.

    + có 2 kỹ thuật đưỢc sử dụng để sắp xếp trong Cobol
        - External sort (sắp xếp bên ngoài): tiện ích sort của JCL, ít dùng
        - internal sort ( sắp xếp bên trong): 
    
    * Sort Verb:  
        + Input file: là tệp phải sắp xếp theo thứ tự tăng hoặc giảm dần.
        + Work file: được sử dụng để giữ các bản ghi trong quá trình sắp xếp đang diễn ra
        + Output file: là tệp sau quá trình đã sắp xếp.
        +syntax:
            SORT work-file ON ASCENDING KEY rec-key1
            [ON DESCENDING KEY rec-key2]
            USING input-file GIVING output-file.

    * Merge Verb (hợp nhất)
    --> Hai hoặc nhiều tệp có trình tự giống hết nhau, có thể kết hợp bằng cách sử dụng hợp nhất
        + tệp công việc ở chế độ I-O, tập đầu vào là INPUT và đầu ra là OUTPUT
        + chuyển các bản ghi trong tệp thứ 1 sang tệp công việc 
        + sắp xếp SORT-FILE theo trình tự tăng dần/ giảm dần bằng phím rec-key
        + chuyển các bản ghi đã được sắp xếp trừ tệp công việc sang tệp đầu ra
        + đóng tệp đầu vào và tập đầu ra và xoá tệp công việc.
        + syntax:
            MERGE work-file ON ASCENDING KEY rec-key1
            [ON DESCENDING KEY rec-key2]

USING input-1, input-2 GIVING output-file.

### 15. database interface
