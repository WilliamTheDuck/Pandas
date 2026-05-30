Câu 1: Khởi động

Đọc file student_data.csv vào một biến DataFrame (ví dụ đặt tên là df).

Hiển thị 4 dòng đầu tiên và 2 dòng cuối cùng của bảng.

Kiểm tra xem bảng dữ liệu này có tổng cộng bao nhiêu dòng, bao nhiêu cột và có những cột nào bị trống (NaN)?

Hãy làm sạch các cột HoTen, GioiTinh, và Lop bằng cách loại bỏ các khoảng trắng thừa ở hai đầu.Kiểm tra xem sau khi strip, dữ liệu lớp chỉ còn đúng 3 nhóm nhãn là '10A1', '10A2', '10A3'.


Câu 2: Trích xuất dữ liệu (Lọc)

Lọc và in ra màn hình danh sách tất cả các học sinh học lớp 10A1.

Tìm những học sinh là Nu và có DiemToan lớn hơn hoặc bằng 8.0.

Tìm những học sinh có DiemToan dưới 5.0 HOẶC DiemVan dưới 5.0.


Câu 3: Phát hiện và xử lý "rác" (Dữ liệu khuyết)

Dùng code để kiểm tra xem mỗi cột đang bị thiếu bao nhiêu giá trị (NaN).

Tạo một DataFrame mới tên là df_sach, trong đó xóa bỏ toàn bộ các dòng có chứa giá trị NaN.

Trở lại với cái df ban đầu, đừng xóa nữa. Hãy điền con số 0 vào tất cả những vị trí bị thiếu điểm Toán và điểm Văn. (Từ câu này trở đi, dùng data đã được điền số 0).


Câu 4: Gom nhóm thống kê

Tính xem điểm Toán trung bình của mỗi lớp (10A1, 10A2, 10A3) là bao nhiêu?

Đếm số lượng học sinh Nam và Nu trong file dữ liệu này. 

Đếm số lượng học sinh Nam và Nu trong theo tung lop file dữ liệu này. 


Câu 5: Tính toán & Sắp xếp

Tạo thêm một cột mới tên là DiemTB. Công thức: DiemTB = (DiemToan + DiemVan) / 2.

Sắp xếp danh sách học sinh theo DiemTB từ cao xuống thấp (giảm dần). Hãy in ra 3 người có DiemTB cao nhất.


Câu 6: Bonus Thêm

Tìm tất cả học sinh có họ là "Nguyen" (Tên bắt đầu bằng chữ "Nguyen").

Liệt kê danh sách những học sinh bỏ thi môn Toán (Điểm Toán bị trống/NaN).

Điền điểm 0 vào tất cả những vị trí học sinh bỏ thi (giá trị NaN) để tính điểm chính xác.

Tính điểm TB, lọc học sinh TB >= 8.0 và xếp hạng