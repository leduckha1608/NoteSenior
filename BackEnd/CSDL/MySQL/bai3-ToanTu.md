###### tham khảo link: https://levunguyen.com/co-so-du-lieu-mysql/

1. toán tử trong Database gồm

    a. toán tử tính toán: +, -, *, /, %

    b. toán tử Bitwise: 
        &: AND  => khi cả 2 đều đúng
        |: OR   => khi 1 trong 2 hoặc cả 2 đều đúng
        ^: XOR  => khi 1 đúng 1 sai

    c. toán tử so sánh: 
        =: bằng
        >: lớn hơn
        <: nhỏ hơn
        >=: nhỏ hơn hoặc bằng
        <=: lớn hơn hoặc bằng
        <>: ko bằng

    d. toán tử kết hợp
        +=: thêm giá trị bằng
        -=: giảm giá trị bằng
        *=: nhân giá trị bằng
        /=: chia giá trị bằng
        %=: mod giá trị bằng
        &=: And giá trị bằng

    e. toán tử logic
        All: được sử dụng để so sánh một giá trị với tất cả các tập hợp giá trị khác. trả về true khi giá trị đúng với tất cả các giá trị trong tập hợp.

        Any: được sử dụng để so sánh một giá trị với tất cả các tập hợp giá trị khác. trả về true khi giá trị đúng với 1 giá trị trong tập hợp.

        And: tồn tại trong mệnh đề Where, là true khi các điều kiện đều là true.

        Between: là giá trị thỏa mãn nằm trong khoảng [min, max].

        Exists: trả về true nếu câu lệnh con tìm kiếm có tồn tại giá trị

        In: so sánh giá trị với danh sách giá trị văn bản chỉ định.

        Like: được sử dụng để so sánh giá trị với các giá trị tương tự, sử dụng toán tử ký tự đại diện(wildcard)

        Not: toán tử phủ định

        OR: được sử dụng để kết hợp nhiều điều kiện Where

        is null: so sánh với null

        Unique: là rằng buộc, các giá trị là duy nhất trong cột. (ví dụ: Email)




----------------------------note 
nên tìm hiểu thêm về mệnh đề like: https://viettuts.vn/sql/menh-de-like-trong-sql