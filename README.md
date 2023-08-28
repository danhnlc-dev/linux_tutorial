# Linux Tutorial

## Website Tool

- Xem thông tin và tài liệu liên quan đến các bản phân phối Linux và các hệ điều hành mã nguồn mở khác.
  [distrowatch](https://distrowatch.com)

- Web cung cấp các dịch vụ và công cụ liên quan đến việc kiểm tra bảo mật, phân tích, theo dõi website và máy chủ, cũng như cung câp thông tin thống kê về tình trạng và xu hương mạng.
  [netcraft](https://sitereport.netcraft.com)

## Commands

### Hướng dẫn lệnh

##### Cung cấp thông tin chi tiết về cách sử dụng lệnh và các tùy chọn liên quan

```bash
###
### Cú pháp
###
man tên_lệnh

# Xem hướng dẫn về lệnh "man"
man man

# Xem hướng dẫn về lệnh "id"
man id

# Xem hướng dẫn về lệnh "ls"
man ls

# Xem hướng dẫn về tập tin cấu hình "/etc/hosts"
man 5 hosts

# More commands ...
```

### Các lệnh file system

##### Xác định vị trí đứng hiện tại

```bash
pwd
```

##### Di chuyển tới thư mục được chỉ dẫn path

```bash
# Di chuyển tới thư mục root
cd

# Di chuyển tới vị trí thư mục chỉ định
## Đường dẫn tuyệt đối (có thêm dấu / trước tên thư mục)
cd /
cd /home
cd /usr/nginx/share/html #

## Đường dẫn tương đối
cd usr
cd etc
cd tên_thư_mục
cd thư_mục_cha/thư_mục_con


# Back lại thư mục cha
cd ..

# More commands ...
```

##### Xem danh sách thư mục, file tại vị trí đứng hiện tại

```bash
# Chỉ hiện thị danh sách các thành phần có tại vị trí đứng hiện tại
ls

# Hiển thị danh sách chi tiết, bao gồm quyền truy cập, số lượng liên kết, chủ sở hữu, nhóm, kích thước, và thời gian sửa đổi của tập tin/thư mục.
ls -l / ll

# Hiển thị tất cả các tập tin và thư mục, bao gồm cả các tập tin/thư mục ẩn (bắt đầu bằng dấu chấm).
ls -a

# Hiển thị kích thước tập tin/thư mục dưới dạng dễ đọc (ví dụ: KB, MB, GB).
ls -h

# Sắp xếp danh sách theo thời gian sửa đổi, từ mới đến cũ.
ls -t

# Đảo ngược thứ tự của danh sách.
ls -r

# Sắp xếp danh sách theo kích thước, từ lớn đến nhỏ.
ls -S

# Hiển thị danh sách chi tiết và các thư mục con.
ls -lR

# Hiển thị số inode của mỗi tập tin/thư mục.
ls -i

# Hiển thị danh sách với màu sắc, giúp phân biệt tập tin và thư mục.
ls --color

#Hiển thị hướng dẫn ngắn về cách sử dụng lệnh "ls" và các tùy chọn.
ls --help

# Example
ls -lstra
```

### Một vài thủ thuật hữu ích khi gõ lệnh

##### Clear màn hình

```bash
clear (Ctrl + l)
```

##### Tìm kiếm lịch sử lệnh

```bash
Ctrl + r
```

##### Xem lịch sử lệnh

```bash
history
```

##### Thực thi nhanh câu lệnh trong history

```bash
! stt_lich_su_lenh

# Example, thực thi câu lệnh có số stt 49 trong lịch sử
!49
```

### Tạo xóa thư mục, file

##### Tạo thư mục

```bash
# Tạo thư mục
mkdir tên_thư_mục

# Tạo nhiều thư mục cùng lúc
mkdir exam lesson demo test
mkdir folder{1,2,3} # mkdir folder1 folder2 folder3

# Tạo thư mục với thư mục con
mkdir -p lesson/lesson1

```

##### Tạo file

```bash
# Tạo file
touch tên_file

# Tạo nhiều file cùng lúc
touch exam.txt test.txt
touch exam{1,2,3}.txt
touch exam{1,2,3}.csv
```

##### Xóa thư mục, file

```bash
# Xóa file
rm tên_file
rm -f tên_file # bắt buộc

# Xóa thư mục
rm -r tên_thư_mục
rm -rf tên_thư_mục # bắt buộc
```

### Copy, di chuyển, đổi tên file và thư mục

##### Copy file và thư mục

```bash
# Copy file
cp tên_file_nguồn tên_thư_mục_đích

# Copy thư mục
cp -r tên_thư_mục_nguồn tên_thư_mục_đích

# Example

Giả định: thư mục test và demo thuộc thư mục root

## Copy thư mục test vào thư mục demo
cp /test /demo

## Copy file test.txt trong thư mục test vào thư mục demo
cp /test/test.txt /demo

```

##### Di chuyển file, thư mục

```bash
mv tên_file_nguồn/tên_thư_mục_nguồn /tên_thư_mục_đích

```

##### Đổi tên file, thư mục

```bash
mv tên_file_ban_đầu/tên_thư_mục_ban_đầu tên_file_thay_đổi/tên_thư_mục_thay_đổi
```

### Các kiểu đọc nội dung

```bash
# Đọc toàn bộ file
cat tên_file

# Đọc file với chế độ cuộn từng phần
more tên_file

# Đọc file với có chế độ tìm kiếm, ...
less tên_file

# Đọc file hiển thị những nội ở đầu file
head tên_file
head -n 5 tên_file # Đọc file hiển thị 5 dòng đầu tiên của file

# Đọc file hiển thị những nội dung cuối file
tail tên_file
tail -n 5 tên_file # Đọc file hiện thị 5 dòng cuối của file
tail -f tên_file # Đọc file với chế độ real mode (nội dung thay đổi sẽ được cập nhật liên tục)
```
