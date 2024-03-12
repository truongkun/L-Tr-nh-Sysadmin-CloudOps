# Kiểm tra dung lượng disk

## DF

- Lệnh df viết tắt của “disk filesystem“, nó được dùng để lấy toàn bộ thông tin về lượng ổ cứng khả dụng và lượng ổ cứng đã dùng của các file hệ thống trên linux
    **Một số option quan trọng:**

    - `df -h` : hiển thị theo format dung lượng K,M,G

    - `df -i` : hiển thị theo format inodes

## DU

- Lệnh du là viết tắt của từ “disk usage” là một công cụ dòng lệnh được cung cấp bởi Linux, nhằm báo cáo dung lượng ổ đĩa được sử dụng bởi các thư mục và file. Đây là công cụ chính để phân tích không gian ổ đĩa trong dòng lệnh.
    
    **Một số option quan trọng:**

    - `du -h `: hiển thị theo format dung lượng K,M,G

    - `du -shc` : hiển thị tổng dung lượng

## So sánh `du` và `df`

|Chức năng       |du (Disk Usage)|df (Disk Free)|
|:---------------|:---------------|:------------|
|Mục đích        |Đo lường dung lượng thực sự của tệp và thư mục|Hiển thị thông tin về dung lượng của hệ thống tệp|
|Đơn vị đo       |Thường hiển thị dung lượng trong bytes hoặc các đơn vị khác (kilo, mega, giga)|Thường hiển thị dung lượng trong blocks hoặc các đơn vị tương tự|
|Phạm vi         |Dùng để đo lường dung lượng của các thư mục và tệp cụ thể|Hiển thị thông tin về dung lượng của toàn bộ hệ thống tệp|
|Thông tin cụ thể|Hiển thị dung lượng của các thư mục và tệp cụ thể|Hiển thị tổng dung lượng, dung lượng sử dụng, dung lượng còn trống và phân bổ trên các hệ thống tệp khác nhau|
|Ví dụ           |du -sh /<thư/mục>|	df -h|

## Điểm chính khác biệt giữa `du và df` là `mục đích sử dụng`.` 
- `du` được sử dụng để đo lường dung lượng của các thư mục và tệp cụ thể trong hệ thống tệp,
- `df` được sử dụng để hiển thị tổng quan về dung lượng, dung lượng sử dụng và dung lượng còn trống trên toàn bộ hệ thống tệp.