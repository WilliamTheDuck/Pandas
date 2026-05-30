1. Lọc nâng cao (Filter)Câu 1: Tìm toàn bộ các vật tư thuộc danh mục 'Thuc Pham Tuoi' mà đang hết hàng (Số lượng tồn bằng 0).
2. Câu 2: Lọc ra danh sách vật tư có DonGia lớn hơn 200000 hoặc có SoLuongTon lớn hơn hoặc bằng 100.2. Sử dụng hàm .query()
3. Câu 3: Dùng .query() để tìm các vật tư có Đơn vị tính (DonViTinh) là 'Thung' và Đơn giá (DonGia) nhỏ hơn hoặc bằng 400000.
4. Câu 4: Dùng .query() để lấy ra các vật tư được cung cấp bởi nhà cung cấp không phải là 'Kho Ruou Tuan Tu'.3. Tạo cột và tính toán (Data Transformation)
5. Câu 5: Tạo thêm một cột tên là GiaTriTonKho được tính bằng công thức: SoLuongTon * DonGia.
6. Câu 6: Sắp xếp lại kho hàng theo thứ tự GiaTriTonKho giảm dần (mặt hàng có giá trị tồn lớn nhất nằm lên đầu).4. Thống kê & Gom nhóm (Groupby)
7. Câu 7: Tính tổng số lượng tồn kho của từng DanhMuc hàng hóa.Câu 8: Tìm giá tiền lớn nhất (Max) và giá tiền nhỏ nhất (Min) của các vật tư theo từng NhaCungCap.5. Xử lý chuỗi và Dữ liệu thiếu (Strings & Missing Values)Câu 9: Liệt kê các vật tư không có hạn sử dụng (Giá trị HanSuDung bị trống/NaN).Câu 10: Tìm các vật tư trong tên (TenVatTu) có chứa từ 'Nuoc'.