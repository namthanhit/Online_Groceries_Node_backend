# Online Groceries Shop - Backend

## Giới thiệu
Đây là backend của dự án **Online Groceries Shop**, một ứng dụng thương mại điện tử giúp người dùng mua sắm thực phẩm trực tuyến. Backend được xây dựng bằng **Node.js** và sử dụng **MySQL** làm hệ quản trị cơ sở dữ liệu.

## Công nghệ sử dụng
- **Node.js** (Express.js)
- **MySQL** (Sequelize ORM)
- **JWT** (Xác thực người dùng)
- **Bcrypt** (Mã hóa mật khẩu)
- **Dotenv** (Quản lý biến môi trường)

## Cài đặt và chạy dự án

### 1. Clone repository
```bash
git clone [https://github.com/your-username/Online_Groceries_Shop_Backend.git](https://github.com/namthanhit/Online_Groceries_Node_backend.git)
cd Online_Groceries_Shop_Backend
```

### 2. Cài đặt dependencies
```bash
npm install
```

### 3. Cấu hình môi trường
Tạo file `.env` trong thư mục gốc và thêm các thông số cấu hình:
```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=online_groceries_shop
JWT_SECRET=your_secret_key
```

### 4. Chạy migrations (nếu sử dụng Sequelize)
```bash
npx sequelize db:migrate
```

### 5. Khởi động server
```bash
npm start
```

Server sẽ chạy trên `http://localhost:5000`.

## API Endpoints

### Auth
- `POST /api/auth/register` - Đăng ký người dùng
- `POST /api/auth/login` - Đăng nhập người dùng

### Users
- `GET /api/users/profile` - Lấy thông tin người dùng

### Products
- `GET /api/products` - Lấy danh sách sản phẩm
- `GET /api/products/:id` - Lấy chi tiết sản phẩm
- `POST /api/products` - Thêm sản phẩm (Admin)
- `PUT /api/products/:id` - Cập nhật sản phẩm (Admin)
- `DELETE /api/products/:id` - Xóa sản phẩm (Admin)

### Orders
- `POST /api/orders` - Tạo đơn hàng
- `GET /api/orders/:id` - Lấy thông tin đơn hàng
- `GET /api/orders/user/:userId` - Lấy danh sách đơn hàng của người dùng

## Cấu trúc thư mục
```
Online_Groceries_Shop_Backend/
│── src/
│   ├── controllers/    # Xử lý logic API
│   ├── models/         # Định nghĩa models Sequelize
│   ├── routes/         # Định nghĩa API routes
│   ├── middlewares/    # Middleware (Xác thực, lỗi...)
│   ├── config/         # Cấu hình database, môi trường
│   ├── app.js          # Cấu hình ứng dụng Express
│── migrations/         # File migrations (nếu có)
│── .env                # File cấu hình môi trường
│── package.json        # Thông tin dependencies
│── README.md           # Tài liệu hướng dẫn
```

## Đóng góp
Nếu bạn muốn đóng góp, vui lòng tạo pull request hoặc mở issue để thảo luận.

## License
MIT
