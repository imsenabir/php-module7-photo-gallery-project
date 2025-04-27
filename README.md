# Photo Gallery App

A simple web application where users can upload and view images. Built with PHP, MySQL, and Bootstrap (optional).

---

## 📂 Project Structure

```
photo-gallery/
├── assets/
│   └── images/          # Stores uploaded images
├── includes/
│   ├── config.php       # Database connection (using PDO)
│   ├── header.php       # Site header and navigation
│   └── footer.php       # Site footer
├── index.php             # Displays all uploaded images
└── upload.php            # Form to upload new images
```

---

## 🗄️ Database Setup

- Database Name: `photo_gallery`
- Table: `images`

| Column Name  | Type         | Details                      |
|--------------|--------------|-------------------------------|
| id           | INT          | Auto Increment, Primary Key  |
| title        | VARCHAR      | Image title                  |
| description  | TEXT         | Image description            |
| filename     | VARCHAR      | Saved filename               |
| upload_date  | TIMESTAMP    | Defaults to current time     |

---

## ⚙️ Features

- Upload images (max 5MB).
- Store images in `/assets/images/` folder.
- Save image details (title, description, filename, upload date) to the database.
- Display uploaded images in a gallery format.
- Show image title and upload date under each photo.
- Use Bootstrap for responsive styling (optional).

---

## 🚀 How to Run

1. **Clone/Download the project** and place it in your web server directory (e.g., `htdocs` for XAMPP).

2. **Create the database**:
    - Import the following SQL:
      ```sql
      CREATE DATABASE photo_gallery;
      
      USE photo_gallery;
      
      CREATE TABLE images (
          id INT AUTO_INCREMENT PRIMARY KEY,
          title VARCHAR(255) NOT NULL,
          description TEXT,
          filename VARCHAR(255) NOT NULL,
          upload_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
      );
      ```

3. **Configure database connection**:
    - Edit `includes/config.php` with your database credentials.

4. **Access the app**:
    - Open your browser and visit `http://localhost/photo-gallery/`.

---

## 🛠️ Notes

- Ensure your `assets/images/` folder has write permissions.
- Validate file types (only image uploads recommended for security).
- Bootstrap CDN can be included for quick styling.
- Keep PHP and HTML code clean and well-commented.

---
