# 🛍️ Product Management System for Facebook Marketplace (Chrome Browser Extension)

## 🚀 Introduction

This project is a **Product Management System** designed to simplify product uploads to **Facebook Marketplace**. It allows users to:

- Add products with **name**, **price**, **category**, **condition**, and **image**
- Fetch and display products in a list
- Inject product details into **Facebook Marketplace**
- Automatically open the image upload dialog for manual selection

---

## 🛠️ Technologies Used

- **Laravel** (Backend API)
- **JavaScript** (Frontend logic & Chrome extension)
- **PHP** (Backend logic)
- **MySQL** (Database)

---

## 📥 Installation Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/tawfiquebd/product-uploader.git
cd product-uploader
git checkout staging
```

### 2️⃣ Install Dependencies

```bash
composer install
npm install
```

### 3️⃣ Set Up Environment

Copy `.env.example` to `.env` and configure your database settings:

```bash
cp .env.example .env
```

Update the `.env` file:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### 4️⃣ Generate Application Key

```bash
php artisan key:generate
```

### 5️⃣ Run Migrations

```bash
php artisan migrate
```

### 6️⃣ Seed Database (Optional)

```bash
php artisan db:seed
```

### 7️⃣ Create the Symbolic Link (for Image Storage)

```bash
php artisan storage:link
```

### 8️⃣ Start the Server

```bash
php artisan serve
```

Your API will be available at `http://127.0.0.1:8000` 🚀

---

## 📡 API Endpoints

### 1️⃣ Fetch All Products

```http
GET /api/products
```

#### Response:

```json
{
  "data": [
    {
      "id": 1,
      "name": "Product Name",
      "price": "50 USD",
      "category": "Tools",
      "condition": "New",
      "image": "storage/products/image.jpg"
    }
  ]
}
```

### 2️⃣ Add a New Product

```http
POST /api/products
```

#### Request Body (FormData):

```json
{
  "name": "New Product",
  "price": "100",
  "category": "Furniture",
  "condition": "Used - Like New",
  "image": "(file upload)"
}
```

#### Response:

```json
{
  "message": "Product added successfully",
  "product": {
    "id": 2,
    "name": "New Product",
    "price": "100",
    "category": "Furniture",
    "condition": "Used - Like New",
    "image": "storage/products/new_image.jpg"
  }
}
```

---

## 🖥️ Chrome Extension Setup

This project includes a **Chrome Extension** to inject products into **Facebook Marketplace**.

### 1️⃣ Load the Extension

1. Open **Google Chrome**
2. Go to `chrome://extensions/`
3. Enable **Developer Mode** (top-right corner)
4. Click **Load unpacked**
5. Select the `chrome-extension` folder in this project

### 2️⃣ Using the Extension

- Click the extension icon and **fetch products**
- Click **Inject** on a product to populate Facebook Marketplace fields

---

## 🎨 UI Enhancements

- **Styled category & condition dropdowns**

---

## 🤝 Contributing

Pull requests are welcome! Follow these steps to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add feature X'`)
4. Push to your branch (`git push origin feature-name`)
5. Open a **Pull Request**

---

## 📜 License

This project is licensed under the **MIT License**. Feel free to modify and use it.

---

## 📞 Contact

If you have any issues or suggestions, feel free to reach out:

- 📧 Email: `tawfiquegub@gmail.com`
- 🐦 LinkedIn: [https://linkedin.com/in/tawfiquebd](https://linkedin.com/in/tawfiquebd)
- 🌍 GitHub: [tawfiquebd](https://github.com/tawfiquebd)

---

🚀 **Happy Coding!** 🎉
