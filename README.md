# 🍔 Food Delivery App (Flutter)

Ứng dụng đặt món ăn giao hàng viết bằng **Flutter**, xây dựng giao diện theo phong cách food-delivery hiện đại: màn hình chào, danh sách món theo danh mục, và trang chi tiết món ăn.

> Đồ án môn **Lập trình di động** — Nguyễn Hoàng Sơn (22010011)

## 📱 Tính năng

| Màn hình | Mô tả |
| --- | --- |
| **Onboarding** (`onboard_page.dart`) | Màn hình giới thiệu đầu tiên với hình minh hoạ, nút bắt đầu dẫn vào trang chủ |
| **Home** (`food_delivery_home_screen.dart`) | Danh sách món ăn dạng thẻ, thanh danh mục (Burger / Pizza / Cup Cake) lọc món theo `category`, giá, đánh giá (rating), nhấn vào món để xem chi tiết |
| **Food Detail** (`food_detail_screen.dart`) | Hình lớn, tên món, giá, đánh giá, mô tả rút gọn/mở rộng bằng package `readmore`, nút quay lại |

- Dữ liệu mẫu tĩnh trong `models/product_model.dart` (6 món) và `models/categories_model.dart` (3 danh mục).
- Bảng màu và hằng số giao diện tập trung tại `consts.dart`.
- Widget hiển thị thẻ sản phẩm tái sử dụng: `Widget/products_items_display.dart`.

## 🗂 Cấu trúc thư mục

```
lib/
└── Food_Delivery_App/
    ├── main.dart                  # Điểm khởi chạy, MaterialApp
    ├── consts.dart                # Màu sắc dùng chung
    ├── models/
    │   ├── product_model.dart     # FoodModel + danh sách món ăn
    │   └── categories_model.dart  # Category + danh sách danh mục
    ├── pages/
    │   ├── onboard_page.dart
    │   ├── food_delivery_home_screen.dart
    │   └── food_detail_screen.dart
    └── Widget/
        └── products_items_display.dart
assets/food-delivery/              # Hình ảnh món ăn & icon
```

## 🚀 Chạy dự án

Yêu cầu: **Flutter SDK ≥ 3.7.2** ([hướng dẫn cài đặt](https://docs.flutter.dev/get-started/install)).

```bash
# 1. Lấy dependencies
flutter pub get

# 2. Kiểm tra thiết bị / giả lập
flutter devices

# 3. Chạy app
flutter run
```

Chạy trên một nền tảng cụ thể:

```bash
flutter run -d chrome     # Web
flutter run -d windows    # Windows
flutter run -d android    # Android (cần emulator hoặc máy thật)
```

Build bản phát hành:

```bash
flutter build apk --release      # Android
flutter build web --release      # Web
flutter build windows --release  # Windows
```

## 📦 Thư viện sử dụng

| Package | Mục đích |
| --- | --- |
| `cupertino_icons` | Bộ icon iOS |
| `readmore` | Rút gọn / mở rộng đoạn mô tả dài |
| `flutter_lints` | Quy tắc lint cho code Dart |

## 🔮 Hướng phát triển

- Thêm giỏ hàng, đặt hàng và tính phí giao hàng
- Lưu dữ liệu cục bộ (Hive/SQLite) hoặc gọi API backend
- Tìm kiếm món ăn, đăng nhập người dùng, theo dõi đơn hàng

## 📄 Giấy phép

Dự án dùng cho mục đích học tập.
