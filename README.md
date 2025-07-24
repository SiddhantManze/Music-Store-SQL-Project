# SQL Music Store Database System

📌 **Overview**
This project is a **complete relational database system** for a fictional music store, built using **MySQL** and **Python**. It includes:
✔ **Artist, Album, and Genre Cataloging**
✔ **Customer & Sales Management**
✔ **Employee Performance Tracking**
✔ **Automated Data Import Scripts**
✔ **SQL Views for Business Analytics**

---

🚀 **Features**
✅ **Database Schema:** 8 normalized tables (`artist`, `album`, `genre`, `employee`, `customer`, `invoice`, `invoice_line`, `track`)
✅ **Python ETL Script:** Automates CSV-to-MySQL data imports
✅ **Optimized SQL Queries:** Fast reporting and analytics for business insights
✅ **Predefined Views:** Sales trends, top customers, employee performance, and genre-specific data
✅ **GitHub-Ready:** Full documentation and setup guide

---

### Prerequisites
- **MySQL Server** (8.0+)
- **Python 3.8+**
- **MySQL Workbench** (Recommended for GUI)

## 📂 Database Schema

### Tables
| Table        | Description                                  |
|--------------|----------------------------------------------|
| `artist`     | [cite_start]Music artists and bands [cite: 1]            |
| `album`      | [cite_start]Album details (linked to artists) [cite: 1]  |
| `genre`      | [cite_start]Music genres (Rock, Jazz, etc.) [cite: 1]    |
| `employee`   | [cite_start]Store staff & support reps, including job title and seniority levels [cite: 1, 6] |
| `customer`   | [cite_start]Customer profiles & purchase history, including first/last names and contact info [cite: 1, 8] |
| `invoice`    | [cite_start]Sales transactions with billing information [cite: 1, 7] |
| `invoice_line`| [cite_start]Detailed information on each item within an invoice [cite: 1, 9] |
| `track`      | [cite_start]Details of each track, including genre and duration [cite: 1, 10] |

### Relationships
- `album.artist_id` → `artist.artist_id`
- `customer.support_rep_id` → `employee.employee_id`
- `invoice.customer_id` → `customer.customer_id`
- `invoice_line.invoice_id` → `invoice.invoice_id`
- `invoice_line.track_id` → `track.track_id`
- `track.album_id` → `album.album_id`
- `track.genre_id` → `genre.genre_id`

---

## 📊 SQL Views
| View Name               | Description                                  |
|-------------------------|----------------------------------------------|
| `vw_rock_albums`        | Lists all Rock genre albums                  |
| `vw_customer_spending`  | Tracks customer purchase totals              |
| `vw_employee_sales`     | Measures sales by support reps               |
| `vw_popular_genres_by_country` | [cite_start]Ranks music genres by purchase count per country [cite: 41] |
| `vw_top_spending_customers` | [cite_start]Identifies the top-spending customer for each country [cite: 42] |
| `vw_customer_artist_spending` | [cite_start]Calculates how much each customer has spent on each artist [cite: 37] |
| `vw_long_tracks`        | [cite_start]Lists all track names longer than the average track length [cite: 34] |

---

## 💡 How to Contribute
1.  **Fork** the repository
2.  Create a **new branch** (`git checkout -b feature/your-feature`)
3.  Commit changes (`git commit -m "Add feature"`)
4.  Push to the branch (`git push origin feature/your-feature`)
5.  Open a **Pull Request**
