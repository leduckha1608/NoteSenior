### String trong Java

### 1. String là gì
--> String là một đối tượng biểu diễn 1 chuổi các giá trị char. cung cấp các method thao tác với chuỗi.

    + implement: Serializable, Comparable và CharSequence
    + có tính đối tượng, so sánh tính toán, biểu diễn chuỗi.
    + khởi tạo bằng new hoặc nháy kép
    + String được lưu vào vùng nhớ đặc biệt (Pool) gọi là hằng số chuỗi => giúp tiết kiệm vùng nhớ
    + String có tính bất biến

    * các phương thức String
        + ChartAt( int index)
        + length()
        + format(String format, Object args)
        + substring(int beginIndex)
        + contains(charSequence s)  / kiểm tra chuỗi có chứ s ko
        + join( CharSequence delimiter, CharSequence...elements) / nối nhiều chuỗi, có delimiter là ký tự nối
        + equals(Object o)
        + isEmpty()
        + concat(String s)  / nối chuỗi cụ thể
        + replace(char old, char new)   / thay đổi giá trị old bằng giá trị new
        + equalsIgnoreCase  / so sánh chuỗi ko phân biệt chữ Hoa
        + split     / trả về các chuỗi tách ra theo regex
        + intern()  / trả về chuỗi từ Pool.
        + int indexOf(String s)   / trả về vị trí chuỗi chứ s
        + toLowerCase   / trả về chuỗi chữ thường
        + toUpperCase   / trả về chuỗi chữ hoa
        + strim()       / loại khoảng trống đầu và cuối chuỗi
        + valueOf(int value)    chuyển đối kiểu dữ liệu đã cho thành chuỗi

    * so sánh chuỗi
        + s1==s2 / so sánh bằng toán tử ==, kiểu so sánh kỹ thuật 
        + s1.equals(s2) so sánh bằng giá trị value
        + so sánh bằng CompareTo()


### 2. String Buffer và String Builder
--> StringBuffer, StringBuild được sử dụng để tạo chuỗi có thay đổi được (mutable)
        + implement: Serializable, CharSequence, Appendable 

    * StringBuffer: 
        + được sử dụng để tạo ra chuỗi có thể thay đổi được (do String bị hạn chế tính bất biến)
        + có tính đồng bộ, luồng an toàn. 
        + phương thức đều là synchronized 

    *String Builder
        + giống Buffer là có thể thay đổi
        + ko có tính đồng bộ , có thể truy nhập đồng thời

    * các phương thức: 
        + append(String s) -- dùng để nối thêm s vào chuỗi
        + insert(int offset, String s) -- chèn s vào vị trí offset của chuỗi
        + replace(int start, int end, String s) -- thay thế s cho vị trí từ start đến end.
        + reverse() -- đảo ngược chuỗi
        + capacity() -- dung lượng hiện tại
        + ensureCapacity() -- dung lượng tối thiểu
        + chartAt(int index) -- trả về value tại vị trí index
        + length()  
        + substring() -- trả về chuỗi con 



