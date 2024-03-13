# RSYNC và SCP

Trong Linux, `rsync` và `scp` đều là các công cụ dùng để sao chép dữ liệu từ một máy tính sang máy tính khác qua mạng. Tuy nhiên, chúng có một số điểm khác biệt:

## RSYNC là gì?

   - `rsync` là một `công cụ mạnh mẽ cho việc sao chép và đồng bộ hóa dữ liệu giữa các máy tính,` thường được sử dụng `để sao chép dữ liệu ở xa hoặc đồng bộ hóa dữ liệu giữa các thư mục cục bộ và từ xa.`
   - Nó cung cấp nhiều tính năng như `sao chép theo tệp tin mới hơn hoặc đã được thay đổi, nén dữ liệu trước khi chuyển, và giảm bớt băng thông` bằng cách chỉ chuyển dữ liệu đã thay đổi.
   - Cú pháp cơ bản của `rsync` như sau:
     ```
     rsync [tùy chọn] nguồn đích
     ```

## SCP là gì?

   - `scp` (Secure Copy Protocol) cũng là một `công cụ dùng để sao chép dữ liệu giữa các máy tính, nhưng nó được sử dụng chủ yếu cho việc truyền dữ liệu qua mạng một cách an toàn bằng cách sử dụng SSH (Secure Shell).`
   - `scp` thường được sử dụng `khi cần sao chép một hoặc một số tệp tin hoặc thư mục từ hoặc đến một máy tính từ xa.`
   - Cú pháp cơ bản của `scp` như sau:
     ```
     scp [tùy chọn] nguồn đích
     ```

Tóm lại, cả hai công cụ đều được sử dụng để sao chép dữ liệu giữa các máy tính trong mạng, nhưng `rsync` thường được ưa chuộng hơn khi cần đồng bộ hóa dữ liệu và quản lý sao chép dữ liệu lớn, trong khi `scp` thích hợp cho việc truyền dữ liệu an toàn một cách đơn giản.