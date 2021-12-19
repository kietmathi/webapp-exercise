# webapp hiển thị doanh số bán xe của 1 số công ty ở 1 số quốc gia

### data
- sử dụng data tại file car-sales.json

### yêu cầu
- url: localhost:8000/sales?continent=[continent được input]&company=[company được input]
  - param continent và company là optional
  - trường hợp input param nào thì get data ứng với param đó tại car-sales.json
    - VD: 
      - chỉ input param continent thì get data có giá trị tương ứng
      - chỉ input param company thì get data có giá trị tương ứng
      - input cả continent và company thì get data có giá trị continent và company tương ứng
  - trường hợp không input bất kỳ param nào thì get toàn bộ data tại car-sales.json
- output
  - trường hợp tồn tại data thì hiển thị data ra view như mô tả tại 1/
    - các record tại table được hiển thị ở view sẽ sắp xếp theo thứ tự sales giảm dần
  - trường hợp không tồn tại data thì hiển thị message ra view thông báo rằng không tồn tại data
  - trường hợp phát sinh error thì hiển thị message ra view với nội dung là err.Error()
  - Về hiển thị của trường hợp không tồn tại data và trường hợp phát sinh error như mô tả tại 2/
 ![](https://github.com/kietmathi/webapp-exercise/blob/main/car-sales/DD-demo-template.png)
