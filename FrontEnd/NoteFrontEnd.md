##### https://viblo.asia/p/bo-cau-hoi-phong-van-intern-fresher-cho-front-end-tu-a-z-Do754rgVZM6
note những câu hỏi thường gặp 

### 1 HTML5
    * <!doctype html> 
        => khai báo trình duyệt web biết website đang sử dụng ngôn ngữ đánh dấu.

    * thẻ meta: 
        + cung cấp thông tin của website cho công cụ tìm kiếm. 
    
    * HTML sematic:
    --> sử dụng các thẻ thích hợp cho ý nghĩa của nó.

        + <section>: dùng để phân chia các phần riêng biệt 
        + <article>: chứa các nội dung động lập trong trang
        + <nav>: dùng chứa các thẻ <a> dẫn tới các nội dung chính của website
        + <aside>: lưu thông tin bên lề nội dung
        + <main>: nội dung chính
        + <div>: ko có ý nghĩa. chỉ dùng dể nhóm. có thể thay đôi CSS chung.
        + <header> <footer> thẻ thông tin giới thiệu trang.

    * HTML5 nâng cấp: 
        + thêm mới một số thẻ sematic
        + đa nền tảng + responsive + hỗ trợ tốt hơn , nhiều layout elements hơn.
    
    * DOM trong HTML
    --> đại diện cho websive

    * thẻ div và thẻ Span:
        + div: là thẻ block, nhóm các thẻ block với nhau
        + span: là thẻ inline, gom các thẻ inline với nhau.
        ==> block, inline là giá trị của thuộc tính display

### 2 CSS
    * Các viết CSS:
        + Inline: viết trực tiếp
        + internal: viết tại thẻ Head
        + External: việt 1 file là link vào.
    
    * Flex box và Grid: 
    
    * Position:
    --> thuộc tính position xác định vị trí tương đối và tuyệt đối cho các thành phần, vị trí này phụ thuộc và các giá trị khai báo của thành phần và thành phần bao ngoài nó.
        + relative: định vị, vị trí tương đối cho các thành phần, khi sử dụng thuộc tính này thành phần sẻ đinh vị theo mốc vùng hiển thị của chính nó.
        + absolute: định vị, vị trí tuyệt đối cho các thành phần theo phần bao ngoài. vùng không gian thành phần sẻ biến mất
        + fixed: định vị, vị trí tuyệt đối với vùng hiễn thị của trình duyệt
        + static: dạng mặc định, các thành phần nằm theo thứ tự của văn bản
        + stiky: bám dính
    **tham khảo: https://topdev.vn/blog/tim-hieu-thuoc-tinh-position-trong-css/

    * Box-sizing: border-Box
    --> cho phép set lại một border. 
        + khi thêm các thuộc tính padding cho các phần tử thì kích thước ban đầu bị tăng lên, box-sizing ngăn chặn điều đó.
    
    * Model box:
        + Content: phần nội dung
        + Padding: phần đệm
        + Border: căn viền
        + Margin: phần dịch chuyển

    * Responsive
    --> là tối ưu giao diện người dùng, cho từng thiết bị Mobile, tablet, desktop. dùng thẻ @media
        

### 3 JavaCript
    * DOM : 
    * phân biệt var, let, const
        - var là global, let và const thuộc block {}.
        - var có thể update và khai báo lại được, let update ko khai báo lại được, const ko update ko khai báo lại.
    * Hoisting:
        - Hoisting là cơ chế mặc định của JavaScript để di chuyển tất cả các biến và hàm khi khai báo lên đầu scope trước khi chúng được thực thi.

    * tham chiếu, tham trị 
        - tham trị chứa giá trị như Number, String, Boolean
        - tham chiếu chưa địa chỉ như Array, Object

### 4 ES6
    * variables
        + thêm biến let, vậy là có 3 cách khai báo biến là var, let, const.

    * default parameters: cho phép tham số mang giá trị mặc định hoặc ko có giá trị 
        + trong khai báo: function multiply(a, b = 1) ; // mặc định b = 1 khi ko truyền tham số.
        + bên trong function:  name = name || "Guess"; 
    
    * Spread syntax:
        + cho phép lặp lại phần tử của mảng (Array) hoặc đối tượng (Object)
        + cú pháp là ... : const newArray = [...oldArray, 4, 5];  // ...oldArray là mảng có sẳn.

    * Rest parameters:
        + tham số còn lại, là tham số đại diện không được khai báo
        + function number(num1, num2, ...numOther)

    * Destructuring(phá vỡ cấu trúc): cho phép ta thay đổi cấu trúc của Array hoặc Object.

    * arrow function: viết dạng mũi tên =>

    * Classes: 
        + Classes là một dạng function đặc biệt, thay vì sử dụng function, ta dùng class + constructor();
        + Classes có thể kế thừa: extends
        + có thể dùng từ khóa this để trỏ vào 
    * export & import:
        + export để file chấp nhận việc xuất các funtion
        + import để liên kết với file export

--------------------------------

######## Angular

### 1 cơ chế hoạt động:
    + load index.html
    + nạp thư viện
    + load file main.ts 
    + load module
    + load compoment

### 2 Data Binding
    * One way binding: dữ liệu truyền 1 chiều , () gọi funtion, [] truyền biến.
    * Two way binding: dữ liệu truyền 2 chiều => [()]
    => dùng để đồng bộ với html.

### 3 Thêm component con:
    --> khai báo tại module. vì module quản lý

### 4 Directive
--> là các thao tác trên web, thao tác trên element của DOM.
    + ngFor 
    + ngIf 
    + ngModel 
    + ngClass 
    + ngStyle 

### 5 truyền dữ liệu:
    * cha xuống con: 
        + @Input(): 
        + @ViewChild():
    
    * từ con lên cha:
        + @Output(): 
        + @ViewChild():

    * thông qua service, trong module chứ cả 2 component

### 6 vòng đời