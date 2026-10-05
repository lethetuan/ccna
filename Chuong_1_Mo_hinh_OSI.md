\# CHƯƠNG 1: Mô hình OSI \[cite: 39\]

\#\# Giới thiệu \[cite: 39\]  
\*\*Mở rộng mạng lưới\*\* \[cite: 39\]  
Một trong những điều chúng ta làm khi học các chủ đề mới, nâng cao kiến thức hiện có, hoặc khi nhằm áp dụng sự hiểu biết thực tế của mình, xảy ra trong hành động mở rộng mạng lưới. \[cite: 39\] Theo một cách nào đó, chúng ta là những người đánh cá tiềm năng đang khám phá những kiến thức mới để nuôi dưỡng tâm trí. \[cite: 39\]

Đây là thế giới của mạng máy tính. \[cite: 39\]  
Nếu mục đích của bạn khi học về mạng là trở thành một quản trị viên mạng, chuẩn bị tham gia kỳ thi CompTIA Network+ hoặc nâng cao kiến thức và kỹ năng thực tế hiện có của bạn, thì cuốn sách này là dành cho bạn. \[cite: 39, 40\]

\#\# Cấu trúc \[cite: 40\]  
Chương này sẽ bao gồm các chủ đề sau: \[cite: 40\]  
\* Nhu cầu về các tiêu chuẩn. \[cite: 40\]  
\* Mô hình OSI. \[cite: 40\]  
\* Bảy tầng của mô hình OSI. \[cite: 40\]  
\* Đóng gói và mở gói dữ liệu (trong bối cảnh của mô hình OSI). \[cite: 40\]

\#\# Mục tiêu \[cite: 40\]  
Sau khi đọc chương này, bạn sẽ có thể so sánh và đối chiếu các tầng của mô hình OSI. \[cite: 40\] Bạn cũng sẽ có thể hiểu các kiến trúc giao thức và đánh giá cao sự cần thiết của các tiêu chuẩn và giao thức, chia nhỏ chức năng tổng thể của việc truyền dữ liệu thành các phần cấu thành của nó. \[cite: 40\]

\#\# Nhu cầu về các tiêu chuẩn \[cite: 40\]  
Thường thì khi các hệ thống truyền thông mới xuất hiện và phát triển, sự phát triển của chúng không nhất thiết được phân bổ đồng đều. \[cite: 40\] Ba từ quan trọng liên quan đến việc thiết lập tiêu chuẩn trong mạng máy tính là: khả năng tương tác (interoperability), khả năng tương thích (compatibility) và khả năng mở rộng (scalability). \[cite: 41\]

\#\# Tiêu chuẩn và Giao thức \[cite: 41\]  
Các tiêu chuẩn tổ chức chủ yếu áp dụng cho con người: những gì họ tạo ra, sản xuất, thiết kế, kỹ thuật và xây dựng. \[cite: 41\] Giao thức, khi theo đuổi mạng, liên quan cụ thể đến dữ liệu. \[cite: 41\] Một giao thức mạng là một tập hợp các quy tắc để định dạng và xử lý dữ liệu. \[cite: 41\]

\#\# Mô hình OSI \[cite: 42\]  
Mô hình Hệ thống Mở Tương hỗ (OSI) được phát triển vào những năm 1970 bởi Tổ chức Tiêu chuẩn hóa Quốc tế (ISO) và được thông qua như một tiêu chuẩn quốc tế vào năm 1984\. \[cite: 42\] Nó được chia thành bảy tầng: \[cite: 42\]  
\* Tầng 1: Tầng vật lý (Physical). \[cite: 43\]  
\* Tầng 2: Tầng liên kết dữ liệu (Data link). \[cite: 43\]  
\* Tầng 3: Tầng mạng (Network). \[cite: 43\]  
\* Tầng 4: Tầng giao vận (Transport). \[cite: 43\]  
\* Tầng 5: Tầng phiên (Session). \[cite: 43\]  
\* Tầng 6: Tầng trình diễn (Presentation). \[cite: 43\]  
\* Tầng 7: Tầng ứng dụng (Application). \[cite: 43\]

\#\# Các đơn vị dữ liệu giao thức (Protocol data units \- PDU) \[cite: 45\]  
PDU là một thuật ngữ OSI đề cập đến một nhóm thông tin được thêm vào hoặc xóa đi bởi một tầng của mô hình OSI. \[cite: 45\]  
\* Ở Tầng 1, PDU là một bit. \[cite: 45\]  
\* Ở Tầng 2, nó là một frame (khung). \[cite: 45\]  
\* Ở Tầng 3, nó là một packet (gói tin). \[cite: 45\]  
\* Ở Tầng 4, nó là một segment (phân đoạn). \[cite: 45\]  
\* Ở Tầng 5 trở lên, PDU được gọi là data (dữ liệu). \[cite: 45\]

\#\# Bảy tầng của mô hình OSI \[cite: 49\]  
\* \*\*Tầng vật lý\*\*: Chịu trách nhiệm truyền và nhận các luồng bit thô qua môi trường vật lý. \[cite: 49\]  
\* \*\*Tầng liên kết dữ liệu\*\*: Chức năng chính là truyền dữ liệu đáng tin cậy giữa hai node được kết nối bởi tầng vật lý, sử dụng địa chỉ MAC. \[cite: 52\]  
\* \*\*Tầng mạng\*\*: Chức năng chính là cấu trúc và quản lý mạng đa node, định tuyến các gói tin bằng địa chỉ IP. \[cite: 53, 54\]  
\* \*\*Tầng giao vận\*\*: Truyền đáng tin cậy các segment dữ liệu giữa các điểm trên mạng. \[cite: 55\]  
\* \*\*Tầng phiên\*\*: Quản lý và đồng bộ hóa các cuộc hội thoại giữa hai hệ thống giao tiếp. \[cite: 57\]  
\* \*\*Tầng trình diễn\*\*: Dịch thuật dữ liệu giữa dịch vụ mạng và ứng dụng, bao gồm mã hóa và nén. \[cite: 58\]  
\* \*\*Tầng ứng dụng\*\*: Cung cấp các API cấp cao, bao gồm chia sẻ tài nguyên và truy cập tệp từ xa (Ví dụ: HTTP, FTP). \[cite: 59, 60\]

\#\# Đóng gói và mở gói dữ liệu \[cite: 60, 61\]  
Đóng gói (Encapsulation) mô tả quá trình đặt các header (và đôi khi là trailer) xung quanh dữ liệu khi nó đi từ tầng cao xuống tầng thấp. \[cite: 61\] Quá trình ngược lại là mở gói (decapsulation), đề cập đến các lớp dữ liệu liên tiếp bị loại bỏ ở đầu nhận của mạng khi dữ liệu đi từ dưới lên. \[cite: 61, 65\]
