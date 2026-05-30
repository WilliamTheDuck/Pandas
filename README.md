### CẨM NANG NHẬP MÔN: PANDAS & MATPLOTLIB TRONG 90 PHÚT

Tài liệu này được thiết kế nhằm giúp người mới bắt đầu làm quen với Python có thể nhanh chóng nắm bắt các thao tác cơ bản nhất về xử lý và trực quan hóa dữ liệu.

### PANDAS
---

Pandas là thư viện mạnh mẽ nhất trong Python để làm việc với dữ liệu dạng bảng (tương tự như Excel nhưng tự động hóa bằng code).

**1. Cấu trúc cốt lõi**

Series: Mảng dữ liệu 1 chiều (tương đương 1 cột trong bảng).

DataFrame: Mảng dữ liệu 2 chiều (tương đương 1 bảng gồm nhiều hàng, nhiều cột). Bản chất DataFrame là tập hợp của nhiều Series.

**2. Đọc và Kiểm tra Dữ liệu**

Bước đầu tiên luôn là tải dữ liệu và kiểm tra cấu trúc của nó trước khi xử lý.

```python
df = pd.read_csv('file.csv') # Đọc dữ liệu từ định dạng CSV.

df.head(5) #Xem trước 5 dòng đầu tiên để đảm bảo dữ liệu được tải đúng.

df.tail(2) #Xem trước 5 dòng cuối tiên để đảm bảo dữ liệu được tải đúng.

df.info() #Xem thông tin tổng quan (số lượng cột, số dòng, kiểu dữ liệu, có giá trị khuyết thiếu hay không).

df.describe() #Thống kê mô tả nhanh (Min, Max, Trung bình, Độ lệch chuẩn...).
```

**3. Truy vấn & Lọc dữ liệu**

Trích xuất các thông tin cụ thể từ tập dữ liệu lớn dựa trên các điều kiện.

Chọn 1 cột: 
```python
df['Tên_Cột']
```
Lọc theo 1 điều kiện: df[df['DiemToan'] >= 8.0] (Lấy danh sách học sinh có điểm Toán >= 8).

Lọc theo nhiều điều kiện: Sử dụng toán tử & (VÀ), | (HOẶC). Lưu ý phải sử dụng dấu ngoặc đơn cho từng điều kiện: df[(df['DiemToan'] > 5) & (df['GioiTinh'] == 'Nam')].

**4. Làm sạch dữ liệu**

Dữ liệu thực tế thường xuyên gặp tình trạng thiếu hụt (missing data - biểu diễn là NaN).
```python
df.isna().sum() #Thống kê số lượng giá trị NaN trong từng cột.

df.dropna() #Loại bỏ hoàn toàn các hàng chứa giá trị NaN.

df.fillna(0) #Thay thế các giá trị NaN bằng một giá trị cụ thể (ví dụ: 0) hoặc bằng giá trị trung bình.
```
**5. Gom nhóm dữ liệu**

Tương tự tính năng Pivot Table trong Excel, dùng để tổng hợp số liệu theo nhóm.
```python
df.groupby('Lớp')['DiemToan'].mean() #Gom nhóm dữ liệu theo 'Lớp', sau đó tính điểm trung bình của cột 'DiemToan'.
```
**6. Các Lỗi Thường Gặp**

KeyError: Gõ sai tên cột (Cần chú ý viết hoa/viết thường và khoảng trắng thừa).

SettingWithCopyWarning: Cảnh báo khi bạn cố gắng thay đổi dữ liệu trên một "lát cắt" (view) thay vì bản gốc. Giải pháp: Thêm .copy() khi tạo DataFrame mới từ một phần của DataFrame cũ.

### MATPLOTLIB
---

Dữ liệu sẽ trở nên dễ hiểu hơn rất nhiều khi được chuyển hóa thành các biểu đồ. pyplot là module phổ biến nhất của Matplotlib.

**1. Thông số biểu đồ cơ bản**
```python
plt.plot(x, y) #Lệnh vẽ biểu đồ cơ bản.

plt.title('Tên biểu đồ') #Đặt tiêu đề cho biểu đồ.

plt.xlabel('Trục X'), plt.ylabel('Trục Y') #Đặt tên nhãn cho các trục tọa độ.

plt.legend() #Hiển thị chú thích (Yêu cầu phải có tham số label='...' trong lệnh vẽ).

plt.show() # Lệnh bắt buộc dùng để kết thúc quá trình thiết lập và hiển thị biểu đồ lên màn hình.
```
**2. Các loại biểu đồ (Chart) thông dụng**

Line Chart (Biểu đồ đường): Dùng `plt.plot()` -> Thể hiện xu hướng theo thời gian.

Bar Chart (Biểu đồ cột): Dùng `plt.bar()` -> So sánh giá trị giữa các hạng mục khác nhau.

Scatter Plot (Biểu đồ phân tán): Dùng `plt.scatter()` -> Xem xét mối tương quan giữa hai biến số.

**3. Subplots (Vẽ nhiều biểu đồ trên cùng một khung hình)**

Giúp so sánh trực tiếp nhiều biểu đồ với nhau.

`fig, axes = plt.subplots(nrows=1, ncols=2)`: Tạo một khung hình (figure) chứa 1 hàng và 2 cột (2 biểu đồ).

Sử dụng axes[0].plot(...) cho biểu đồ thứ nhất và axes[1].plot(...) cho biểu đồ thứ hai.