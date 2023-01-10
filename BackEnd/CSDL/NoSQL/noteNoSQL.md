###### tham khảo: https://itguru.vn/blog/co-so-du-lieu-nosql-la-gi-va-tat-ca-nhung-gi-can-biet-ve-nosql-database/
 https://viblo.asia/p/nosql-va-nhung-dac-tinh-khac-biet-m68Z0RMj5kG


# 1: định nghĩa:
---> noSQL là một hệ thống quản lý dữ liệu ko quan hệ có lược đồ linh hoạt. dễ mở rộng. 
    + mục đích là dành cho các kho dữ liệu phân tán với nhu cầu lưu trữ dữ liệu lớn
    + được sử dụng cho web thời gian thực.
    + gồm: 
        Column: bảng với hàng và cột thay đổi
        Graph: nodes và cạnh
        key-value: 
        Document: JSON documents

# 2. đặc điểm:
    * High scalability: Lượng dữ liệu có thể quản lý ko bị giới hạn bởi hệ thống
    * High Availability: Chấp nhận dư thừa dữ liệu, khả năng chịu lỗi cũng cao hơn CSLD.
    * Atomicity: trạng thái dữ liệu độc lập mỗi khi diễn ra thay đổi.
    * Consistency: tính nhất quán, tính đúng đắn có thể mất sau 1 khoảng thời gian cập nhật.
    * Durability: dữ liệu tồn tại trong bộ nhớ nhưng đồng thời cũng lưu lại ở ổ đĩa.
    * Deployment Flexibility: hệ thống tự động nhận biết và lưu trữ thay đổi các node. 
    * Modeling flexibility: dữ liệu lưu dưới nhiều dạng.
    * Query flexibility: linh hoạt trong truy vấn, bằng việc load một tập giá trị dự vào một dãy các key.

# 3. Các kiểu dữ liệu

    * Key-value: dữ liệu được lưu trữ dưới dạng key/value.
        + thiết kế theo cách để xử lý nhiều dữ liệu và tải nặng
        + lưu trữ dưới dạng bảng băm, key duy nhất và value có thể là Json hoặc blob(Binary large Objects)
        => giới hạn của Key-value trong noSQL:
            + ko có mối quan hệ giữa các khóa
            + lưu trữ nhiều khóa, ko lưu trữ 1 khóa
            + tìm kiếm khóa dựa trên thông tin được tìm thấy của phần giá trị 'key/value'.
            + các hoạt động được giới hạn ở 1 khóa, tại một thời điểm. ko thể chạy đồng thời nhiều khóa.
        => thường dùng trong: DynamoDB, Redis, Riak, Berkeley DB

        
    * Column-based: dữ liệu được lưu dưới dạng cột, mỗi cột được sử lý riêng biệt, giá trị của csdl cột đơn được lưu liền kề
        + hiệu suất cho truy vấn tổng hợp: SUM, COUNT, AVG, MIN, MAX
        +  được sử dụng để quản lý data warehouse, business intelligence, CRM, Libary card catalogs...
        => giới hạn Column-base trong noSQL:
            + cần nhiều thời gian để ghi dữ liệu
            + cần nhiều để đọc dữ liệu
        => thường dùng trong: Hbase, Cassandra, Hypertable


    * Document-Oriented: dữ liệu dưới dạng key/value, nhưng phần giá trị dưới dạng tài liệu. Tài liệu dưới dạng JSON hoặc XML
        +
        => giới hạn Document-oriented: 
            + thông tin có thể trùng lặp trên nhiều tài liệu
            + thiết kế phức tạp, ko có tính nhất quán.
        => thường dùng trong: Mongo DB, Amazon simpleDB, CouchBD, Riak, Lotus Notes.

    * Graph-Based: dữ liệu kiểu đồ thị lưu trữ thực thể cũng như mối quan hệ giữa các thực thể.
        + thực thể lưu dưới dạng note, quan hệ lưu dưới dạng cạnh
        + mỗi cạnh là mối quan hệ giữa các note
        + mỗi note và cạnh đều có mã đích danh duy nhất.
        => giới hạn Graph-Basd:
            + thiếu tính đồng thời hiệu suất cao
            + thiếu ngôn ngữ chuẩn
            + thiếu tính song song
        => thường dùng trong: Infinite Graph, OritentDB, FlockDB, Neo4J, Giraph

# 4. hạn chế trong noSQL
    + No Schema
    + ko nhất quán
    + sự phụ thuộc lỏng lẽo
    

