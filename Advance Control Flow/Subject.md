# The goto statement
- Giống trong bash

# NULL statement
- Là một lệnh thực thi, lệnh này không làm gì cả, nếu muốn thực thi lệnh và câu giờ thì dùng lệnh này

# comma operator
- Đánh giá qua toán tử thứ nhất, bỏ qua kết quả, đánh giá kết quả thứ 2 và trả về giá trị thứ 2
	int i = (5, 10); /* 10 is assigned to i*/
- Hoặc có nhiều toán tử ngăn cách với nhau bằng comma operator thì đánh giá lần lượt, trả về kết quả cuối
	int x = 10;
    	int y = (x++, ++x); //y=12

# setjump and longjmp functions
- nằm trong thư viện <setjmp.h>
- setjump(jmp_buf buf) : uses buf to remember current position and returns 0.
- longjump(jmp_buf buf, i) : Go back to place buf is pointing to and return i .