# Defining a Union
- Union giống với struct, tuy nhiên các thành viên trong union sử dụng chung 1 vùng nhớ, như vậy tất cả các giá trị của thành viên đều như nhau. 
- Ví dụ ứng dụng của Union, ta tạo ra 2 phần tử int x và char y sau đó gán x = 65 khi gọi x chương trình sẽ trả về 65, gọi y thì chương trình trả về A (phiên dịch theo mã ASCII)
- Có thể ứng dụng vào quản lý dữ liệu trên binary tree

# Accessing Union Members
- Tuy cập vào phần tử union theo cách thông thường hoặc qua con trỏ đều được
	union test p1;
    	p1.x = 65;
	union test* p2 = &p1;
	printf("%d %c", p2->x, p2->y);