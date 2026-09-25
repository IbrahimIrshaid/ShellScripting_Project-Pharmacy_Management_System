# Pharmacy Management System (PMS)

This is a terminal-based Pharmacy Management System written in Bash. It uses the `dialog` utility to provide a user-friendly interface and allows pharmacy staff to manage inventory, process sales, search for data, and generate various reports.

---

## 📁 Project Structure

- `PMS.txt` – Main script to launch the system, display the main menu and navigate between sub-menus.
- `inventoryMenu.txt` – Manages adding, updating, removing all expired, and displaying medicines.
- `salesOp.txt` – Handles sales operations, billing, and customer records.
- `searchMenu.txt` – Allows searching by medicine name, category, and retrieves customer history.
- `reportMenu.txt` – Generates reports for low-stock, expired medicines, sales within a given period, and top-selling medicines.
- `inventory.txt` – Stores medicine records in CSV format.
- `sales.txt` – Logs individual sales in CSV format.
- `salesPerMedName.txt` – Tracks number of units sold per medicine.
- `customers.txt` – Contains customer name, contact info and purchase history.
- `error.txt` – Logs errors or invalid operations.
- `logs.txt` – Records user login data.
- `bill.txt`, `LsReport.txt` – Temporary files for displaying output.

---

## ✅ Features

- **Inventory Management**
  - Add new medicine to the inventory with data validation.
  - Update quantity or price.
  - Remove expired items.
  - Display all inventory items.

- **Sales Management**
  - Make a sale and auto-update inventory.
  - Generate and display a customer bill.
  - Maintain sales and customer history.

- **Search System**
  - Search medicine by name or category.
  - Retrieve a customer's purchase history.

- **Report Generation**
  - View low-stock medicines.
  - List expired medicines.
  - Generate sales report within a date range.
  - Show top-selling medicines.

---

## 🚀 How to Run

1. **Ensure Bash and dialog are installed:**

```bash
sudo apt install dialog
```

2. **Make the PMS script executable:**

```bash
chmod +x PMS.txt 

```
- other files are excuted withen the PMS file 

3. **Run the main program:**

```bash
./PMS.txt
```

---

## 📌 Notes

- Date format should always be `yyyy-mm-dd` which is checked in the inventoryMenu => addMed() function 
- The system uses CSV-style text files for data persistence.
- Errors and user attempts (like trying to sell a non-existent medicine) are logged for later review.
- The salesPerMed file is used to get easily sort the top sold medicines 
- In the update medicine info & make a sale features the program keeps dispalying a yes or no box using the dialog command dialog --yesno so the user can update as many medicines as they want 
- The purchase history should always have a space (" ") before any purchase field because the program depends on it for inserting any new purchase feild 

---

