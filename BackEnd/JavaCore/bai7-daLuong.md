# Đa luồng trong Java

## 1. Đa luồng trong Java (Multithreading)

     * khái niệm về đa luồng trong java
        + đa luồng trong java là một tiến trình thực hiện đa luồng đồng thời.
        + Thread (luồng) là những sub-process (tiến trình con), là đơn vị nhỏ nhất của tiến trình. Multiprocessing and MultiThreading (đa tiến trình và đa luồng) được sử dụng trong Multitasking (đa nhiệm).
    
    * Ưu nhược điểm của đa luồng trong java
        + ko chặn người sử dụng vì luồng là độc lập, có thể thực hiện nhiều công việc cùng 1 lúc.
        + có thể thực hiện nhiều luồng với nhau để tiết kiệm time
        + Luồng là độc lập vậy nên nếu xảy ra ngoại lệ thì nó ko lên quan đến luồng khác.

    * Multitasking (đa nhiệm)
        + Multitasking là quá trình thực hiện hiều nhiệm vụ cùng lúc, chúng ta sử dụng đa nhiệm để tận dụng tính năng của CPU.
            - Đa nhiệm dựa trên Process - Multiprocessing (tiến trình - đa tiến trình)
            - Đa nhiệm dựa trên Thread - multiTheading ( luồng - đa luồng)

        + Đa nhiệm từ Process đến Multiprocessing
            -  

        + Đa nhiệm từ Thread đến MultiTheading

## 2. Vòng đời của Thread 

## 3. Tạo Thread

## 4. 

-----
# Synchronization

--------------------
# 6 Đa luồng
--> Đa luồng trong java là tiến trình thực hiện nhiều luồng đồng thời 
    + tiết kiệm thời gian 
    + các luồng ko bị ảnh hưởng lẫn nhau.

    * vòng đời Thread:
        + new: khời tạo 
        + Runnable: trình biên dịch
        + Running: trình lên lịch và chọn thread 
        + Non-Runnable (blocked): thread vẫn sống nhưng ko được chọn
        + Terminated: ko run() thoát
        + ---------- một số phương thức lớp Thread
        + run()
        + start()
        + sleep()
        + join()
        + getPriority() => trả về mức độ ưu tiên
        + setPriority() => thay đổi mức độ ưu tiên
        + getName() 
        + setName()
        + currentThread() => trả về thread đang được thực thi
        + getId()
        + getState()    => trả về trạng thái
        + isAlive()     => kiểm tra thread còn sống hay ko
        + yield()       => cho phép thread tạm dừng để thread # thực thi
        + suspend()     => hoãn các thread, ko dùng nữa
        + resume()      => tiếp tục thread đang bị hoãn
        + stop()
        + isDaemon()    => kiểm tra nếu thread là một luồng hiểm
        + setDaemon()   => đánh dấu thread là môt luồng hiểm hoặc luồng người dùng
        + interrupt()   => ngắt thread
        + isInterrupt() => kiểm tra thread đã bị ngắt
        + interrupted() => kiểm tra nếu thread hiện tại bị ngắt
        + ------------ 
        + mức độ ưu tin của thread: 
            - min = 1, mặc định = 5, max = 10
            - setPriority: dùng để sét mức độ ưu tiên

        + luồng hiểm (thread Daemon): 
            - luồng gom rác, gom các tài nguyên ko sử dụng để giải phóng bộ nhớ.
            - luồng được đánh dấu bởi phương thực setDaemon(true).
        + thread pool: 
            - gồm nhóm các thread đang chờ đợi công việc, để tái sử dụng nhiều lần. 
            - tiết kiệm thơi gian, ko cần khởi tạo thread mới
            - khởi tạo + call:
                ExecutorService executor = Executors.newFixedThreadPool(5);
                executor.execute(worker);

    * Synchronization:
        - đồng bộ là khả năng kiểm soát nhiều luồng đến bất kỳ nguồn tài nguyên chia sẻ.
        - sychronized  => khối đồng bộ
        - Deadlock     => là bế tắc trong luồng, xảy ra khi cả 2 luồng đều đang chờ đợi giải phóng khóa