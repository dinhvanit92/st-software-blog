# Documentation
## Install

**1. Clone file ghost về máy chủ host bằng dòng lệnh:**

```
git clone https://github.com/dinhvanit92/st-software-blog.git
```
**2. Đến thư mục chưa file Dockerfile sửa đường dẫn hiển thị**

```cd ghost```
Vào file Dockerfile bằng dòng lệnh: 

```sudo nano Dockerfile```

Tìm đến dòng 33 thay `http://localhost:2368` thành tên domain của bạn; ví dụ: `http://trandinhvan.com:2368` sau đó lưu file 

**3. Cấp quyền cho file `docker-entrypoint.sh` bằng dòng lệnh.**

```
chmod 755 docker-entrypoint.sh
```
**4. Tạo Image GHOST**

`cd` đến thư mục chứa file `Dockerfile` và chạy dòng lệnh:

```
docker build -t stsoftware:v1 -f Dockerfile .
```

**5. Tạo và chạy Container GHOST**

```
docker run -it -d --name stsoftware -h vghost -p 80:2368 stsoftware:v1
```

**CÀI ĐẶT THÀNH CÔNG**
