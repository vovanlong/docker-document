# Cách lệnh thường dùng trong DockerFile

## FROM

Cú Pháp:  

```bash
  FROM <base_image>:<phiên_bản>
```

- Khởi nguồn từ image nào?
- Tải nếu chưa có trong local registry
- Là lệnh đầu tiên trong local registry

## Maintainer

Cú Pháp:  

```bash
  MAINTAINER <tên_tác_giả>
```

- Khai báo tác giả của dockerfile

## RUN

Cú Pháp:  

```bash
  RUN <câu_lệnh>
```

- Chúng ta sử dụng lệnh này để chạy một command cho việc cài đặt các công cụ cần thiết cho Image của chúng ta.

## CMD

Cú Pháp:  

```bash
  CMD <câu_lệnh>
```

- Chúng ta sử dụng lệnh này để chạy một command cho việc cài đặt các công cụ cần thiết cho Image của chúng ta.

## ADD

Cú Pháp

```bash
  CMD <src> <dest>
```

- Câu lệnh này dùng để copy một tập tin local hoặc remote nào đó vào một vị trí nào đó trên Container.

## ENTRYPOINT

Cú Pháp

```bash
  ENTRYPOINT <câu_lệnh>
```

- Định nghĩa biến môi trường trong Container.

## ENV

Cú Pháp

```bash
  ENV <tên_biến>
```

- Định nghĩa biến môi trường trong Container.

## VOLUME

Cú Pháp

```bash
  VOLUME <tên_thư_mục>
```

Dùng để truy cập hoặc liên kết một thư mục nào đó trong Container.
Có 2 loại VOLUME:

- Volume giữa host và container
- Volume giữa các container

ví dụ

```bash
volumes:
      - ./postgres-data:/var/lib/postgresql/data
or

volumes: ./postgres-data
```
