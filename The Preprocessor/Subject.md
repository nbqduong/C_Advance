- preprocessor bắt đầu với kí tự #, cung cấp các chỉ thị trước biên dịch 
- Có 4 loại chỉ thị trước biên dịch:
# Macros
- cho chỉ thị #define tên, khi trình biên dịch gặp tên này, nó sẽ thay tên này bằng mảng code kèm theo phía sau
- Chúng ta có thể cho thêm tham số vào khi định nghĩa macro

#file inclusion
- kí tự <> theo sau #include nói cho trình biên dịch biết rằng nó nên tìm file trong các đường dẫn cơ bản (quy định trước khi cài ide hay gcc) "" thì là các file do người dùng tự định nghĩa 

# Conditional Compilation
- Chỉ thị cho trình biên dịch biết nên dịch hay loại bỏ phần nào của chương trình
- Các chỉ thị nằm ở giữa ifdef và endif

# Các chỉ thị khác
- #undef có tác dụng undefine a macro có sẵn
- #pragma  This directive is a special purpose directive and is used to turn on or off some features.
- #pragma startup and #pragma exit: These directives help us to specify the functions that are needed to run before program startup (before the control passes to main()) and just before program exit (just before the control returns from main()). 
- #if #elif #else #endif hoạt động bình thường
- #line
- #error chỉ thị này hủy bỏ quá trình biên dịch nếu phát hiện điều kiện do người lập trình đặt
