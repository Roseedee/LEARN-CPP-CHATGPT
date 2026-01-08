# 🧭 C++ Programming with Win32 API – Learning Roadmap

แผนการเรียนนี้ออกแบบมาสำหรับผู้ที่ **เขียน C++ ระดับพื้นฐานได้แล้ว** และต้องการพัฒนาไปสู่
**Windows System / Low-level / OS-oriented programming** โดยอิงตาม Win32 API ของ Microsoft

> เป้าหมาย
> - อ่าน Win32 API documentation แล้วเข้าใจ
> - เขียน Windows application ด้วย C++ แบบไม่พึ่ง framework
> - ปูพื้นฐานสู่ Windows Internals / Kernel / Low-level systems

---

## 🟦 Week 1: C++ Fundamentals for Win32
> เตรียมภาษาให้พร้อมสำหรับ Win32 (ซึ่งใช้ C++ แบบ low-level มาก)

### Topics
- Compilation model (source → object → linker → exe)
- Header / Source separation
- Pointer & Reference (practical usage)
- `struct` vs `class`
- RAII concept (basic)
- `const`, `constexpr`

### Practice
- แยก `.h` / `.cpp` เอง
- ใช้ pointer ส่งค่าเข้า function
- อ่าน struct จาก header

---

## 🟦 Week 2: Windows & Win32 Fundamentals
> เข้าใจสถาปัตยกรรมของ Windows OS

### Topics
- Windows architecture (User mode / Kernel mode)
- HANDLE concept
- Windows data types
  - `DWORD`, `BOOL`, `LPVOID`, `LPCWSTR`
- Unicode / Wide character strings
- Error handling
  - `GetLastError`
  - `FormatMessage`

### Practice
- Console application เรียกใช้ Win32 API
- แสดง error message จาก error code

---

## 🟦 Week 3: Win32 Program Structure (Core)
> หัวใจของ Win32 programming

### Topics
- `WinMain`
- `WNDCLASSEX`
- `RegisterClassEx`
- `CreateWindowEx`
- Message loop
  - `GetMessage`
  - `DispatchMessage`
- Window Procedure (`WndProc`)

### Mini Project
- สร้างหน้าต่างเปล่า ๆ ด้วย Win32
- ปิดหน้าต่างแล้วโปรแกรมจบอย่างถูกต้อง

---

## 🟦 Week 4: Message System & Event-Driven Programming
> เปลี่ยน mindset สู่ event-driven architecture

### Topics
- Windows message system
- Common messages
  - `WM_CREATE`
  - `WM_PAINT`
  - `WM_COMMAND`
  - `WM_DESTROY`
- Keyboard input messages
- Mouse input messages

### Mini Project
- แสดงข้อความเมื่อกด keyboard
- แสดงตำแหน่ง mouse เมื่อคลิก

---

## 🟦 Week 5: GDI & Low-level Drawing
> เข้าใจระบบวาดภาพระดับต่ำของ Windows

### Topics
- Device Context (`HDC`)
- `BeginPaint` / `EndPaint`
- Drawing primitives
  - Line
  - Rectangle
  - Text
- GDI Objects
  - Pen
  - Brush
  - Font
- Resource lifetime management

### Mini Project
- วาดรูปทรงพื้นฐาน
- แสดงข้อความตามตำแหน่ง mouse

---

## 🟦 Week 6: Controls, Dialogs & Resources
> สร้าง GUI ด้วย Win32 แบบดิบ

### Topics
- Standard controls
  - Button
  - Edit
  - Static
- Control messages
- Dialog box
- Resource script (`.rc`)
- Menu & accelerator

### Mini Project
- โปรแกรมที่มีปุ่มและกล่องข้อความ
- เมนู `File -> Exit`

---

## 🟦 Week 7: File, Process & Thread (System Core)
> เริ่มเข้าสู่ system programming อย่างแท้จริง

### Topics
- File I/O
  - `CreateFile`
  - `ReadFile`
  - `WriteFile`
- Process management
  - `CreateProcess`
- Threading
  - `CreateThread`
- Synchronization
  - Mutex
  - Critical Section

### Mini Project
- อ่านไฟล์ด้วย Win32 API
- Thread ทำงานเบื้องหลัง

---

## 🟦 Week 8: Memory & Windows Internals (Low-level)
> ปูทางสู่ OS / Kernel development

### Topics
- Virtual memory
  - `VirtualAlloc`
  - `VirtualProtect`
- Heap vs Virtual memory
- Memory alignment & protection
- PE file format (concept)
- DLL loading mechanism (concept)

### Mini Project
- Allocate memory ด้วย `VirtualAlloc`
- ทดลองเปลี่ยน memory protection

---

## 🧠 Learning Tips
- อ่าน Microsoft Docs → ดู function signature → เปิด header file
- ใช้ debugger ของ Visual Studio อย่างจริงจัง
- อย่า copy code ทั้งหมดโดยไม่เข้าใจ
- ถามตัวเองเสมอ: **"OS ทำอะไรให้เรา?"**

---

## 🚀 Next Steps (Advanced)
หลังจาก roadmap นี้ สามารถต่อยอดไปสู่:
- Windows Internals
- NT Native API
- Driver development
- Kernel debugging
- Reverse engineering (defensive / educational)

---

> 📌 เหมาะสำหรับเก็บไว้ใน GitHub เป็น learning roadmap หรือ study notes
