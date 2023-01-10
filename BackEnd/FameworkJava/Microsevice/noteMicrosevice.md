###### tham khảo: https://topdev.vn/blog/phat-trien-phan-mem-theo-kien-truc-microservice/
https://vietnix.vn/microservices-la-gi/
https://itnavi.com.vn/blog/microservices-la-gi

### Mô hình Microsevice

# 1. Microsevice:
--> microsevice là một mô hình được ứng dụng trong  phát triển hệ thống phần mềm. dựa vào việc tập chung xây dựng các module chức năng với giao diện, và hoạt động được xác định rõ ràng.
    + giải quyết vấn đề khó khăn của hệ thống nguyên khối bằng cách modul hóa.
    
    * Microservice architecture:
        + chia theo dịch vụ thành phần
        + hoạt động giống Unix: nhận request, xử lý, tạo phản hồi.
        + 

    * 6 điều cần tuân thủ khi thiết kế kiến trúc Microsevice
        + 1 service là có phạm vi và chức năng giới hạn.
        + các service theo chức năng nghiệp vụ cụ thể.
        + đảm bảo tính độc lập từng module
        + thiết kế theo nghiệp vụ, ko theo đơn giản các nghiệp vụ
        + kích thước service phải đáp ứng được chức năng của hệ thống
        + ko nên quá nhiều hàm hay chức năng hỗ trợ xung quanh, định dạng thông báo đơn giản

### API Gateway
--> là cổng chung gian và duy nhất để tới hệ thống microsevice. 
    + api Gateway nhận các request từ client, chỉnh sửa, xác thực điều hướng tới các API cụ thể phía service.
    + api gateway thường đảm nhiệm luôn vai trò khác như: bảo mật, monitoring(giám sát), analytics(phân tích) số lượng request cũng như tình trạng hệ thống.
    
    * lợi ích của việc sử dụng API Gateway:
        + che giấu kiến trúc với hệ thống
        + phần code fontend đẹp
        + dễ dàng theo dõi và quản lý tranffic(lưu lượng dữ liệu)
        + Request caching + cân bằng tải.
        + thêm lớp bảo vệ bảo mật
        + thay thế authentication service.

    * các bước tạo API Gateway:
        + List các API public
        + Implement API bên phía Gateway, có thể là (forward/composite/aggregate) tùy thuộc mục đích.
    
    * Pros & Cons
    ----->ưu
        + Decrease MSA complexity (giảm độ phức tạp)
        + Cross-cutting concern (mối quan tâm xuyên suốt)
        + Protocol translating (phương thức giao dịch)
    ----->nhược
        + Latency: độ trễ
        + Single-point failure: fail 1 điểm là có thể gây là lỗi luồng và nút cổ chai
        + Cost: mất phí
        + Complexity: giảm độ phức tạp implement , nhưng tổng thể hệ thống ko ko.
        + Security: khi có 1 điểm hở (sai xót trong quá trình implement) có thể gây ra là toàn bộ Services đều bị tấn công.

    * Backend for Frontend(BFF)
    ---> communication pattern phổ biến:
        + Direct call: FE gọi trực tiếp
        + API Gateway: có một API Gateway đứng giữa FE và BE
        + BFF: vẫn là API Gateway đứng giữa, nhưng có nhiều gateway.

    * yếu tố nên sử dụng API gateway: 
        + dự án ko quá lớn thì ko cần dùng
        + timeline
        + Team skill

    * After credit
        --> sau khi chốt phương án sử dụng API gateway thì có 2 hướng: build và buy.
            + Kong Gateway: 
            + Cloud Gateway:
### Các mô hình Microsevice