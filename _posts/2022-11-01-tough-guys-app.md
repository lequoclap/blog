---
title: "TOUGH GUYS NEVER DIE -  TẠO APP QUẢN LÝ GROUP CHALLENGES SỬ DỤNG STRAVA API"
date: 2022-11-01
---

TLDR;

Như các bạn đã biết (hoặc chưa biết) thì app Strava là 1 app rất tiện lợi và hoàn toàn miễn phí để tracking vận động nên nó là app không thể thiếu với những người mê chạy bộ, đạp xe, bơi lội.

Và app Strava có một chức năng rất hay đó là Group challenges để nhiều người có thể tham gia, nôm na thì nó là 1 cái dashboard để hiển thị kết quả của nhiều người 1 lúc, có mục tiêu chung và sẽ tính tổng quãng đường chạy được của tất cả thành viên.

// Ảnh

Điều rất không hay ở đây là với tài khoản miễn phí, mỗi user chỉ được join vào 3 challenge trong vòng 1 năm. Mà với sự "cuồng nhiệt trong thể thao" và sự "tiết kiệm trong tiền bạc" mình không chấp nhận được sự thật này.

Vì vậy vào 1 ngày cuối tuần rảnh rỗi (thực ra là 2), vợ bị covid phải cách ly không cho lại gần thì mình đã nhân cơ hội trời cho này tạo 1 cái app dashboard đơn giản cho group đạp xe của mình. Mình lấy tên app là **Tough Guys Never Die** - cái tên nói lên đúng (1 nửa) sự cuồng nhiệt thể thao của nhóm. 

Mình chia các yêu cầu theo thứ tự ưu tiên như sau

## Yêu cầu tối cần thiết

- Phát triển nhanh
- Mất ít tiền duy trì server

## Yêu cầu chính:

- Sử dụng Strava API để lấy dữ liệu activities của nhiều user.
- Tổng hợp và show ra dashboard.
- Dễ dàng regist, login.

## Yêu cầu phụ

- Bảo mật tốt
- Tính khả dụng cao


Các bước tiếp cận

## Kiểm tra API, có yêu cầu cần thiết gì không

- Cần đăng ký app trên Strava.com
- Authenticate sử dụng Auth 2.0
- Có API để lấy all activities by athele
- Quote: giới hạn 150 requests/day


## Architect Design



## Phân tích yêu cầu

Như các bạn thấy, vì làm 1 app side project và muốn sử dụng luôn và ngay nên mình ưu tiên phong cách mì ăn liền, làm nhanh gọn lẹ, và tất nhiên mình không muốn mất quá nhiều tiền và công sức cho việc duy trì và phát triển app. 
Vì app chỉ sử dụng nội bộ do đó traffic cũng không quá nhiều, vì vậy mình chọn phát triển serverless app, code và build app lên AWS Lambda.
AWS Lambda là 1 service khá hay để host backend resouces, nó sẽ tính tiền dựa vào lượt sử dụng. Vì vậy bạn không cần phải thuê và duy trì server hằng tháng.

Về giao diện Front end mình sẽ code ASP app sử dụng Angular và host trên S3, dịch vụ lưu trữ dữ liệu S3 của AWS cũng rất chi là rẻ.


//Ảnh


Nhìn chung thì app sẽ như thế này

// S3 -> Lambda



// S3 -> Cloud front -> 





## Design UI

## Code

## Deploy / Auto Deploy


