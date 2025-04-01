# Shop Smart, Save Time - Backend

## Giới thiệu
Backend cửa hàng tạp hóa online
### Thành viên
- **Lê Thành Nam**
- **Bùi Ngọc Đức**
- **Vũ Thành Dương**
- **Nguyễn Việt Quang**

## ⚙️ Công nghệ sử dụng
- **Node.js** (Express.js)
- **MySQL** (Sequelize ORM)
- **Socket.io** (Cập nhật thời gian thực)
- **JWT** (Xác thực người dùng)
- **Bcrypt** (Mã hóa mật khẩu)
- **Dotenv** (Quản lý biến môi trường)

## 🚀 Tính năng chính
- **Đăng ký & Xác thực người dùng**: Tạo tài khoản và đăng nhập an toàn.
- **Duyệt sản phẩm**: Khám phá nhiều mặt hàng tạp hóa với thông tin chi tiết.
- **Thêm vào giỏ hàng & Thanh toán**: Dễ dàng thêm sản phẩm vào giỏ hàng và tiến hành thanh toán.
- **Cập nhật thời gian thực**: Nhận thông báo và trạng thái đơn hàng tức thời.
- **Thanh toán an toàn**: Đảm bảo quy trình thanh toán thuận tiện và bảo mật.
- **Theo dõi đơn hàng**: Kiểm tra trạng thái đơn hàng để tiện theo dõi.

## Cài đặt và chạy dự án

### 1. Clone repository
```bash
git clone https://github.com/namthanhit/Online_Groceries_Node_backend
cd Online_Groceries_Node_backend
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

### 4. Khởi động server
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
- `GET /api/orders/track/:orderId` - Theo dõi đơn hàng

### Real-Time Updates
- `Socket.io` - Cập nhật trạng thái đơn hàng theo thời gian thực

Nhóm 6

