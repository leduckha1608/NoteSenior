############https://viblo.asia/p/luong-di-trong-spring-boot-ORNZqdELK0n


### 1 luồng đi trong String boot
--> Spring boot được dự trên 2 mô hình là MVC và 3 lớp
    * Mô hình 3:
        + Presentation: tầng tương tác người dùng
        + Busines: tầng logic
        + Data access: tầng tương tác database
    * Mô hình MVC
        + Model, view, controller
    * Spring boot
        + Controller: tầng API, tương tác với view
        + Service:  tầng logic
        + Repository: tương tác với database
### 2 Dependency Injection
--> 
    * Module coupling:
    --> Mối quan hệ giữa 2 module,2 đối tượng, có sự phụ thuộc lẫn nhau.
        + Tight coupling: module liên kết chặt chẽ, khó tách rời.
        + Loose coupling: liên kế yếu rời rạc
        => Đễ code dễ bảo trì và sử đổi , thì phải giảm sự phụ thuộc giữa các module. Nghĩa là biến đổi mối quan hệ từ (Tight coupling) thành (Loose coupling).

    * Nguyên lý DI:
    -->
        + Các module cấp cao ko phụ thuộc trực tiếp vào module cấp thấp. Cả 2 nên phụ thuộc vào Abstraction(của OOP).
        + Abstraction ko nên phụ thuộc vào chi tiết, mà ngược lại.

    * Inversion of Control (IoC):
    --> là đảo ngược điều khiển, giúp thay đổi luồng điều khiển của chương trình một cách linh hoạt. Mục đích nhằm giảm quá trình tạo đối tượng và liên kết giữa chúng.
    
        + Ioc Container: tạo ra 1 đối tượng, lắp ráp chúng với nhau, cấu hình và quản lý vòng đời cho đến khi hủy.

    * Dependency Injection:
    --> là một kỷ thuật theo đó 1 đối tượng được cung cấp các phụ thuộc với các đối tượng #
        + DI Container: là chỉ các thành phần tạo và quản lý module/object được Inject.

    ==> IoC của Spring được gọi là ApplicationContext
    ==> Các module chúng các IoC Container gọi là các Bean.

### 3 Bean và ApplicationContext
    * Bean: 
    --> Bean là những module chính của chương trình, được tạo và quản lý với Spring IoC Container.

    * ApplicationContext:
    --> đại diện cho các dependency, dùng chỉ các Spring IoC container.
    Khi ứng dụng Spring chạy, các Spring IoC container sẻ quét toàn bộ package tìm các bean và đưa chúng vào trong ApplicationContext. gọi là cơ chết component Scan.
        + lấy bean ra từ ApplicationContext -> dùng getBean()
        + Inject bean và trong bean khác: @Autowired, hoặc constructor, setter.
    
    ** khi có nhiều bean:
        + có thể  @Primary để ưu tiên
        + hoặc @Qualifier("VNEngine") để loại bean ko phù hợp


### 4 Vòng đời, các loại bean, cơ chế ComponentScan
--> vòng đời của bean là từ khi bean được khởi tạo đến khi chết đi.
    gồm các bước:
        + IoC container tìm thấy Bean cần quản lý, và khởi tạo bằng Constructor
        + Inject Dependencies và Bean bằng Setter, và thực hiện các cài đặt khác
        + @PostConstruct dùng để thực hiện một số task khi khởi động bean
        + @PreDestroy dùng để dọn dẹp Bean ko dùng xong, khi ko dùng nữa.

    * các loại Scope trong Bean:
        + Singleton: tạo ra duy nhất một lần với mỗi object từ class bean. 
        + Prototype: tạo ra một thể mới của bean mỗi khi cần thiết
        + request:  tạo theo request
        + session:  tạo theo session
        + Global session: theo mỗi global session

### 5 Cấu trúc dự án SpringBoot
### 6 Entity, domain model, DTO
### 7 ModelMapper trong SpringBoot
--> dùng để convert lại 2 object có cấu trúc gần giống nhau

### 8 Xử lý request
    * Controller:
        + @Controller: trả về View qua một String hoặc Json data trong response body.
        + @RestController: trả về data trong response body. thích hợp cung cấp API.
        ==> @RestController = @Controller + @responseBody.

    * các method HTTP:
    --> 
        + @GetMapping
        + @PostMapping
        + @PutMapping
        + @DeleteMapping

    * các request Data HTTP:
        + RequestHeader
        + RequestParam
        + PathVariable 
        + RequestBody

    * Response HTTP:
    --> gồm: status, header, body.


### 9 Xử lý Exception
--> @RestControllerAdvice hoặc @ControllerAdvice. được dùng để bắt các Exception
    + các exception sẻ được chuyển tới method @ExceptionHandler sử lý.

### 10 Xử lý vadidation
--> được sử lý ở DTO, dùng @Valid để kiểm tra vadidation.
        + @NotEmpty
        + @NotNull
        + @Email
        + @Min ...

    * có 2 cách sử lý khi xãy ra vadidation.
        + dùng BindingResult:
            vẫn cho method gọi vào, nhưng xử lý bằng cách ném ra một throw new Exception với nội dung của vadidation.
        + dùng ExceptionHandler:

--------------------một số câu hỏi thường gặp 

### AOP ( Aspect Oriented Programming ) 

* Là một mẫu lập trình làm tăng tính module bằng các cho phép phân tác các mối quan tâm xuyên suốt,
 cho phép thêm các hành vi bổ sung cho vào đoạn code mà ko cần chỉnh sửa tới đoạn code.
 
* sửa dụng AOP, cần xác định các chứng năng chung ở một nơi. 
 
1. Các thuật ngữ:
 + Aspect: là một module đóng gói các Advice và các poincut và cúng cấp tính xuyên suốt.
 + Pointcut: là một biểu thức chọn 1 hoặc nhiều điểm nối ( join poin) nơi advice được thực thi.
 + Join poin: là điểm trong ứng dụng nơi chúng ta áp dụng AOP
 + Advice: là một hành động mà chúng ta thực hiện trước hoặc sau khi thực hiện method
 + Target object: đối tượng được các device sử dụng. luôn là một proxy
 + Weaving: là tiến trình nối các aspect với object,ty
 + Proxy: dùng để cài đặt các Aspect
 + Introduction: cho phép các introduce vác new interface tới bất kì các object advice nào.
 + Interceptor: là một aspect chỉ có duy nhất một advice.

 
IoC:
DI:

