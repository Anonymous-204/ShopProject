# ShopProject
# Project Name

Mô tả ngắn gọn về dự án (1–3 câu).

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
- HandleBars
- Promt AI Gemini

## Installation

```bash
git clone https://github.com/yourname/project.git
cd project
npm install
```

## Environment

Tạo file `.env`:

.env
PORT=3000
DB_HOST=localhost
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

- Swagger: `http://localhost:3000/api`

## Author

Ngô Lê Anh Dương
