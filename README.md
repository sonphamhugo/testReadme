# TIVI Android API

API cho phép người dùng từ client app lấy danh sách tivi (đã chứa link play từ server).

Cho phép Tool tivi submit, update, delete danh sách tivi.

## LƯU Ý:

Tất cả request đều dùng có thể pass qua clientkey ở mục body bằng key cứng :"tivi.devteam0903@gmail.com"

Hoặc clientkey đc tạo ra iệc mã hóa MD5 chuỗi thời gian hiện tại (không lấy giây) ở muối giờ Europe/London

có dạng : MD5(currentMilisecondAtLondon()) 

với dateTime format = "YYYY-mm-dd HH:ii"

Muốn chỉnh sửa clientkey vào đường dẫn: application/core/public_controller.php

Hàm checkClientKey()

## Chú thích thông số: 

| Tên                   | Loại dữ liệu      | Mô tả |
| ----------------------|:-----------------:| -----:|
| id                    | int               | ID của tivi. VD: 123 |
| categoryName          | string            | Tên của thể loại tivi. VD: Bóng đá  |
| thumbnail             | string            | Link logo hình ảnh tivi. VD: https://lh3.googleusercontent.com/-u3tR0eMNeio/Vm0xFIaAhDI/AAAAAAAAANE/4FjjIHd80Vs/h120/vtc7.png ![IMAGE ALT TEXT HERE](https://lh3.googleusercontent.com/-u3tR0eMNeio/Vm0xFIaAhDI/AAAAAAAAANE/4FjjIHd80Vs/h120/vtc7.png)|
| channelName           | string            | Tên kênh tivi: vtv3-hd |
| idfpt                 | string            | id của tivi trên fpt dùng để check lịch tivi |
| position              | int               | vị trí của tivi trong group: VD: 1 |
| linkPlay              | string            | link play của tivi chứa *.m3u8. VD: http://123.30.185.126/hls/vtc3.m3u8|
| isLock                | bool              | khóa tivi, tivi bị khóa sẽ được mở bằng cách cài app. VD  true|
| create_at             | long              | thời gian tạo dữ liệu. VD: 1492070724500|
| last_activity         | long              | thời gian tương tác lần cuối dữ liệu. VD: 1492070724500|
