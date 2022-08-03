# Binary numbers and bits

# Bitwise Operators (Logical)

# Bitmasks
# Using Bit Operators to pack data
- Pack data thực chất là tích hợp nhiều thông tin có bề rộng nhỏ thành một vài thông tin lớn hơn 
- Ứng dụng rõ thấy nhất là các thanh ghi trong MCX514, nhà sản xuất quy định từng bit với các giá trị 0, 1 đại diện cho các thông số như thế nào 

# Using Bit Fields to pack data
- Tham khảo https://www.dictionary4it.com/term/bitfield-5250/
- ví dụ
	struct date {
    		// d has value between 0 and 31, so 5 +1 bits
    		// are sufficient, nếu chỉ có 5 bit thì MSB bit sẽ là số 1, dẫn đến trả về kết quả số âm
    		int d : 6;
 
    		// m has value between 0 and 15, so 4+1 bits
    		// are sufficient, giải thích tương tự trên
    		int m : 5;
 
    		int y : 11;
		};
- Chương trình sẽ chia struct thành các bit nhỏ, sau đó chèn các biến tích hợp được vào các ô bit đó. Khi tạo 1 biến khác không dùng bitfield hoặc kết thúc mảng, các ô trống còn lại sẽ không được dùng
- Ví dụ chúng ta chia bitfield dạng int ra, hệ thống sẽ cấp cho chúng ta 4 bytes, gộp các bitfields khác vào, khi vượt quá 4 bytes, hệ thống cấp thêm 4 bytes nữa. Nhưng một phần tử không được chia lớn hơn 4bytes. Trong ví dụ trên nếu chúng ta khai báo int m : 33; sẽ sinh ra lỗi
- Tuy nhiên, không thể trỏ vào bitfield member được, vì khi chia như vậy có thể phần tử không phải nằm ở đầu của byte. Câu lệnh sau đây sẽ gây ra lỗi
		printf("Address of t.x is %p", &t.x);
