# Cảm biến độ ẩm đất điện dung MKE-S13 Capacitive Soil Moisture Sensor
MKE-S13 Capacitive Soil Moisture Sensor là module cảm biến độ ẩm đất sử dụng phương pháp đo điện dung, giúp hạn chế hiện tượng ăn mòn điện cực so với các cảm biến dạng điện trở truyền thống. Nhờ đó, cảm biến có độ bền cao, hoạt động ổn định và cho kết quả đo chính xác trong thời gian dài.

Cảm biến chuyển đổi sự thay đổi điện dung của đất theo hàm lượng nước thành tín hiệu điện áp Analog tuyến tính, giúp các hệ thống vi điều khiển đọc và xử lý dữ liệu theo độ ẩm thực tế thay vì chỉ nhận trạng thái bật/tắt (Digital) như nhiều loại cảm biến phổ biến trên thị trường.

Sản phẩm phù hợp cho nhiều ứng dụng như đo độ ẩm đất, hệ thống tưới cây tự động, vườn thông minh, thiết bị IoT và các dự án STEM. Mạch được thiết kế tối ưu về độ ổn định tín hiệu và khả năng chống nhiễu, đảm bảo độ tin cậy trong cả môi trường học tập và ứng dụng thực tế.

Cảm biến độ ẩm đất điện dung MKE-S13 Capacitive Soil Moisture Sensor hỗ trợ điện áp giao tiếp 3.3V và 5VDC, cho phép kết nối trực tiếp và an toàn với hầu hết các bo mạch điều khiển phổ biến hiện nay như Arduino, Raspberry Pi, Jetson Nano, Micro:bit và nhiều nền tảng khác. Sản phẩm đi kèm cáp kết nối 3P XH2.54 – Dupont, đảm bảo kết nối chắc chắn, ổn định và thuận tiện trong quá trình sử dụng.

## Nguyên lý hoạt động

Cảm biến hoạt động dựa trên sự thay đổi hằng số điện môi của đất theo độ ẩm:
- Khi đất khô: điện dung giảm → điện áp đầu ra thay đổi theo hướng tương ứng.
- Khi đất ẩm: điện dung tăng → điện áp đầu ra thay đổi.

Mạch xử lý trên module sẽ chuyển đổi sự thay đổi điện dung này thành tín hiệu điện áp Analog để đưa vào chân ADC của vi điều khiển, từ đó xác định mức độ ẩm của đất.

## Thông số kỹ thuật
- Điện áp cấp nguồn: 5VDC
- Chuẩn tín hiệu giao tiếp: Analog
- Điện áp giao tiếp: 0~3.3VDC
- Đo độ ẩm đất bằng phương pháp đo điện dung và trả ra giá trị điện áp Analog tuyến tính tương ứng.
- Đầu dò được phủ lớp sơn chống ăn mòn cho độ chính xác, độ bền và độ ổn định cao
- Khả năng tương thích:
  - Arduino
  - Raspberry Pi
  - Jetson Nano
  - Micro:bit
  - Và các board điều khiển 3.3/5VDC khác
- Thiết kế mạch:
  - Ổn định, chống nhiễu
  - Phù hợp cho ứng dụng học tập và thực tế
- Đi kèm cáp kết nối: 3P XH2.54–Dupont

## Các chân tín hiệu
<table><thead>
  <tr>
    <th>MKE-S13</th>
    <th>Ghi chú</th>
  </tr></thead>
<tbody>
  <tr>
    <td>-</td>
    <td>Chân cấp nguồn âm 0VDC</td>
  </tr>
  <tr>
    <td>+</td>
    <td>Chân cấp nguồn dương 5VDC</td>
  </tr>
  <tr>
    <td>S</td>
    <td>Chân tín hiệu Analog Out</td>
  </tr>
</tbody>
</table>

## Hướng dẫn sử dụng
### Hướng dẫn kết nối
- Cấp nguồn 5VDC cho mạch qua hai chân - và +.
- Nhận tín hiệu của cảm biến qua chân S (SIGNAL).
<table><thead>
  <tr>
    <th>SIG (Analog Out)</th>
    <th>Trạng thái</th>
  </tr></thead>
<tbody>
  <tr>
    <td>Max</td>
    <td>3.3VDC</td>
  </tr>
  <tr>
    <td>Min</td>
    <td>0VDC</td>
  </tr>
</tbody>
</table>

### Hướng dẫn sử dụng với Arduino Uno / Vietduino Uno / ESP32
- Trong **Tools / Library Manager**, tìm và cài đặt bộ thư viện tổng hợp **"MKE_ONE" by MakerEdu.vn**
- Mở chương trình mẫu **"MKE_S13_SOIL_MOISTURE_XXX"** tại **File / Examples / MAKEREDU / Module / MKE_S13_SOIL_MOISTURE**
- Cấu hình board mạch tương ứng là **Arduino Uno / ESP32**, chọn đúng cổng **COM Port** của mạch và nhấn **Upload** để nạp chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân S (SIGNAL) của cảm biến với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

### Hướng dẫn lập trình với Micro:bit (kéo thả khối)

- Khởi động [Microsoft MakeCode](https://makecode.microbit.org/) và **Import** chương trình theo đường link sau: `https://github.com/makereduvn/mke_s13_soil_moisture_microbit/`
- Kết nối mạch Micro:bit và **Download** chương trình.
- Cấp nguồn 5VDC cho mạch, kết nối chân S (SIGNAL) của cảm biến với chân điều khiển được khai báo trong chương trình.
- Xem kết quả mạch hoạt động theo chương trình đã nạp.

Nếu bắt đầu tự án mới cần cài đặt Extension **MKE_ONE_MICROBIT** trên [Microsoft MakeCode](https://makecode.microbit.org/) theo [hướng dẫn tại đây](https://github.com/makereduvn/MKE_ONE_MICROBIT). Sau khi cài đặt thành công, các khối lệnh của Extension **MKE_ONE_MICROBIT** sẽ xuất hiện trong danh sách block và sẵn sàng để sử dụng.

## Kích thước sản phẩm
![MKE-S13 SOIL_MOISTURE](/extras/MKE-S13_1.jpg)

## Hình ảnh sản phẩm
![MKE-S13 SOIL_MOISTURE](/extras/MKE-S13_2.png)
![MKE-S13 SOIL_MOISTURE](/extras/MKE-S13_3.png)



