# webapp hiển thị total doanh số bán xe của 1 số công ty

### data
- sử dụng data tại file car-sales.json

### yêu cầu
- url: localhost:8000/sales?company=[company được input]
  - company là optional
  - trường hợp input company nào thì get data ứng với company đó tại car-sales.json
  - trường hợp không input bất kỳ param nào thì get data của toàn bộ công ty tại car-sales.json
- output
  - trường hợp tồn tại data thì hiển thị sales total của công ty ra view như mô tả tại 1/
    - VD: công ty A có data sales tại JP, US và US tương ứng với 3, 1 và 2 thì sales total sẽ là 3 + 1 + 2 = 6
  - trường hợp không tồn tại data thì hiển thị message ra view thông báo rằng không tồn tại data
  - trường hợp phát sinh error thì hiển thị message ra view với nội dung là err.Error()
  - Về hiển thị của trường hợp không tồn tại data và trường hợp phát sinh error như mô tả tại 2/
  - Khi click vào công ty sẽ di chuyển đến trang sales detail của công tại các chi nhánh như mô tả ở 3/
    - Về chart sẽ là barchart
    - Data vẽ chart là tỉ lệ % giữa sales tại chi nhánh và sales total
      - VD: sales tại chi nhánh JP là 3 và sales total là 6 -> data vẽ chart là 50
    - Về URL của trang sales detail thì tự quyết định
    - Trường hợp phát sinh lỗi thì xử lý tương tự như mô tả tại 2
 ![](https://github.com/kietmathi/webapp-exercise/blob/main/car-sales2/DD-demo-template2.png)
