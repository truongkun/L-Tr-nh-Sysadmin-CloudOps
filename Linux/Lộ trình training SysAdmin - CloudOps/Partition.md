# Linux Partition
- Một phân vùng (partition) trong hệ thống máy tính là một phần của ổ đĩa vật lý được chia thành các phần riêng biệt. Mỗi phân vùng có thể được sử dụng như một ổ đĩa độc lập với các phân vùng khác, có thể chứa hệ thống tệp và dữ liệu của riêng mình.

- Dưới đây là một số khái niệm cơ bản liên quan đến phân vùng:

  - **Dung lượng**: Mỗi phân vùng có dung lượng riêng của nó, được đo bằng đơn vị như gigabyte (GB) hoặc terabyte (TB).

  - **Loại phân vùng**: Có nhiều loại phân vùng khác nhau, bao gồm phân vùng hệ thống (system partition), phân vùng dữ liệu (data partition), phân vùng trao đổi (swap partition), và phân vùng khôi phục (recovery partition).

  - **Hệ thống tệp**: Mỗi phân vùng thường được định dạng với một loại hệ thống tệp cụ thể như ext4, NTFS, FAT32, và APFS. Hệ thống tệp xác định cách dữ liệu được tổ chức và lưu trữ trên phân vùng.

  - **Mount point**: Mỗi phân vùng có thể được gắn kết với một điểm gắn kết (mount point) trong hệ thống tệp của hệ điều hành, cho phép truy cập vào nội dung của phân vùng thông qua đường dẫn thư mục.

  - **Quản lý phân vùng**: Quá trình tạo, xóa, thay đổi kích thước và quản lý phân vùng thường được thực hiện bằng các công cụ như fdisk, gparted, hoặc các tiện ích quản lý ổ đĩa tích hợp trong hệ điều hành.

Phân vùng là một phần quan trọng của cách tổ chức và quản lý dữ liệu trên các ổ đĩa vật lý và là một phần không thể thiếu của việc cài đặt và sử dụng hệ thống máy tính.

## 2) Quản lý Partition
### **2.1 ) `fdisk`**
- Chỉ để tạo phân vùng dưới `2TB`
- Chỉ hỗ trợ ổ cứng chuẩn **MBR** 
- Cấu trúc lệnh :
    ```
    # fdisk [options] [/dev/...]
    ```
    - **Options :** `-l` : liệt kê tất cả các ổ cứng và các partition
    - **Command** sử dụng trong lệnh :
        - `n` : tạo mới 1 partition
        - `p` : hiển thị **partition table**
        - `q` : thoát mà không lưu thay đổi
        - `w` : lưu thay đổi và thoát
        - `d` : xóa 1 partition


## Phân biệt giữa file system và partition và mối liên hệ giữa chúng trong một máy chủ:

|Thuật ngữ|Miêu tả|Mối quan hệ trên máy chủ|
|:--------|:------|:-----------------------|
|Partition|Một phân vùng là một phần của ổ đĩa vật lý được chia thành các phần riêng biệt. Mỗi phân vùng có dung lượng và hệ thống tệp riêng của mình.|Trên máy chủ, ổ đĩa vật lý thường được chia thành các phân vùng khác nhau để tổ chức dữ liệu và hệ thống tệp.|
|File System|Hệ thống tệp là cách dữ liệu được tổ chức và lưu trữ trên một phân vùng. Nó định nghĩa cách thức truy cập, đọc và ghi dữ liệu vào ổ đĩa. Mỗi hệ thống tệp có một định dạng và tính năng riêng của mình.|Mỗi phân vùng trên máy chủ được định dạng với một hệ thống tệp cụ thể như ext4, NTFS, hoặc XFS. Hệ thống tệp quyết định cách dữ liệu được tổ chức và truy cập trên phân vùng tương ứng.|
|Mối quan hệ| Một phân vùng phải được định dạng với một hệ thống tệp cụ thể để có thể sử dụng được. Hệ thống tệp xác định cách dữ liệu được tổ chức và quản lý trên phân vùng tương ứng.|Mỗi phân vùng trên máy chủ có một hệ thống tệp được gắn kết với nó. Hệ thống tệp này quyết định cách dữ liệu được tổ chức và quản lý trên phân vùng tương ứng.|

Trên một máy chủ, `partition` là cách chia ổ đĩa vật lý thành các phần riêng biệt, trong khi `file system` là cách dữ liệu được tổ chức và quản lý trên từng phân vùng. 

Mỗi phân vùng phải có một hệ thống tệp cụ thể để có thể sử dụng được, và hệ thống tệp này sẽ quyết định cách dữ liệu được tổ chức và truy cập trên phân vùng tương ứng.