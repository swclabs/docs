# Tổng Quan Về Backend

## Mục lục

1.[Cấu trúc thư mục](#cấu-trúc-thư-mục)

## Cấu trúc thư mục

Dự án được tổ chức theo Clean Architecture, xem chi tiết các thư mục dưới đây:

**swipe-api**/
├── **cmd** : thư mục chứa các file bắt đầu.
│   ├── module
│   ├── server
│   └── worker
├── **delivery**: thư mục chứa các adapter kết nối các file thực thi với các framework.
├── **docs**: tạo ra bởi swagger
├── **hack**: chứa các file scripts của hệ thống
├── **internal**: thư mục chứa các Business Logic
│   ├── **config**: lưu các biến môi trường của hệ thống
│   ├── **core**: chứa 3 lớp chính của kiến trúc sạch
│   │   ├── domain
│   │   ├── repo
│   │   └── service
│   ├── **helper**: chứa các lớp, hàm trợ giúp các chức năng chính.
│   ├── **http**: chứa các controller và là nơi dùng framework.
│   │   ├── controller
│   │   ├── middleware
│   │   └── router
│   └── **workers**: hiện thực các produce/consume
├── misc
│   ├── archive
│   ├── k8s
│   ├── nginx
│   └── postman
├── **pkg**: chứa các gói được dùng chung trong dự án
│   ├── **cache**: sửa dụng Redis
│   ├── **cloud**: sửa dụng cloudinary
│   ├── **db**: sửa dụng postgresql
│   ├── **sentry**: theo dõi các lỗi của hệ thống khi vận hành
│   ├── **tools**: các công cụ cần thiết
│   ├── **utils**: các chức năng ngoài lề
│   └── **web**: chứa các template html
└── **test**: chứa các file test.
