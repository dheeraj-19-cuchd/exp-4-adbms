# 🗄️ Transactions and Concurrency Control Demo

This repository contains SQL scripts to demonstrate concurrency control and transaction management in relational databases using a simple `StudentEnrollments` table.  
The examples cover **deadlock simulation, MVCC (Multiversion Concurrency Control), and row-level locking**, showing how data integrity is maintained under concurrent access.  

---

## 📂 Files

- **session_one.sql** – SQL script for Session 1 (Transaction operations, deadlock, MVCC, locking)  
- **session_two.sql** – SQL script for Session 2 (Transaction operations, deadlock, MVCC, locking)  
- **assets/session_one_output.png** – Output screenshot of Session 1  
- **assets/session_two_output.png** – Output screenshot of Session 2  

---

## ⚡ Problem Breakdown

### **Part A – Deadlock Simulation**
- Simulates deadlock when two concurrent sessions update rows in different orders.  
- Demonstrates how DB detects and resolves deadlocks.  

### **Part B – MVCC (Multiversion Concurrency Control)**
- Uses `REPEATABLE READ` isolation level.  
- Shows consistent reads without blocking updates.  
- Prevents dirty reads and non-repeatable reads.  

### **Part C – Locking vs. MVCC**
- Demonstrates `SELECT ... FOR UPDATE` row-level locking.  
- One session holds lock, another session waits until commit/rollback.  
- Compares blocking behavior of locks with non-blocking MVCC.  

---

## 📊 Outputs

### 🔹 Session 1 Output
<img src="assets/session_one_output.png" alt="Session One Output" width="700"/>

### 🔹 Session 2 Output
<img src="assets/session_two_output.png" alt="Session Two Output" width="700"/>

---

## ✅ Key Learnings

- Deadlocks can occur when transactions lock resources in different orders.  
- MVCC allows **non-blocking reads** while maintaining isolation.  
- Row-level locks ensure **strong consistency** but can block concurrent updates.  
- Correct use of **isolation levels** and **locking** ensures data integrity under concurrency.  

---
