# Documentation
## Install

**1. Clone file ghost về máy chủ host bằng dòng lệnh:**

```
git clone https://github.com/dinhvanit92/st-software-blog.git
```
**2. Đến thư mục chưa file Dockerfile**

```cd ghost```

**3. Cấp quyền cho file `docker-entrypoint.sh` bằng dòng lệnh.**

```
chmod 755 config/docker-entrypoint.sh
```
**4. Tạo Image GHOST**

`cd` đến thư mục chứa file `Dockerfile` và chạy dòng lệnh:

```
docker build -t stsoftware:v1 -f Dockerfile .
```

**5. Tạo Container GHOST**

```
docker run -it --name stsoftware -h vghost -p 80:2368 stsoftware:v1
```

**CÀI ĐẶT THÀNH CÔNG**
