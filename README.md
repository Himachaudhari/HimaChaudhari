## 👋 Hello! Welcome to my Portfolio 

<img width="2000" height="600" alt="Blue   Black Geometric Technology LinkedIn Banner" src="https://github.com/user-attachments/assets/b21be524-6c52-4c4b-9234-db68b2aef998" />


## 📌About Me

I am Himanshu M Chaudhari, an Embedded Systems trainee with strong programming skills in C, C++, Embedded C, and Data Structures. Currently training at Vector India, Hyderabad, I’m working extensively with microcontrollers like ARM7 (LPC2129/LPC2148), 8051 and gaining in-depth knowledge of embedded hardware and software integration.

My focus areas include real-time operating systems (RTOS), Linux-based development, and communication protocols such as CAN, SPI, I2C, and UART. I enjoy problem-solving and continuously seek to improve system efficiency and reliability. My dedication to learning and building practical solutions is driven by a passion for coding, electronics, and system interfacing.

I’m looking forward to contributing to innovative embedded technology projects and growing in a challenging, fast-paced environment that values creativity and technical depth.

________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
## 💻 Tools & Technologies:

 - __Programming Languages:__
      - C Programming 
      - C++ Programming
      - Python Programming
      - Linux System Programming
      - Linux Kernel Programming
      - Linux Device Driver Programming 
      - Data Structures & Algorithms (DSA)
      - Bare-Metal Programming
           - Embedded C
           - Embedded C++
           - Assembly Language 

 - __Microcontrollers:__
      - ARM Development Board
           - [LPC2129](https://github.com/Himachaudhari/Dynamic-OTP-Driven-Secure-Access-System.git)
           - [LPC2148](https://github.com/Himachaudhari/Dynamic-OTP-Driven-Secure-Access-System/blob/main/LPC214x%20Manual.pdf)
           - [STM32F407G]()
           - [STM32F103C8T6]()
      - Arduino Development Board
           - [Arduino Uno]()
           - [Arduino Nano]()
      - Microcontroller 8051 Development Board
           - [AT89S51](https://github.com/Himachaudhari/Dynamic-OTP-Driven-Secure-Access-System/blob/main/AT24C256.pdf)
           - [AT89C52](https://github.com/Himachaudhari/Dynamic-OTP-Driven-Secure-Access-System/blob/main/AT24C256.pdf)

 - __Operating Systems:__
    - Window
    - Linux (Ubuntu)
    - Real-Time Operating System (RTOS)

 - __Single Board Computer:__
    - Raspberry Pi 5
    - Beaglebone Black

 - __Developer Tools:__
    - Keil µVision
    - Proteus
    - Arduino IDE

 - __Protocols:__
    - CAN, SPI, I2C, USB, UART, TCP/IP, USART, UDP, ETHERNET, WIFI, BLUETOOTH, LIN

 - __Certificate:__
 - __Certificate and Achievements:__
    - [Vector India: Advanced Embedded System](https://drive.google.com/file/d/1nTKeDTNMIQDpTZGpLLPsMFHwkrV1Ie2T/view?usp=drivesdk)
   - [Smart india hackathon 2023](https://drive.google.com/file/d/1nSFFJ127w64BKGxnjHH7jbN6gDz8g8I6/view?usp=drivesdk)
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
<img width="1584" height="396" alt="Adobe Express - file (1)" src="https://github.com/user-attachments/assets/29a40a80-423c-46aa-ad09-1b8fdc974139" />

## MAJOR PROJECTS

__Module C, DSA, Embedded C, Linux, ARM7(LPC2148) & Protocols : DYNAMIC OTP-DRIVEN SECURE ACCESS SYSTEM___

__Objective:__ To architect and implement a Dynamic OTP‑Driven Secure Access System that delivers time‑sensitive, single‑use passcodes (OTP) to authenticate users against a protected backend, integrating strong cryptography, delivery flexibility, and robust system design, all while aligning with security best practices. Key components.


__Project Overview:__\
The system consists of two main components: \
__1. Front-End [Microcontroller (LPC2148) side]:__\
Acts like a real OTP Dynamic One-Time Password Generation:
 - Input Interface: User enters a password or request via keypad or serial/UART input.
 - Shared Secret / Seed: A stored token (counter, time-sync value, or key) within flash or NVRAM.
 - OTP Computation: Implement HOTP-like (counter-based) or TOTP-like (time-based) logic using HMAC‑SHA1/SHA256, possibly in software. This dynamic 6-digit OTP is generated per interaction.
 - Output: Displayed via LCD, UART, or transmitted via GSM/serial to remote device.
 - Verification Mechanism: Server or second microcontroller recalculates expected OTP and verifies match.
__2. Back-End [PC (Linux) side Application in C]:__\
Simulates a otp system:
 - Load user data: base32 secret, last-used timestep, retry count.
 - Request input: USER_ID, OTP, OPERATION (via CLI or socket).
 - Compute TOTP based on current UNIX time / 30 s.
 - Validate OTP:
Check that it matches generated code.
Ensure it's not already used (compare timestep).
If OK:
Mark current timestep used.
Reset retry count.
Print “ACCESS GRANTED”; log success.
If invalid:
Increment retry count; lockout if exceeded.
Log failure and reject.
Each attempt is logged: timestamp, user ID, provided OTP, operation, and result.

__Learning Keys:__
 - HOTP (counter-based): Uses a shared secret and a synchronized counter between client and server. Each successful authentication increments the counter. Allows look‑ahead to handle out‑of-sync counters
 - HMAC hashing: OTPs are produced by applying a keyed-hash message authentication code (SHA‑1 or SHA‑256) to the secret + counter (for HOTP) or time window (for TOTP), followed by dynamic truncation of output bits to derive a 6-digit code 
 - Single-use enforcement: Once an OTP is used, it must not be accepted again, even within the same time window or counter value. Replay protection must be enforced.
 - Base32 encoding: Secrets are stored in base32 format and decoded before OTP generation. Compatibility with standard authenticator apps and libraries is easier this way 
 - Comprehensive event logging: Log all OTP-related events—attempts, success or failure, timestamp, user ID, operation context—for diagnostics and compliance.
 - liboath (oathtool): A widely used C library that supports TOTP/HOTP and integrates easily into Linux/C applications 
 - For critical operations like transactions, consider using OCRA (Challenge‑Response OTP, RFC 6287) where the OTP is tied to contextual data (e.g. amount, account) for stronger security.
 - Metacognition: Be aware of your own thinking—plan, monitor your understanding, adjust strategies as needed. Examples include self-questioning, visualization, and reflection
 - Keil uVision & Flash Magic: Practiced embedded development cycle: code > compile > flash > test using LPC2148.
 - GCC & Linux Terminal Usage: Compiled and debugged C programs on Linux, improving command-line confidence.
 - Embedded-Desktop System Integration:  Understood complete flow of embedded system communicating with a software database.
 - Modular Code Architecture: Separated logic into reusable modules (RFID, keypad, LCD, UART, banking logic).
 - Debugging & Troubleshooting: Gained skills in tracing serial data issues, peripheral mismatches, and logical errors.
 - Real-Time Application Thinking: Developed understanding of real-world system behavior, user access security, and fault-tolerance.

__📁 View Project LPC2148: 🔗[Link](https://github.com/Himachaudhari/Dynamic-OTP-Driven-Secure-Access-System.git)__
________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

## 🌐 Let’s Connect!
📍 Location: Nagpur\
📧 Email: himanshuchaudhari110@gmail.com \
🔗 LinkedIn: https://www.linkedin.com/in/himanshu-chaudhari-22b59a2a5?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BR0YSWBr7ROeorw68%2BwhJoA%3D%3D\
📦 GitHub: https://github.com/Himachaudhari/HimaChaudhari

________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

## ✨ Final Words
Thank you for exploring my portfolio!
