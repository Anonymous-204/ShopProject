# ShopProject
# Project Name

đây là dự án tôi dùng để luyện tay backend nodejs, tự học tự phát triển, 
có tham khảo Gemini để xây Front end phục vụ quá trình trải nghiệm

## Features

- Đăng ký / Đăng nhập / Đổi mật khẩu
- Quản lý người dùng
- CRUD sản phẩm
- Người dùng chủ động thêm sản phẩm hoặc đặt hàng
- ...

## Tech Stack

### Backend
- ExpressJs
- MySql
- JWT

### Frontend 
- giao diện được hỗ trợ viết bằng AI (Gemini) dựa trên Handlebars

###database

mysql -u root -p < schema.sql

## Installation

```bash
git clone https://github.com/Anonymous-204/ShopProject.git
cd shop
npm install
```

## Environment

Tạo file `.env`:

.env
PORT=3000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=shop_db
SECRET_KEY=mysupersecretkey123


## Run

npm start

## Project Structure

pro/
└── Shop/
    ├── .env
    ├── .gitignore
    ├── .vscode/
    │   └── settings.json
    ├── package.json
    ├── package-lock.json
    ├── schema.sql
    └── src/
        ├── index.js
        ├── controllers/
        │   ├── authControllers.js
        │   ├── cartControllers.js
        │   ├── orderControllers.js
        │   ├── productControllers.js
        │   └── userControllers.js
        ├── lib/
        │   └── db.js
        ├── middlewares/
        │   └── authMiddleware.js
        ├── routes/
        │   ├── authRoutes.js
        │   ├── cartRoutes.js
        │   ├── orderRoutes.js
        │   ├── productRoutes.js
        │   └── userRoutes.js
        ├── services/
        │   ├── authServices.js
        │   ├── cartServices.js
        │   ├── orderServices.js
        │   ├── productServices.js
        │   └── userService.js
        └── views/
            ├── cart.hbs
            ├── change.hbs
            ├── home.hbs
            ├── order.hbs
            ├── product.hbs
            ├── profile.hbs
            ├── signIn.hbs
            ├── Signup.hbs
            ├── test.hbs
            ├── layouts/
            │   └── main.hbs
            └── partials/
                └── navbar.hbs

## API Documentation

### Auth — `/api/auth`
- POST `/signup` — Đăng ký tài khoản
- POST `/signin` — Đăng nhập
- POST `/signout` — Đăng xuất
- POST `/refreshToken` — Làm mới access token
- PATCH `/change` — Đổi mật khẩu

### User — `/api/user` (yêu cầu đăng nhập)
- GET `/me` — Lấy thông tin user hiện tại
- GET `/profile` — Lấy thông tin chi tiết hồ sơ
- PATCH `/edit` — Cập nhật hồ sơ

### Product — `/api/product`
- GET `/search` — Tìm kiếm sản phẩm
- GET `/all` — Lấy danh sách sản phẩm công khai
- GET `/meta` 🔒 — Lấy metadata sản phẩm (brand, category...)
- GET `/products` 🔒 — Lấy sản phẩm theo user (người bán)
- POST `/create` 🔒 — Tạo sản phẩm mới
- GET `/:productId` — Xem chi tiết sản phẩm
- PATCH `/:productId` 🔒 — Cập nhật sản phẩm
- DELETE `/:productId` 🔒 — Xóa sản phẩm

### Cart — `/api/cart` (yêu cầu đăng nhập)
- GET `/` — Lấy giỏ hàng đang active
- POST `/` — Thêm sản phẩm / tăng số lượng
- PUT `/` — Cập nhật số lượng nhiều sản phẩm
- DELETE `/` — Xóa toàn bộ giỏ hàng
- DELETE `/:cartItemId` — Xóa 1 sản phẩm khỏi giỏ

### Order — `/api/order` (yêu cầu đăng nhập)
- POST `/checkout` — Đặt hàng (checkout)
- GET `/` — Lấy danh sách đơn hàng của user

🔒 = route riêng yêu cầu đăng nhập thêm (ngoài các route đã chung `protectedRoute` ở đầu file)

## Author

Ngô Lê Anh Dương
