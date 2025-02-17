# Analisis Mikrokontroller Pada MSP430

# MSP430: Struktur, Spesifikasi, dan Control Unit

![image](https://github.com/user-attachments/assets/ba3bc223-bf48-4a6f-b60a-dd556a82c1a7)
(MSP430)

## 1 Struktur MSP430

MSP430 adalah mikrokontroler 16-bit dari Texas Instruments, dirancang untuk aplikasi yang membutuhkan konsumsi daya sangat rendah (ultra-low-power). Arsitektur RISC membuatnya sederhana dan efisien.

### Blok Utama MSP430

1. **CPU (Central Processing Unit)**
   - 16-bit RISC core.
   - 27 instruksi inti.
   - 7 mode pengalamatan.

2. **Memori**
   - Flash Memory: Penyimpanan program non-volatile.
   - RAM: Data sementara selama eksekusi.
   - Info Memory: Area khusus untuk data kalibrasi atau konfigurasi.

3. **Clock System**
   - Dapat menggunakan internal clock (DCO) atau external crystal.
   - Low-power modes dengan LPM0–LPM4.

4. **Peripherals (Unit I/O)**
   - Timer_A dan Timer_B: PWM, capture, compare.
   - ADC: Analog-to-Digital Converter 10-bit atau 12-bit.
   - UART, SPI, I2C: Komunikasi serial.
   - Watchdog Timer (WDT).

5. **Digital I/O Ports**
   - Port digital dengan opsi pull-up/pull-down.

---

## 2 Spesifikasi Umum MSP430

 **Fitur**              **Detail**                           
 Arsitektur           =  16-bit RISC                         
 Kecepatan Clock      =  Hingga 25 MHz (tergantung model)    
 Tegangan Operasi     =  1.8V – 3.6V                         
 Memori Flash         =  0.5KB – 256KB                       
 RAM                  =  128B – 16KB                        
 GPIO                 =  8 hingga 80 pin I/O                
 ADC                  =  10-bit atau 12-bit SAR ADC         
 Komunikasi Serial    =  UART, SPI, I2C                     
 Power Modes          =  LPM0 – LPM4 (Low Power Modes)     

---

## 3 Control Unit MSP430

Control Unit (CU) bertugas mengelola aliran instruksi dan mengendalikan operasi internal CPU. Mari kita bahas lebih rinci!

### a. Fetch-Decode-Execute Cycle

1. **Fetch**
   - Mengambil instruksi dari Flash memory.
   - PC (Program Counter) mengarahkan alamat instruksi berikutnya.

2. **Decode**
   - Instruksi didekode untuk menentukan opcode dan mode pengalamatan.

3. **Execute**
   - ALU (Arithmetic Logic Unit) menjalankan operasi aritmetika/logika.

---

### b. Status Register (SR)

- Status Register menyimpan flag penting selama eksekusi instruksi:
  - **C (Carry)**: Menunjukkan overflow aritmetika.
  - **Z (Zero)**: Menunjukkan hasil operasi bernilai nol.
  - **N (Negative)**: Menunjukkan hasil negatif.
  - **V (Overflow)**: Menandakan overflow signed arithmetic.

---

### c. Interrupt Control

1. **Vectored Interrupts**
   - Setiap sumber interrupt memiliki vektor alamat tertentu.

2. **Low-Latency Wake-up**
   - CPU dapat terbangun dari low-power mode dengan interrupt.

---

## 4 Unit yang Dikontrol oleh Control Unit

 **Unit**               **Fungsi**                                            
 Program Counter (PC)  = Mengarahkan alamat instruksi berikutnya.              
 Stack Pointer (SP)    = Mengelola tumpukan data selama eksekusi program.      
 Status Register (SR)  = Menyimpan kondisi hasil operasi ALU.                  
 General Purpose Regs  = Menyimpan data sementara selama proses eksekusi.      
 Clock System          = Mengatur kecepatan eksekusi dan mode daya rendah.     
 Watchdog Timer (WDT)  = Memastikan mikrokontroler tidak mengalami crash.      
 GPIO Control          = Mengelola input/output digital pada pin mikrokontroler. 

---

## 5 Kelebihan MSP430

 **Ultra-Low-Power:** Sangat hemat daya, cocok untuk sensor nirkabel dan pengukuran energi.
 **Compact Instruction Set:** Set instruksi ringkas dan efisien.
 **Low-Power Modes:** LPM0-LPM4 untuk menghemat energi saat idle.
 **Flexible Peripherals:** ADC, timer, komunikasi serial.

---


