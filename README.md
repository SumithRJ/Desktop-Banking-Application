# Desktop-Banking-Application
# PostInter Bank – Desktop Banking Application

A full-featured, Tkinter-based desktop banking app built in Python. PostInter Bank demonstrates user account management, secure login/OTP flows, transaction history, peer transfers, usage analytics, and profile handling (including avatar upload), all backed by a SQLite database.

---

## 🚀 Project Overview

PostInter Bank lets users:

- **Authenticate** via username/password or recover via email+OTP  
- **Create Accounts** with personal details, UPI key, and profile picture  
- **View & Edit Profile** (name, email, phone, address, avatar)  
- **Check Balance** with UPI validation  
- **Transfer Funds** to any account (peer-to-peer & friend payments)  
- **Browse Transaction History** (color-coded sent/received entries)  
- **Visualize Usage** with an in-app matplotlib graph  
- **Search & Pay Friends** by name or phone number  

All data is persisted in `myproject.db` (SQLite), and user photos are stored as BLOBs.

---

## 🧩 Repository Structure

```
.
├── main.py                 # Application entry point & UI logic
├── dbfile.py               # `OneUser` class: all DB operations & business logic
├── myproject.db            # SQLite database (auto-generated)
├── python_logo.gif         # App logo shown on login screen
├── requirements.txt        # Python dependencies
├── assets/                 # (Optional) Additional images
│   ├── logo1.jfif
│   ├── logo2.jfif
│   ├── logo3.jfif
│   └── friend.jpg
└── README.md               # This file
```

---

## 🔧 Technologies & Dependencies

- **Python 3.7+**  
- **GUI**: Tkinter, ttk, tkcalendar  
- **Database**: SQLite (`sqlite3`)  
- **Plotting**: matplotlib  
- **Image Handling**: Pillow (`PIL`)  
- **Email/OTP**: smtplib, random  
- **Other**: re, datetime  

Install dependencies with:

```bash
pip install -r requirements.txt
```

Your `requirements.txt` should include:

```
tkcalendar
pillow
matplotlib
```

*(Tkinter and sqlite3 are included in the Python standard library.)*

---

## 🛠️ Installation & Setup

1. **Clone the repo**  
   ```bash
   git clone https://github.com/your-username/PostInterBank.git
   cd PostInterBank
   ```

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Initialize the database**  
   On first run, `main.py` will create (or connect to) `myproject.db`.

4. **Run the application**  
   ```bash
   python main.py
   ```

---

## 📚 Usage

1. **Login**: Username/password or email OTP recovery.  
2. **Dashboard**: View balance, transactions, and navigate sections.  
3. **Profile**: Edit personal details and avatar.  
4. **Transfer**: Send funds to accounts or friends.  
5. **History**: Browse transactions (sent in red, received in green).  
6. **Analytics**: Plot last 30 balance changes.  

---

## 🔍 Database Schema

- **users** table: `id, name, email, address, dob, phone, password, upi, recent, image`  
- **banks** table: `id, bank_name, account_number, balance`  
- **transact** table: `fromacc, toacc, amount, timestamp, sender_name, receiver_name`

---

## 🚀 License

This project is released under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## 📬 Contact & Contributions

Contributions and feedback are welcome!  
Open an issue or PR, or contact **sumithrjala@gmail.com**.
