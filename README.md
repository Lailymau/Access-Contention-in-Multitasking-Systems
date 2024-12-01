# Exercise 5 - Demonstrating Resource Contention in Multitasking Systems

**Deskripsi Singkat**  
Proyek ini menggunakan RTOS (Real-Time Operating System) untuk mengontrol LED pada mikrokontroler STM32. Dua tugas RTOS dikonfigurasikan untuk mengatur LED hijau dan merah secara bergantian dengan akses data bersama yang aman.

---

## 🎯 **Tujuan**
- Mengimplementasikan multitasking menggunakan FreeRTOS.  
- Mengidentifikasi dampak negatif dari tidak adanya mekanisme perlindungan sumber daya. 
- Mengelola akses data bersama secara aman untuk mencegah konflik antar tugas.

---

## 📂 Node Diagram
![image](https://github.com/user-attachments/assets/43c486cf-fb34-4313-8343-d65454baaaa0)

---

## 🛠️ **Peralatan**
- STM32 Microcontroller.  
- IDE STM32CubeIDE.  
- Framework RTOS: FreeRTOS.  
- Debugger  

---

## 📋 **Langkah Implementasi**
1. 🛠️ **Setup RTOS Tasks**  
   - Konfigurasikan dua tugas RTOS: **GreenTask** untuk LED hijau dan **RedTask** untuk LED merah.  
   - Atur prioritas masing-masing tugas dengan `osThreadAttr_t`.

2. 🌐 **Inisialisasi GPIO**  
   - Konfigurasikan pin GPIO untuk mengontrol LED.  

3. 🔐 **Pengelolaan Data Bersama**  
   - Implementasikan fungsi `AccessSharedData()` untuk mengelola akses aman terhadap data bersama.

4. ⏲️ **Konfigurasi Delay**  
   - Tambahkan jeda (delay) pada setiap tugas untuk memastikan eksekusi bergantian dengan lancar.

---

## 🎯 **Hasil yang Diharapkan**
- LED hijau dan merah menyala bergantian tanpa konflik data.
- LED hijau menyala setiap **500 ms**, sementara LED merah menyala setiap **100 ms**.   
- Konflik data dapat dihindari dengan mekanisme manajemen yang diterapkan dalam `AccessSharedData()`. 

---

## 📊 **Hasil Percobaan**
https://github.com/user-attachments/assets/36247127-44c3-4fca-9767-a421523ea4a4
