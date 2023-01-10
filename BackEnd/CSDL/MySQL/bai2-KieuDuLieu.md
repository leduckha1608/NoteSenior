###### tham khảo link: https://levunguyen.com/co-so-du-lieu-mysql/

1. Kiểu dữ liệu 
   - mỗi cột (column) trong Database đều có kiểu dữ liệu để lưu thông tin về đối tượng. 
   - kiểu dữ liệu chuỗi, số, date

    a. kiểu dữ liệu chuỗi: 
        - Char()        => từ 0-255 ký tự
        - VarChar()     => 0-65535 ký tự
        - Binary()
        - VarBinary()
        - TinyBlob()    => max là 255 bytes
        - TinyText()    => max là 255 ký tự
        - Text()        => max là 65.535 ký tự
        - Blob()        => max là 65.535 bytes
        - MediumText    => max là 16,777,215 ký tự
        - MediumBlob    => max là 16,777,215 bytes
        - LongText      => max là 4,294,967,295 ký tự
        - LongBlob      => max là 4,294,967,295 bytes

    b. kiểu dữ liệu số:
        - Bit           => từ 1-64
        - Tinynt()      => size 0-255
        - Bool          => 0 hoặc 1
        - Boolean       
        - Smallint()    => size 0-65535
        - mediumint()   => size 0-16777215
        - int()         => size 0-4294967295
        - interger()    => 
        - bigint()      => size 0-18446744073709551615
        - float()       => chứa dạng tiền tệ
        - double()

    c. kiểu ngày
        - date          => YYYY-MM-DD
        - datetime      => YYYY-MM-DD hh:mm:ss
        - timestamp     => YYYY-MM-DD hh:mm:ss
        - times         => hh:mm:ss
        - year          => 1901-2155