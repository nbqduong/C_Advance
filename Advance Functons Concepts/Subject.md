# Variadic Functions
- Variadic functions are functions that can take a variable number of arguments
- Chúng ta có thể truy cập các giá trị truyền vào thông qua thư viện <stdarg.h>
- Các lệnh tham khảo:
- va_start(va_list ap, argN)	This enables access to variadic function arguments
- va_arg(va_list ap, type)	This one accesses the next variadic function argument.
- va_copy(va_list dest, va_list src)	This makes a copy of the variadic function arguments.
- va_end(va_list ap)	This ends the traversal of the variadic function arguments. 
# va_copy

- Nhìn chung hàm variadic functions hỗ trợ tốt cho việc hàm chứa nhiều thông số, số lượng thông số chưa biết khi lập trình. Ví dụ ứng dụng đơn giản là hàm tổng hay hàm tìm giá trị lớn nhất
- (tham khảo thêm)[https://www.geeksforgeeks.org/variadic-functions-in-c/ư

# Inline functions
- công cụ giúp gói hàm, nhìn dễ hơn

# _Noreturn Functions
- Hàm này sẽ không trả về hàm gọi nó
- The primary benefits for using _Noreturn (or the equivalent noreturn) are making the intention of the function clear in the code for future readers, and detecting unintentionally unreachable code.
