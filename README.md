# SERVICE ORIENTED ARCHITECTURE

Đồ án môn học: **Kiến trúc hướng dịch vụ**
Giảng viên hướng dẫn: [**Dương Hữu Phúc**][dhp]

Thành viên tham gia:

-   Phạm Nguyễn Hoàng Quân - 51900419
-   Nguyễn Minh Phước - 51900770

## Giới thiệu đề tài

-   Tên đề tài: **TÌM HIỂU VÀ PHÂN TÍCH PHÂN HỆ QUẢN LÝ ĐƠN HÀNG TỪ THỰC KHÁCH**
    Hệ thống quản lý thông tin sinh viên của sinh viên đóng vai trò hết sức quan trọng
    đối với hoạt động của các trường đại học, cao đẳng, ... Hệ thống thông tin sinh viên
    là một hệ thống cung cấp các dịch vụ, công cụ và tài nguyên để quản lý thông tin
    liên quan đến sinh viên trong một trường đại học hoặc các tổ chức giáo dục khác.
    Việc triển khai hệ thống thông tin sinh viên giúp trường đại học quản lý dữ liệu sinh
    viên một cách chính xác và hiệu quả, từ đó giảm thiểu tình trạng nhầm lẫn và tránh
    việc bị mất thông tin quan trọng. Hệ thống quản lý sinh viên giúp giảng viên và nhân
    viên quản lý trường có thể dễ dàng truy cập và cập nhật thông tin sinh viên một
    cách chính xác và nhanh chóng. Bên cạnh đó cũng giúp sinh viên quản lý thông tin
    cá nhân, đăng ký học phần, xem thời khóa biểu và kiểm tra điểm số để dễ dàng quản
    lý việc học tập. Hệ thống cung cấp các chức năng cơ bản như quản lý thông tin sinh
    viên, quản lý lớp, quản lý điểm, quản lý môn học và các chức năng phục vụ việc học
    tập như xem thời khóa biểu, đăng ký kế hoạch học tập, đăng ký môn học, ...

## Những tính năng chính

• Đăng nhập/Đăng xuất
• Quản lý nhân viên
• Quản lý hóa đơn
• Quản lý đơn hàng
• Quản lý menu
• Thanh toán
• Báo cáo và thống kê

## Ảnh màn hình

## Công nghê sử dụng

Công nghệ sử dụng cho việc xây dụng hệ thống API BACK-END:

-   [Node.js] - evented I/O for the backend
-   [Express] - fast node.js network app framework
-   [SocketIO] - Bidirectional and low-latency communication for every platform
-   [Docker] - Bidirectional and low-latency communication for every platform

Công nghệ sử dụng xây dựng giao diện người dùng:

-   [VueJS] - HTML enhanced for web apps!

Hệ cơ sở dũ liệu : [MongoDB]

## Cài đặt

Yêu cầu tối thiểu [Node.js](https://nodejs.org/) v10+

Tiến hành cài đặt các gói thư viện cần thiết cho Back-end:

```sh
cd backend
npm install --force
```

Tiến hành cài đặt các gói thư viện cần thiết cho Front-end:

```sh
cd frontend
npm install
```

Cấu hình các biến môi trường cho Front-end:

-   **SERVER_BASE_URL**: địa chỉ mặc định của server.
-   **VUE_APP_BASE_URL**: địa chỉ mặc định của VueJS font-end chạy ở môi trường DEV.
-   **VUE_APP_API_URL**: chỉ định địa chỉ API cho việc call API ở phía font-end.

Cấu hình các biến môi trường cho Back-end:

-   **PORT**: port của server.
-   **HOST**: host của server mặc định là localhost.
-   **PORT_CLIENT**: port front end.
-   **DB_URL**: địa chỉ url của mongodb docker (ex: mongodb://mongo_container:27017/SOA_Midterm).
-   **ADMIN_PASSWORD**: 123456.
-   **ACCESS_TOKEN_SECRET_KEY**: .
-   **REFRESH_TOKEN_SECRET_KEY**: .

Cài đặt MongoDB, xem thêm cách cài đặt tại đây [MongoDB - Document]

## Khởi chạy hệ thống

Dưới đây là các bước chi tiết khởi chạy hệ thông sau khi hoàn thành các yêu cầu tối thiểu phía trên.

##### 1. Chạy ứng dụng :

APi sẽ được khởi chạy mặc định tại [localhost:3300](http://localhost:3300/)
Để xem document của api [localhost:3300/api/docs](http://localhost:3300/api/docs)

-   Khởi chạy api:

```
cd backend
npm run dev
```

Ứng dụng Vue sẽ được khởi chạy mặc định tại [localhost:8080](http://localhost:8080)

-   Khởi chạy Vue app:

```
cd frontend
npm run serve
```

##### 2. Build ứng dụng Vue:

Để build ứng dụng VUE bằng cách chạy dòng lệnh sau:

```
cd frontend
npm run build
```

Sau khi hoàn tất quá trình build ứng dụng, các tài nguyên được tạo trong thư mục **/frontend/dist**

##### 3. Deploy với docker:

```
docker-compose up
```

## License

MIT

**Thanks!**

[//]: # "These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax"
[dhp]: https://github.com/duonghuuphuc
[git]: https://git-scm.com/
[node.js]: http://nodejs.org
[express]: http://expressjs.com
[vuejs]: http://vuejs.org
[mongodb]: https://www.mongodb.com
[mongodb - document]: https://www.mongodb.com/docs/
[SocketIO]: https://socket.io/
[Docker]: https://www.docker.com/
