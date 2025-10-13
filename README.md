# <div align="center">🎁 Anugrah</div>

<div align="center">
  
![Version](https://img.shields.io/badge/version-1.0.0-blueviolet.svg?cacheSeconds=2592000)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-success.svg)
![License](https://img.shields.io/badge/license-MIT-yellow.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

### *Give with Grace — Share Joy, Spread Kindness* 💝

**A responsive donation platform connecting donors with communities**

[🚀 Features](#-features) • [📖 Setup](#%EF%B8%8F-setup-instructions) • [🛠️ Tech Stack](#%EF%B8%8F-tech-stack) • [📡 API](#-api-endpoints)

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />

</div>

## 🌟 About Anugrah

**Anugrah** (Sanskrit: अनुग्रह - meaning *grace* or *blessing*) is a full-stack donation platform that allows users to donate items by submitting a form with item details, images, and location information. Built with session-based authentication and real-time form validation.

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🚀 Features

<table>
<tr>
<td width="50%">

### 📦 **Core Features**
- 📝 Donate items with description
- 📸 Optional image upload
- 📍 Auto-location via Geolocation API
- ✅ Real-time form validation
- 🔄 No page reload (AJAX)
- 🗃️ MongoDB storage

</td>
<td width="50%">

### 🔐 **Security & UX**
- 🔒 Session-based authentication
- 🍪 Cookie storage
- 🚪 Logout functionality
- 📱 Responsive design
- 🎨 Clean UI
- ⚡ Fast performance

</td>
</tr>
</table>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🛠️ Tech Stack

<div align="center">

### **Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)

### **Backend**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=for-the-badge&logo=mongoose&logoColor=white)

### **Additional Tools**

![Multer](https://img.shields.io/badge/Multer-FF6B6B?style=for-the-badge&logo=files&logoColor=white)
![Express Session](https://img.shields.io/badge/Sessions-000000?style=for-the-badge&logo=express&logoColor=white)
![AJAX](https://img.shields.io/badge/AJAX-005571?style=for-the-badge&logo=ajax&logoColor=white)

</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## ⚙️ Setup Instructions

### 📋 Prerequisites

```bash
✓ Node.js >= 14.0.0
✓ MongoDB (local or Atlas)
✓ npm
```

### 🚀 Installation

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/anugrah.git
cd anugrah

# 2️⃣ Install dependencies
npm install

# 3️⃣ Setup environment variables (if applicable)
# Create .env file with:
MONGO_URI=your_mongodb_connection_string
SESSION_SECRET=your_secret_key

# 4️⃣ Start the server
node server.js

# 5️⃣ Open in browser
# Visit http://localhost:5000
```

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 📁 Project Structure

```
anugrah/
│
├── 📂 public/
│   ├── donation.css              # Main stylesheet
│   ├── donor.png                 # Favicon/icon
│   └── home.html                 # Home page
│
├── 📂 views/
│   └── donate.html               # Donation form
│
├── 📂 uploads/                   # Uploaded images
│
├── 📂 models/
│   └── Donor.js                  # Mongoose schema
│
├── 📄 server.js                  # Main server file
├── 📄 package.json               # Dependencies
└── 📄 README.md                  # Documentation
```

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 📡 API Endpoints

| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| `GET` | `/` | Serve home page | ❌ |
| `GET` | `/donate` | Serve donation form | ✅ |
| `POST` | `/donor` | Handle form submission (with image and location) | ✅ |
| `GET` | `/logout` | Destroy session and log out user | ✅ |

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🗄️ Database Schema

```javascript
{
  item: String,               // Item name/title
  description: String,        // Detailed description
  latitude: Number,           // Geographic latitude
  longitude: Number,          // Geographic longitude
  imagePath: String,          // Path to uploaded image
  timestamp: {                // Auto-generated timestamp
    type: Date, 
    default: Date.now 
  }
}
```

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🧪 Testing

### Testing Checklist

- ✅ Submit valid form entries
- ✅ Submit invalid entries (test validation)
- ✅ Grant location permission
- ✅ Deny location permission
- ✅ Upload supported image formats (.jpg, .png)
- ✅ Verify data saved to MongoDB
- ✅ Test session authentication
- ✅ Test logout functionality

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 📷 Screenshots Gallery

<div align="center">

### 🏠 Home Page
*Clean landing page with easy navigation*

![Home Page](https://github.com/user-attachments/assets/fdced12d-552e-49b9-b6d6-b91d5fff9d59)

---

### 📝 Donation Form
*Intuitive form with real-time validation*

![Donation Form 1](https://github.com/user-attachments/assets/999afdb6-04bf-4830-8645-cc7ce663a05b)

![Donation Form 2](https://github.com/user-attachments/assets/09e8e91c-0e45-401d-b0b2-741920ec655c)

![Donation Form 3](https://github.com/user-attachments/assets/a7a3f66b-79cf-48e8-bf5b-7373afcf8447)

---

### 📸 Image Upload & Details
*Easy image upload with preview*

![Upload 1](https://github.com/user-attachments/assets/02d4c2d4-9911-48cc-bae6-f982da69654a)

![Upload 2](https://github.com/user-attachments/assets/e661181f-b4b8-4050-b35f-05c1a5248aca)

![Upload 3](https://github.com/user-attachments/assets/23bdefe5-2ee9-4c2f-8e38-d4a518a55508)

---

### 📍 Location Tracking
*Automatic location detection*

![Location 1](https://github.com/user-attachments/assets/158fa4c9-3d07-4a91-b50a-a4be01626d90)

![Location 2](https://github.com/user-attachments/assets/73c2911a-c58b-4cd1-a210-ec0855ebe5f4)

---

### ✅ Form Submission
*Success confirmations and feedback*

![Success 1](https://github.com/user-attachments/assets/a4b2044f-a70d-48a9-992c-1f9a3603e914)

![Success 2](https://github.com/user-attachments/assets/ca4c366e-62d9-45c7-88dc-cee40627f5c2)

![Success 3](https://github.com/user-attachments/assets/fa40ba48-9f0f-4ee5-a139-76b5975be247)

---

### 🔐 Authentication
*Secure login and session management*

![Auth 1](https://github.com/user-attachments/assets/8b69d97d-e73b-4420-b51d-0c5ba41788d4)

![Auth 2](https://github.com/user-attachments/assets/59beaf9b-1af8-4ee6-ae7e-6be2b595861d)

![Auth 3](https://github.com/user-attachments/assets/489eef48-04b3-40f5-a86e-4d0ace5d6218)

---

### 📱 Responsive Design
*Works perfectly on all devices*

![Mobile 1](https://github.com/user-attachments/assets/ba0792df-5f71-44f5-b69c-6027218e7500)

![Mobile 2](https://github.com/user-attachments/assets/da6913b3-74ad-49c5-ab72-3f3d396aa320)

![Mobile 3](https://github.com/user-attachments/assets/3c7b0cb3-5bd4-43ee-ab3a-45912ab38684)

---

### 🎨 UI Elements
*Beautiful and functional interface*

![UI 1](https://github.com/user-attachments/assets/111338ea-08ab-4731-a27b-c101495da413)

![UI 2](https://github.com/user-attachments/assets/a0df013d-e884-40f5-994f-45029c27c99d)

</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🤝 Contributing

Contributions are welcome! Here's how:

```bash
# Fork the repository
# Create your feature branch
git checkout -b feature/AmazingFeature

# Commit your changes
git commit -m 'Add some AmazingFeature'

# Push to the branch
git push origin feature/AmazingFeature

# Open a Pull Request
```

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 🙌 Acknowledgements

- [MDN Web Docs](https://developer.mozilla.org/) - Web development resources
- [Express.js](https://expressjs.com/) - Web framework
- [Mongoose](https://mongoosejs.com/) - MongoDB ODM
- [jQuery](https://jquery.com/) - JavaScript library
- Open Source Community ❤️

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 👨‍💻 Author

<div align="center">

**[Your Name]**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/yourusername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yourusername)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

</div>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%" />
</div>

## 💖 Support

<div align="center">

If this project helped you, please consider giving it a ⭐️!

<img src="https://readme-typing-svg.herokuapp.com?font=Architects+Daughter&color=%2300D9FF&size=50&center=true&vCenter=true&height=60&width=800&lines=Thanks+for+visiting!;Give+with+Grace+💝;Spread+Kindness!" alt="Thanks"/>

---

**Built with 💚 | Made with ❤️ for Communities**

**[⬆ Back to Top](#-anugrah)**

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer" width="100%"/>

</div>
