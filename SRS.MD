
# B1. ĐỌC VÀ PHÂN TÍCH YÊU CẦU SƠ KHỞI CỦA KHÁCH HÀNG Ở GIAI ĐOẠN 1

## 1. Tổng quan yêu cầu

Dựa trên tài liệu **“Yêu cầu của khách hàng – Dự án xây dựng hệ thống CAB System – Nền tảng đặt xe”**, Công ty ABC hiện đang cung cấp dịch vụ đặt xe trực tuyến thông qua tổng đài và một ứng dụng đơn giản. Tuy nhiên, hệ thống hiện tại còn tồn tại nhiều hạn chế như việc phân công tài xế chủ yếu được thực hiện thủ công, khách hàng khó theo dõi trạng thái chuyến đi, thông tin thanh toán chưa được quản lý tập trung và hệ thống gặp khó khăn trong việc mở rộng khi số lượng khách hàng và tài xế tăng lên.

Vì vậy, khách hàng mong muốn xây dựng một **nền tảng CAB System mới**, không chỉ đáp ứng nhu cầu đặt xe hiện tại mà còn có khả năng phục vụ số lượng lớn người dùng và hỗ trợ mở rộng thêm các tính năng trong tương lai. Thời gian dự kiến xây dựng và triển khai sản phẩm là **7 tuần**.

## 2. Xác định các tác nhân chính

Qua phân tích yêu cầu sơ khởi, hệ thống có ba nhóm tác nhân chính:

### 2.1. Khách hàng

Khách hàng là người sử dụng dịch vụ đặt xe. Các nhu cầu chính gồm:

* Đăng ký và đăng nhập tài khoản.
* Cập nhật thông tin cá nhân.
* Nhập điểm đón và điểm đến.
* Lựa chọn loại xe.
* Gửi yêu cầu đặt xe.
* Theo dõi trạng thái yêu cầu và chuyến đi.
* Biết tài xế nào đã nhận chuyến và thời gian dự kiến tài xế đến.
* Xem lịch sử chuyến đi và số tiền phải trả.
* Đánh giá tài xế sau khi chuyến đi hoàn thành.

### 2.2. Tài xế

Tài xế là tác nhân trực tiếp thực hiện chuyến xe. Hệ thống cần hỗ trợ:

* Đăng ký tài khoản hoặc được nhân viên vận hành tạo tài khoản.
* Cập nhật hồ sơ và thông tin phương tiện.
* Cập nhật trạng thái hoạt động.
* Chuyển sang trạng thái sẵn sàng nhận chuyến.
* Nhận thông báo khi có chuyến phù hợp.
* Chấp nhận hoặc từ chối chuyến.
* Cập nhật trạng thái chuyến đi.
* Cung cấp thông tin vị trí để hỗ trợ việc tìm tài xế và dự kiến thời gian đến.

### 2.3. Nhân viên vận hành

Nhân viên vận hành chịu trách nhiệm quản lý và hỗ trợ hoạt động của hệ thống. Các chức năng chính gồm:

* Quản lý khách hàng, tài xế và phương tiện.
* Quản lý các chuyến đi.
* Theo dõi các chuyến đang diễn ra.
* Kiểm tra trạng thái tài xế.
* Hỗ trợ xử lý các chuyến bị lỗi.
* Tra cứu lịch sử giao dịch.
* Thực hiện các thao tác quản trị theo quyền được cấp.
* Theo dõi các báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế.

## 3. Phân tích các nhóm yêu cầu chức năng

Từ yêu cầu sơ khởi, có thể xác định các nhóm chức năng chính của CAB System như sau:

### 3.1. Quản lý tài khoản

Hệ thống cần hỗ trợ đăng ký, đăng nhập và cập nhật thông tin đối với khách hàng và tài xế. Người dùng phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản.

### 3.2. Đặt và quản lý chuyến xe

Khách hàng có thể nhập điểm đón, điểm đến, lựa chọn loại xe và gửi yêu cầu đặt xe. Sau khi tạo yêu cầu, khách hàng cần theo dõi được quá trình tìm tài xế, tài xế nhận chuyến, thời gian dự kiến đến và trạng thái chuyến đi.

### 3.3. Tìm kiếm và phân công tài xế

Đây là một trong những chức năng nghiệp vụ quan trọng nhất. Khi có yêu cầu đặt xe, hệ thống cần xác định những tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành khác.

Hệ thống ưu tiên tài xế phù hợp và gần khách hàng. Nếu tài xế được đề xuất không phản hồi hoặc từ chối, hệ thống phải tiếp tục tìm tài xế khác mà không yêu cầu khách hàng tạo lại yêu cầu. Nếu không tìm được tài xế, khách hàng phải nhận được thông báo rõ ràng.

### 3.4. Tính cước và thanh toán

Sau khi chuyến đi hoàn thành, hệ thống cần xác định số tiền khách hàng phải thanh toán dựa trên loại dịch vụ và thông tin chuyến đi.

Hệ thống hỗ trợ hai hình thức thanh toán:

* Thanh toán tiền mặt.
* Thanh toán điện tử thông qua nhà cung cấp thanh toán bên ngoài.

Thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán không được lưu trực tiếp trong hệ thống CAB. Trong trường hợp giao dịch điện tử thất bại, hệ thống phải thông báo cho khách hàng và hỗ trợ xử lý lại theo chính sách của doanh nghiệp.

### 3.5. Hệ thống thông báo

Thông báo được sử dụng để cập nhật trạng thái cho khách hàng và tài xế.

Khách hàng cần được thông báo khi:

* Yêu cầu đặt xe được tiếp nhận.
* Tài xế nhận chuyến.
* Tài xế đến điểm đón.
* Chuyến đi hoàn thành.
* Thanh toán có kết quả.

Tài xế cũng cần nhận thông báo về chuyến mới hoặc những thay đổi liên quan đến chuyến đang thực hiện. Hệ thống cần có khả năng mở rộng thêm các kênh thông báo trong tương lai.

### 3.6. Quản trị và báo cáo

Hệ thống cần cung cấp giao diện quản trị để nhân viên vận hành quản lý các đối tượng và theo dõi hoạt động. Đồng thời, ban lãnh đạo cần có các báo cáo phục vụ việc đánh giá hiệu quả kinh doanh và vận hành, bao gồm số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế.

## 4. Phân tích yêu cầu phi chức năng

Bên cạnh các chức năng nghiệp vụ, khách hàng đặt ra nhiều yêu cầu liên quan đến chất lượng và kiến trúc hệ thống.

### 4.1. Khả năng mở rộng

Hệ thống phải có khả năng phục vụ số lượng lớn khách hàng và tài xế. Khi tải tăng, các thành phần của hệ thống cần có khả năng mở rộng độc lập.

### 4.2. Tính ổn định và khả năng chịu lỗi

Một lỗi xảy ra tại một thành phần, chẳng hạn thanh toán hoặc thông báo, không được làm toàn bộ hệ thống đặt xe ngừng hoạt động.

### 4.3. Khả năng triển khai và phát triển từng phần

Các chức năng mới cần có khả năng được triển khai từng phần, hạn chế ảnh hưởng đến những chức năng đang hoạt động.

### 4.4. Bảo mật

Hệ thống phải:

* Xác thực khách hàng và tài xế trước khi sử dụng các chức năng yêu cầu tài khoản.
* Kiểm soát quyền truy cập đối với các thao tác quản trị.
* Bảo vệ thông tin cá nhân.
* Bảo vệ thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch.
* Lưu vết các thao tác quan trọng để phục vụ kiểm tra khi xảy ra sự cố.

### 4.5. Tính linh hoạt trong tương lai

Kiến trúc hệ thống cần đủ linh hoạt để có thể:

* Bổ sung loại dịch vụ mới.
* Thêm phương thức thanh toán.
* Thêm nhà cung cấp dịch vụ thông báo.
* Thay đổi một số thành phần kỹ thuật.

Các thay đổi trên không nên yêu cầu xây dựng lại toàn bộ ứng dụng.

## 5. Các quy tắc nghiệp vụ sơ bộ

Từ yêu cầu của khách hàng, có thể xác định một số quy tắc nghiệp vụ ban đầu:

1. Tài xế cần ở trạng thái sẵn sàng để có thể nhận chuyến.
2. Hệ thống ưu tiên tài xế phù hợp và gần khách hàng.
3. Nếu tài xế không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác.
4. Khách hàng không cần tạo lại yêu cầu khi hệ thống chuyển sang tìm tài xế khác.
5. Nếu không tìm được tài xế, hệ thống phải thông báo rõ ràng cho khách hàng.
6. Sau khi chuyến đi hoàn thành, hệ thống xác định số tiền khách hàng phải trả.
7. Thông tin thanh toán nhạy cảm không được lưu trực tiếp trong hệ thống CAB.
8. Các chức năng quản trị nhạy cảm phải được kiểm soát bằng cơ chế phân quyền.
9. Các sự kiện quan trọng của chuyến đi và thanh toán cần được thông báo đến các bên liên quan.

## 6. Các vấn đề chưa rõ cần được làm rõ

Qua phân tích, yêu cầu sơ khởi **chưa đủ chi tiết để có thể chuyển ngay sang thiết kế và phát triển hệ thống**. Tài liệu xác định một số vấn đề cần Business Analyst trao đổi thêm với các bên liên quan, bao gồm:

* Cách tính cước cụ thể.
* Tiêu chí ưu tiên tài xế.
* Thời gian tài xế phải phản hồi yêu cầu.
* Chính sách hủy chuyến.
* Cách xử lý khi mất kết nối mạng.
* Thời gian lưu trữ dữ liệu.
* Chính sách xử lý khi thanh toán điện tử thất bại.
* Các tiêu chí vận hành khác được sử dụng trong quá trình tìm và phân công tài xế.

Đây là những nội dung cần được xác nhận trước khi nhóm phát triển xây dựng giải pháp, nhằm tránh việc hiểu sai yêu cầu hoặc phát sinh thay đổi lớn trong quá trình triển khai.

## 7. Đánh giá tổng quan yêu cầu sơ khởi

Qua phân tích, có thể đánh giá yêu cầu sơ khởi của khách hàng đã xác định tương đối rõ **mục tiêu của dự án, các nhóm người dùng, quy trình nghiệp vụ chính, các chức năng cốt lõi và những yêu cầu về bảo mật, ổn định, mở rộng**.

Tuy nhiên, yêu cầu hiện tại vẫn đang ở mức **sơ khởi**, chưa đặc tả đầy đủ các quy tắc nghiệp vụ và trường hợp ngoại lệ. Đặc biệt, các vấn đề liên quan đến tính cước, phân công tài xế, hủy chuyến, mất kết nối và lưu trữ dữ liệu vẫn cần được xác nhận với khách hàng. Do đó, vai trò của Business Analyst ở giai đoạn tiếp theo là rất quan trọng trong việc thu thập thông tin, xác định phạm vi, làm rõ yêu cầu và chuyển các yêu cầu ban đầu thành những yêu cầu có thể kiểm chứng và triển khai.

## 8. Kết luận

Từ yêu cầu sơ khởi, nhóm xác định **CAB System không chỉ là một ứng dụng đặt xe mà được định hướng trở thành một nền tảng có khả năng vận hành và mở rộng lâu dài**. Hệ thống phải hỗ trợ xuyên suốt quy trình từ tạo yêu cầu đặt xe, tìm và phân công tài xế, thực hiện chuyến, tính cước, thanh toán, thông báo đến đánh giá sau chuyến.

Bên cạnh việc đáp ứng nhu cầu của khách hàng, hệ thống còn phải hỗ trợ bộ phận vận hành quản lý tập trung, cung cấp dữ liệu phục vụ theo dõi hoạt động và đảm bảo các yêu cầu về bảo mật, ổn định, khả năng mở rộng và phát triển trong tương lai. Vì vậy, trước khi chuyển sang giai đoạn thiết kế và phát triển, nhóm cần tiếp tục làm rõ các điểm chưa xác định với khách hàng để đảm bảo yêu cầu được hiểu thống nhất giữa **khách hàng – Business Analyst – nhóm phát triển**.


