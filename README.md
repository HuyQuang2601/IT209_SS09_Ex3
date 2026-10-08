# Bài 3: Đóng gói trang HTML tĩnh với Nginx

## Build image

Chạy các lệnh sau trong thư mục `homework/session_09/ex3/`:

```bash
docker build -t my-html-app:v1 .
```

## Khởi chạy container

```bash
docker run -d -p 8081:80 --name html-app my-html-app:v1
```

## Kiểm tra

```bash
curl http://localhost:8081
```

Kết quả mong đợi:

```html
<h1>Hello Docker Session 09!</h1>
```

## Dừng và xóa container

```bash
docker stop html-app
docker rm html-app
```
