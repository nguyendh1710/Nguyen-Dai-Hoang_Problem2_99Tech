Các điểm kém hiệu quả trong mã gốc:

-	Kiểm tra mức độ ưu tiên: Kiểm tra và lọc logic thừa trong hook useMemo.
-	Sắp xếp: Gọi lồng nhau của getPriority trong hàm sắp xếp.
-	Ánh xạ: Các hàm map riêng biệt để định dạng và render các hàng.
-	Logic dư thừa: Logic getPriority được sử dụng lặp lại và cần được đơn giản hóa.


Các cải tiến đã thực hiện:

-	Tính toán mức độ ưu tiên: Chuyển sang một bản đồ đối tượng duy nhất để tra cứu nhanh hơn.
-	Kết hợp Lọc và Ánh xạ: Kết hợp các hàm filter và map để tránh các vòng lặp thừa.
-	Sắp xếp tối ưu hóa: Đơn giản hóa logic sắp xếp bằng một dòng tính toán duy nhất.
-	Memoization: Đảm bảo chỉ bao gồm các phụ thuộc cần thiết trong hook useMemo.
