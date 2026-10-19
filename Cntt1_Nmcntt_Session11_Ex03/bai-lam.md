# Bài 3: Chuẩn hóa quy trình tra cứu dữ liệu kho hàng
## Phần 1: Định nghĩa rõ 4 tham số của VLOOKUP trong bài toán này
1. Lookup_value: Dữ liệu cần tìm kiếm
2. Table_array: Bảng chứa dữ liệu cần tìm (Nằm ở mã linh kiện -> Đơn giá)
3. Col_index_num: Số cột
4. Range_lookup: Giá trị tuyệt đối (0), giá trị tương đối (1)
## Phần 2: Viết công thức VLOOKUP hoàn chỉnh (kèm hàm IFERROR để xử lý lỗi #N/A thân thiện).
### Công thức VLOOKUP
- Lọc tên linh kiện

=IFERROR(VLOOKUP(Trim(A2),A2,$A$2:$C$100,2,1),"Mã không tồn tại")
- Lọc Đơn giá

=IFERROR(VLOOKUP(Trim(A2),A2,$A$2:$C$100,3,1),"Không có giá")
