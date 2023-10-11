# DebuggingDemo
122. Debugging Intro

122. Giới thiệu gỡ lỗi

Gỡ lỗi là quá trình xác định và sửa lỗi hoặc khiếm khuyết trong chương trình máy tính. Đó là một kỹ năng cần thiết đối với mọi lập trình viên vì trong quá trình phát triển, lỗi và hành vi không mong muốn là không thể tránh khỏi. Các công cụ và kỹ thuật gỡ lỗi giúp bạn xác định và khắc phục những vấn đề này trong mã của mình. Dưới đây là phần giới thiệu tổng quan về gỡ lỗi trong C#:

1. **Các loại lỗi**:

    - **Lỗi thời gian biên dịch**: Những lỗi này xảy ra trong quá trình biên dịch và khiến chương trình của bạn không được xây dựng. Các ví dụ phổ biến bao gồm lỗi cú pháp, thiếu tham chiếu hoặc kiểu dữ liệu không chính xác.

    - **Lỗi thời gian chạy**: Những lỗi này xảy ra khi chương trình đang chạy và có thể khiến chương trình bị lỗi. Các ví dụ bao gồm các ngoại lệ tham chiếu null, lỗi chia cho 0 và lỗi chỉ mục ngoài phạm vi.

    - **Lỗi logic**: Đây là những lỗi khó xác định nhất vì mã chạy không có lỗi nhưng không tạo ra kết quả như mong đợi. Việc tìm ra lỗi logic đòi hỏi sự hiểu biết sâu sắc về logic của chương trình.

2. **Công cụ gỡ lỗi**:

    - **Môi trường phát triển tích hợp (IDE)**: Hầu hết các IDE hiện đại, bao gồm Visual Studio và Visual Studio Code, đều cung cấp các công cụ gỡ lỗi mạnh mẽ. Những công cụ này cho phép bạn đặt điểm ngắt, duyệt từng bước mã, kiểm tra các biến, v.v.

    - **Điểm dừng**: Việc đặt điểm dừng trong mã của bạn cho phép bạn tạm dừng quá trình thực thi chương trình tại các điểm cụ thể. Điều này là vô giá để hiểu những gì đang xảy ra tại thời điểm đó và tại sao.

    - **Xem Windows**: Công cụ gỡ lỗi thường bao gồm cửa sổ xem nơi bạn có thể thêm các biến để theo dõi. Khi bạn xem qua mã của mình, các cửa sổ này sẽ cập nhật theo thời gian thực, hiển thị các giá trị thay đổi.

    - **Ngăn xếp cuộc gọi**: Ngăn xếp cuộc gọi hiển thị cho bạn chuỗi các cuộc gọi phương thức dẫn đến điểm hiện tại trong mã của bạn. Điều này có thể giúp bạn hiểu chương trình của bạn đạt đến trạng thái hiện tại như thế nào.

    - **Đầu ra/Windows ngay lập tức**: Bạn có thể in thông báo hoặc đánh giá các biểu thức trong các cửa sổ này để kiểm tra trạng thái chương trình của bạn mà không cần thay đổi mã.

    - **Xử lý ngoại lệ**: Công cụ gỡ lỗi có thể phát hiện các ngoại lệ và cho phép bạn kiểm tra chi tiết ngoại lệ. Bạn cũng có thể đặt trình gỡ lỗi ở trạng thái ngắt khi có ngoại lệ được đưa ra.

3. **Kỹ thuật gỡ lỗi**:

    - **Đặt điểm dừng**: Đặt điểm dừng ở các dòng mã cụ thể mà bạn nghi ngờ có thể xảy ra sự cố. Khi chương trình của bạn đạt đến điểm dừng, bạn có thể kiểm tra các giá trị biến và duyệt qua mã.

    - **Bước qua**: Bạn có thể duyệt qua từng dòng mã của mình, thực thi mã đó và xem các hiệu ứng. Sử dụng "Step Into" để thực hiện các cuộc gọi phương thức.

    - **Điểm dừng có điều kiện**: Bạn có thể đặt điểm dừng chỉ kích hoạt khi đáp ứng một điều kiện nhất định. Điều này rất hữu ích khi bạn cần điều tra một tình huống cụ thể.

    - **Kiểm tra biến**: Trong khi gỡ lỗi, bạn có thể kiểm tra giá trị của biến. Điều này giúp bạn xác định các giá trị không chính xác hoặc không mong muốn.

    - **Ghi nhật ký**: Việc thêm câu lệnh nhật ký vào mã của bạn có thể giúp bạn theo dõi quá trình thực thi mã và tìm ra điểm xảy ra sự cố. Sử dụng các thư viện như log4net hoặc Microsoft.Extensions.Logging.

    - **Kiểm tra đơn vị**: Viết bài kiểm tra đơn vị có thể giúp bạn xác định sớm các vấn đề trong quá trình phát triển và cung cấp mạng lưới an toàn cho các thay đổi mã. Việc kiểm tra đơn vị gỡ lỗi có thể dễ dàng hơn vì chúng tách biệt các phần cụ thể trong mã của bạn.

4. **Các tình huống gỡ lỗi phổ biến**:

    - **Ngoại lệ tham chiếu null**: Những ngoại lệ này thường xảy ra khi bạn cố truy cập một thành viên hoặc phương thức trên một đối tượng null. Đặt điểm ngắt nơi ngoại lệ được đưa ra để xác định tham chiếu null.

    - **Lỗi logic**: Sử dụng điểm ngắt để kiểm tra các giá trị biến và luồng của chương trình nhằm xác định logic không chính xác trong mã của bạn.

    - **Vòng lặp vô hạn**: Sử dụng trình gỡ lỗi để dừng vòng lặp vô hạn và kiểm tra các điều kiện dẫn đến kết thúc vòng lặp.

    - **Vấn đề về hiệu suất**: Công cụ lập hồ sơ có thể giúp xác định các điểm nghẽn về hiệu suất trong mã của bạn.

5. **Các phương pháp hay nhất**:

    - Bắt đầu gỡ lỗi với sự hiểu biết rõ ràng về vấn đề. Tái tạo vấn đề và hiểu bối cảnh của nó trước khi bạn bắt đầu.

    - Sử dụng kiểm soát phiên bản để theo dõi các thay đổi và hoàn nguyên về trạng thái hoạt động đã biết nếu cần.

    - Giữ cho cơ sở mã của bạn sạch sẽ và được tổ chức tốt để giảm nguy cơ xảy ra lỗi.

    - Sử dụng tên biến có ý nghĩa và viết nhận xét mang tính mô tả.

    - Thường xuyên kiểm tra mã của bạn khi bạn phát triển. Thử nghiệm nhỏ, tăng dần có thể ngăn chặn việc gỡ lỗi phức tạp.

Gỡ lỗi là một kỹ năng được cải thiện nhờ thực hành. Càng có nhiều kinh nghiệm, bạn càng trở nên giỏi hơn trong việc xác định vấn đề và khắc phục chúng một cách hiệu quả.

123. Debugging Basics

123. Cơ bản về gỡ lỗi

Gỡ lỗi là một kỹ năng cần thiết đối với bất kỳ lập trình viên nào. Đó là quá trình tìm và sửa lỗi (bug) trong mã của bạn. Trong C#, bạn có thể sử dụng Môi trường phát triển tích hợp (IDE) như Visual Studio hoặc Visual Studio Code, cung cấp các công cụ sửa lỗi mạnh mẽ. Dưới đây là một số vấn đề cơ bản về gỡ lỗi trong C#:

1. **Đặt điểm dừng**:
   
    - Điểm ngắt là một điểm trong mã của bạn nơi trình gỡ lỗi sẽ tạm dừng việc thực thi chương trình.
    - Bạn có thể đặt điểm dừng bằng cách nhấp vào lề trái của trình soạn thảo mã bên cạnh dòng bạn muốn ngắt.
    - Bạn cũng có thể đặt điểm dừng bằng phím tắt. Ví dụ: trong Visual Studio, F9 đặt điểm ngắt.

2. **Bắt đầu gỡ lỗi**:

    - Để bắt đầu gỡ lỗi, bạn thường có thể nhấn F5 hoặc sử dụng nút "Bắt đầu gỡ lỗi" trong IDE của mình.
    - Thao tác này sẽ xây dựng và chạy chương trình của bạn ở chế độ gỡ lỗi và chương trình sẽ dừng ở bất kỳ điểm dừng nào bạn đã đặt.

3. **Kiểm soát gỡ lỗi**:

    - Khi trình gỡ lỗi đã tạm dừng chương trình của bạn, bạn có một số điều khiển để duyệt qua mã:
   
      - **Bước vào (F11)**: Điều này cho phép bạn bước vào lệnh gọi phương thức hoặc hàm. Nếu dòng hiện tại chứa lệnh gọi phương thức, F11 sẽ đưa bạn vào phương thức đó.
     
      - **Bước qua (F10)**: Thao tác này cho phép bạn chuyển sang dòng tiếp theo. Nếu dòng hiện tại chứa lệnh gọi phương thức, F10 sẽ thực thi toàn bộ phương thức và dừng ở dòng tiếp theo.
     
      - **Bước ra (Shift+F11)**: Thao tác này cho phép bạn thoát khỏi phương thức hiện tại và quay lại người gọi.
     
      - **Tiếp tục (F5)**: Điều này cho phép bạn tiếp tục chạy chương trình cho đến điểm dừng tiếp theo hoặc cho đến khi điểm dừng đó kết thúc.

4. **Kiểm tra các biến**:

    - Trong khi gỡ lỗi, bạn có thể kiểm tra giá trị của các biến.
    - Bạn có thể di chuột qua một biến để xem giá trị của nó hoặc có thể thêm biến để xem cửa sổ.
    - Trong Visual Studio có cửa sổ Watch và cửa sổ Locals để kiểm tra các biến.
   
5. **Các loại điểm ngắt**:

    - Bạn có thể đặt các loại điểm dừng khác nhau:

      - **Điểm dừng thông thường**: Những điểm dừng này tạm dừng thực thi tại dòng được chỉ định.
      - **Điểm dừng có điều kiện**: Những điểm này chỉ tạm dừng quá trình thực thi nếu điều kiện được chỉ định là đúng.
      - **Điểm dừng đếm lượt truy cập**: Điểm dừng này sẽ tạm dừng thực thi sau một số lần truy cập nhất định.
      - **Điểm dừng ngoại lệ**: Những điểm này tạm dừng khi một ngoại lệ cụ thể được đưa ra.

6. **Gỡ lỗi ngoại lệ**:

    - Khi một ngoại lệ chưa được xử lý được ném ra, trình gỡ lỗi có thể ngắt dòng gây ra ngoại lệ đó.
    - Bạn có thể định cấu hình hành vi này trong IDE của mình.

7. **Đầu ra gỡ lỗi**:

    - Bạn có thể viết tin nhắn vào đầu ra gỡ lỗi bằng cách sử dụng 
`System.Diagnostics.Debug.WriteLine("message")`.
    - Những thông báo này sẽ xuất hiện trong cửa sổ đầu ra gỡ lỗi.

8. **Gỡ lỗi tương tác**:

    - Một số IDE, như Visual Studio, cho phép gỡ lỗi tương tác. Điều này có nghĩa là bạn có thể thay đổi giá trị biến trong khi gỡ lỗi để xem tác động lên chương trình của mình.
   
9. **Các tình huống gỡ lỗi phổ biến**:

    - **Ngoại lệ tham chiếu null**: Những ngoại lệ này có thể được giải quyết bằng cách kiểm tra xem các biến có rỗng hay không và bằng cách kiểm tra biến nào là null khi ngoại lệ được ném ra.

    - **Lỗi logic**: Sử dụng điểm ngắt để kiểm tra các giá trị biến và hiểu luồng chương trình của bạn.

    - **Vòng lặp vô hạn**: Đặt điểm dừng trong vòng lặp để kiểm tra các biến vòng lặp. Điều này sẽ giúp bạn tìm ra điều kiện cần thay đổi để vòng lặp kết thúc.

10. **Mẹo gỡ lỗi**:

     - Bắt đầu với sự hiểu biết rõ ràng về vấn đề bạn đang cố gắng giải quyết.
     - Cô lập vấn đề bằng cách thu hẹp vấn đề vào một đoạn mã cụ thể.
     - Sử dụng kiểm soát phiên bản để theo dõi các thay đổi.
     - Ghi lại quá trình gỡ lỗi, đặc biệt khi làm việc với các vấn đề phức tạp.

Hãy nhớ rằng gỡ lỗi là một kỹ năng sẽ được cải thiện khi thực hành. Càng gỡ lỗi nhiều, bạn càng có thể xác định và khắc phục các vấn đề trong mã của mình tốt hơn.
