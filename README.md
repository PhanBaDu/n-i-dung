# CHỨC NĂNG HIỂN THỊ SẢN PHẨM

_Dựa trên tài liệu yêu cầu KH-20_RO.MD - Chức năng hiển thị sản phẩm của User_

## MỤC LỤC

1. [Hiển thị danh sách sản phẩm](#1-hiển-thị-danh-sách-sản-phẩm)
   - 1.1 [Trang chủ - Sản phẩm nổi bật](#11-trang-chủ---sản-phẩm-nổi-bật)
   - 1.2 [Trang danh sách sản phẩm](#12-trang-danh-sách-sản-phẩm)
   - 1.3 [Hiển thị chi tiết sản phẩm](#13-hiển-thị-chi-tiết-sản-phẩm)

---

## 1. HIỂN THỊ DANH SÁCH SẢN PHẨM

### 1.1 TRANG CHỦ - SẢN PHẨM NỔI BẬT

#### 1.1.1 Thông tin màn hình:

| Screen        | Trang chủ - Sản phẩm nổi bật                                                              |
| ------------- | ----------------------------------------------------------------------------------------- |
| Description   | Hiển thị các sản phẩm mô hình nổi bật, danh mục sản phẩm và thanh tìm kiếm trên trang chủ |
| Screen Access | User truy cập **/user** hoặc click vào logo/trang chủ                                     |

#### 1.1.2 Chi tiết thành phần màn hình:

| Item                  | Type           | Data                                                                                      | Description                                       |
| --------------------- | -------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------- |
| **Hero Section**      | Banner         | Chào mừng đến với Model Shop<br>Khám phá bộ sưu tập mô hình đa dạng                       | Khu vực chào mừng và giới thiệu chính             |
| **Tiêu đề chính**     | Text           | Chào mừng đến với Model Shop                                                              | Tiêu đề chính của trang chủ                       |
| **Mô tả**             | Text           | Khám phá bộ sưu tập mô hình đa dạng từ Gundam, Figure đến mô hình xe và máy bay           | Mô tả ngắn gọn về dịch vụ                         |
| **Nút Xem sản phẩm**  | Button         |                                                                                           | Nút chuyển đến trang danh sách sản phẩm           |
| **Nút Tìm kiếm**      | Button         |                                                                                           | Nút chuyển đến trang tìm kiếm                     |
| **Thanh tìm kiếm**    | Input + Button | Tìm kiếm sản phẩm, thương hiệu, series...                                                 | Ô nhập từ khóa tìm kiếm                           |
| **Danh mục sản phẩm** | Card Grid      | Gundam (45), Figure (32), Mô hình xe (28), Máy bay (15)                                   | Hiển thị các danh mục chính với số lượng sản phẩm |
| **Tên danh mục**      | Text           | Gundam, Figure, Mô hình xe, Máy bay                                                       | Tên của từng danh mục sản phẩm                    |
| **Số lượng sản phẩm** | Text           | 45 sản phẩm, 32 sản phẩm, 28 sản phẩm, 15 sản phẩm                                        | Số lượng sản phẩm trong mỗi danh mục              |
| **Icon danh mục**     | Icon           | Package, Star, TrendingUp, Bell                                                           | Icon đại diện cho từng danh mục                   |
| **Sản phẩm nổi bật**  | Card Grid      | 4 sản phẩm được hiển thị                                                                  | Danh sách các sản phẩm được đánh dấu nổi bật      |
| **Tên sản phẩm**      | Text           | Gundam RX-78-2, Figure Naruto Uzumaki, Model Xe Ferrari F40, Máy bay F-16 Fighting Falcon | Tên của sản phẩm                                  |
| **Thương hiệu**       | Text           | Bandai, Good Smile Company, Tamiya, Revell                                                | Thương hiệu sản xuất sản phẩm                     |
| **Giá hiện tại**      | Text           | 1.200.000đ, 2.500.000đ, 800.000đ, 600.000đ                                                | Giá bán hiện tại của sản phẩm                     |
| **Giá gốc**           | Text           | 1.500.000đ, 3.000.000đ, 1.000.000đ, 750.000đ                                              | Giá gốc trước khi giảm giá (có gạch ngang)        |
| **Đánh giá**          | Stars + Text   | 4.8 (156), 4.9 (89), 4.7 (203), 4.6 (134)                                                 | Điểm đánh giá và số lượng đánh giá                |
| **Badge sản phẩm**    | Badge          | Hot, New, Sale, Limited                                                                   | Nhãn đặc biệt cho sản phẩm                        |
| **Hình ảnh sản phẩm** | Image          | /sg-11134201-7rcel-lsbarszebn5jda.webp, ...                                               | Hình ảnh đại diện của sản phẩm                    |
| **Nút Yêu thích**     | Button (Icon)  | Heart icon                                                                                | Nút thêm/xóa sản phẩm khỏi danh sách yêu thích    |
| **Nút Xem chi tiết**  | Button         | Xem chi tiết                                                                              | Nút chuyển đến trang chi tiết sản phẩm            |
| **Hành động nhanh**   | Card Grid      | Giỏ hàng (3 sản phẩm), Yêu thích (12 sản phẩm), Thông báo (5 thông báo mới)               | Các chức năng nhanh với số liệu thống kê          |

#### 1.1.3 Hành động và xử lý:

| Action Name               | Description                                                                                                                                                                                                                                                                | Success                                                                                                                  | Failure                                                                                 |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| **Hiển thị trang chủ**    | Hiển thị trang chủ với các sản phẩm nổi bật, danh mục sản phẩm và thanh tìm kiếm. Trang chủ cung cấp cái nhìn tổng quan về cửa hàng và các sản phẩm phổ biến. Người dùng có thể nhanh chóng truy cập các chức năng chính như xem sản phẩm, tìm kiếm hoặc quản lý giỏ hàng. | Trang chủ hiển thị đầy đủ thông tin. Các sản phẩm nổi bật được load thành công. Danh mục và thống kê hiển thị chính xác. | Không thể tải dữ liệu sản phẩm. Lỗi hiển thị danh mục. Thống kê không chính xác.        |
| **Tìm kiếm sản phẩm**     | Cho phép người dùng tìm kiếm sản phẩm trực tiếp từ trang chủ bằng cách nhập từ khóa vào thanh tìm kiếm. Hệ thống sẽ chuyển hướng đến trang kết quả tìm kiếm với các sản phẩm phù hợp. Tìm kiếm hỗ trợ tên sản phẩm, thương hiệu, series và các từ khóa liên quan.          | Chuyển hướng đến trang tìm kiếm thành công. Kết quả tìm kiếm hiển thị chính xác theo từ khóa.                            | Từ khóa tìm kiếm không hợp lệ. Không tìm thấy sản phẩm phù hợp. Lỗi chuyển hướng trang. |
| **Xem danh mục sản phẩm** | Cho phép người dùng click vào các danh mục sản phẩm để xem tất cả sản phẩm trong danh mục đó. Mỗi danh mục hiển thị số lượng sản phẩm và icon đại diện. Khi click vào danh mục, hệ thống sẽ lọc và hiển thị các sản phẩm thuộc danh mục đó.                                | Chuyển hướng đến trang sản phẩm với bộ lọc danh mục. Hiển thị đúng các sản phẩm thuộc danh mục đã chọn.                  | Danh mục không tồn tại. Không có sản phẩm trong danh mục. Lỗi khi áp dụng bộ lọc.       |

### 1.2 TRANG DANH SÁCH SẢN PHẨM

#### 1.2.1 Thông tin màn hình:

| Screen        | Danh sách sản phẩm                                                               |
| ------------- | -------------------------------------------------------------------------------- |
| Description   | Hiển thị tất cả mô hình có sẵn và các sản phẩm chưa ra mắt với bộ lọc và sắp xếp |
| Screen Access | User truy cập **/user/products** hoặc click "Xem sản phẩm" từ trang chủ          |

#### 1.2.2 Chi tiết thành phần màn hình:

| Item                     | Type           | Data                                                                       | Description                                |
| ------------------------ | -------------- | -------------------------------------------------------------------------- | ------------------------------------------ |
| **Tiêu đề trang**        | Text           | Sản phẩm                                                                   | Tiêu đề chính của trang danh sách sản phẩm |
| **Thanh tìm kiếm**       | Input + Button | Tìm kiếm sản phẩm...                                                       | Ô nhập từ khóa tìm kiếm                    |
| **Bộ lọc bên trái**      | Sidebar        | Danh mục, Thương hiệu, Khoảng giá, Đánh giá                                | Panel bộ lọc các tiêu chí                  |
| **Danh mục**             | Checkbox Group | Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Khác                          | Lọc sản phẩm theo danh mục                 |
| **Thương hiệu**          | Checkbox Group | Tất cả, Bandai, Good Smile Company, Tamiya, Hasegawa, Revell, Max Factory  | Lọc sản phẩm theo thương hiệu              |
| **Khoảng giá**           | Slider         | 0đ - 5.000.000đ                                                            | Lọc sản phẩm theo khoảng giá               |
| **Đánh giá**             | Radio Group    | Tất cả, 4 sao trở lên, 3 sao trở lên, 2 sao trở lên, 1 sao trở lên         | Lọc sản phẩm theo mức đánh giá             |
| **Tình trạng hàng**      | Checkbox Group | Đang bán, Chưa ra mắt, Hết hàng                                            | Lọc sản phẩm theo tình trạng               |
| **Thanh công cụ**        | Toolbar        | Sắp xếp, Chế độ xem, Số sản phẩm hiển thị                                  | Các công cụ điều khiển hiển thị            |
| **Sắp xếp**              | Select         | Liên quan, Giá thấp đến cao, Giá cao đến thấp, Đánh giá cao nhất, Mới nhất | Lựa chọn tiêu chí sắp xếp                  |
| **Chế độ xem**           | Toggle Group   | Grid (lưới), List (danh sách)                                              | Chuyển đổi giữa chế độ hiển thị            |
| **Số sản phẩm hiển thị** | Select         | 12, 24, 48, 96 sản phẩm/trang                                              | Lựa chọn số lượng sản phẩm hiển thị        |
| **Danh sách sản phẩm**   | Grid/List      | Hiển thị sản phẩm theo chế độ đã chọn                                      | Khu vực hiển thị danh sách sản phẩm        |
| **Card sản phẩm**        | Card           | Thông tin sản phẩm trong từng card                                         | Thẻ hiển thị thông tin một sản phẩm        |
| **Hình ảnh sản phẩm**    | Image          | Hình ảnh đại diện của sản phẩm                                             | Ảnh chính của sản phẩm                     |
| **Tên sản phẩm**         | Text           | Tên đầy đủ của sản phẩm                                                    | Tiêu đề sản phẩm                           |
| **Thương hiệu**          | Text           | Tên thương hiệu sản xuất                                                   | Thương hiệu của sản phẩm                   |
| **Series**               | Text           | Tên series/series                                                          | Series mà sản phẩm thuộc về                |
| **Scale**                | Text           | Tỷ lệ mô hình (1/144, 1/7, 1/24, 1/72)                                     | Tỷ lệ của mô hình                          |
| **Giá**                  | Text           | Giá bán hiện tại                                                           | Giá sản phẩm                               |
| **Giá gốc**              | Text           | Giá gốc (có gạch ngang)                                                    | Giá trước khi giảm giá                     |
| **Phần trăm giảm giá**   | Badge          | -26%, -17%, -20%, -20%                                                     | Phần trăm giảm giá                         |
| **Đánh giá**             | Stars + Text   | 4.8 (1250), 4.6 (890), 4.7 (650), 4.5 (420)                                | Điểm đánh giá và số lượng đánh giá         |
| **Mô tả ngắn**           | Text           | Mô tả ngắn gọn về sản phẩm                                                 | Mô tả sản phẩm                             |
| **Số lượng tồn kho**     | Text           | Còn 50, Còn 30, Còn 25, Còn 40                                             | Số lượng sản phẩm còn trong kho            |
| **Badge đặc biệt**       | Badge          | New, Bestseller, Hot, Limited                                              | Nhãn đặc biệt cho sản phẩm                 |
| **Nút Yêu thích**        | Button (Icon)  | Heart icon                                                                 | Nút thêm/xóa khỏi danh sách yêu thích      |
| **Nút Thêm giỏ hàng**    | Button (Icon)  | ShoppingCart icon                                                          | Nút thêm sản phẩm vào giỏ hàng             |
| **Nút Xem chi tiết**     | Button         | Xem chi tiết                                                               | Nút chuyển đến trang chi tiết sản phẩm     |
| **Phân trang**           | Pagination     | Trang 1/10, Hiển thị 1-12 của 120 sản phẩm                                 | Điều hướng giữa các trang                  |
| **Nút Trang trước**      | Button         | ← Trang trước                                                              | Nút chuyển đến trang trước                 |
| **Nút Trang sau**        | Button         | Trang sau →                                                                | Nút chuyển đến trang sau                   |
| **Số trang**             | Button Group   | 1, 2, 3, ..., 10                                                           | Các nút chuyển đến trang cụ thể            |

#### 1.2.3 Hành động và xử lý:

| Action Name                     | Description                                                                                                                                                                                                                                                                                                                                                                       | Success                                                                                                            | Failure                                                                                             |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| **Hiển thị danh sách sản phẩm** | Hiển thị tất cả sản phẩm mô hình có sẵn và các sản phẩm chưa ra mắt trong một danh sách có thể lọc và sắp xếp. Người dùng có thể xem sản phẩm theo dạng lưới hoặc danh sách, lọc theo danh mục, thương hiệu, khoảng giá và đánh giá. Hệ thống hỗ trợ sắp xếp theo nhiều tiêu chí khác nhau.                                                                                       | Danh sách sản phẩm hiển thị đầy đủ. Bộ lọc hoạt động chính xác. Sắp xếp theo đúng tiêu chí đã chọn.                | Không thể tải danh sách sản phẩm. Bộ lọc không hoạt động. Sắp xếp không chính xác.                  |
| **Lọc sản phẩm**                | Cho phép người dùng lọc danh sách sản phẩm theo các tiêu chí khác nhau bao gồm danh mục (Gundam, Figure, Mô hình xe, Máy bay), thương hiệu (Bandai, Good Smile Company, Tamiya, Hasegawa, Revell, Max Factory), khoảng giá (từ 0đ đến 5.000.000đ), đánh giá (từ 1 đến 5 sao) và tình trạng hàng (đang bán, chưa ra mắt, hết hàng). Bộ lọc có thể kết hợp nhiều tiêu chí cùng lúc. | Sản phẩm được lọc chính xác theo tiêu chí đã chọn. Kết quả lọc hiển thị ngay lập tức. Có thể kết hợp nhiều bộ lọc. | Bộ lọc không hoạt động. Kết quả lọc không chính xác. Không thể kết hợp nhiều bộ lọc.                |
| **Sắp xếp sản phẩm**            | Cho phép người dùng sắp xếp danh sách sản phẩm theo các tiêu chí: Liên quan (mặc định), Giá thấp đến cao, Giá cao đến thấp, Đánh giá cao nhất, Mới nhất. Sắp xếp được áp dụng ngay lập tức và ảnh hưởng đến thứ tự hiển thị sản phẩm.                                                                                                                                             | Sản phẩm được sắp xếp đúng theo tiêu chí đã chọn. Thứ tự hiển thị được cập nhật ngay lập tức.                      | Sắp xếp không hoạt động. Thứ tự hiển thị không thay đổi. Lỗi khi áp dụng tiêu chí sắp xếp.          |
| **Tìm kiếm sản phẩm**           | Cho phép người dùng tìm kiếm sản phẩm theo tên sản phẩm, thương hiệu, series, scale, chất liệu. Tìm kiếm hỗ trợ từ khóa một phần và không phân biệt hoa thường. Kết quả tìm kiếm được hiển thị ngay lập tức trong danh sách sản phẩm.                                                                                                                                             | Kết quả tìm kiếm hiển thị chính xác. Tìm kiếm nhanh và chính xác. Hỗ trợ tìm kiếm một phần từ khóa.                | Không tìm thấy sản phẩm phù hợp. Tìm kiếm chậm hoặc không phản hồi. Lỗi khi xử lý từ khóa tìm kiếm. |
| **Thay đổi chế độ xem**         | Cho phép người dùng chuyển đổi giữa chế độ hiển thị lưới (grid) và danh sách (list). Chế độ lưới hiển thị sản phẩm dưới dạng card với hình ảnh lớn, phù hợp để duyệt nhanh. Chế độ danh sách hiển thị sản phẩm dưới dạng hàng với thông tin chi tiết hơn, phù hợp để so sánh.                                                                                                     | Chế độ xem được thay đổi thành công. Giao diện hiển thị phù hợp với chế độ đã chọn. Dữ liệu được bảo toàn.         | Không thể thay đổi chế độ xem. Giao diện hiển thị không đúng. Dữ liệu bị mất khi chuyển đổi.        |
| **Phân trang**                  | Chia danh sách sản phẩm thành nhiều trang để dễ dàng duyệt. Người dùng có thể chọn số lượng sản phẩm hiển thị trên mỗi trang (12, 24, 48, 96). Hệ thống cung cấp các nút điều hướng để chuyển giữa các trang và hiển thị thông tin về trang hiện tại.                                                                                                                             | Phân trang hoạt động chính xác. Điều hướng giữa các trang mượt mà. Số lượng sản phẩm hiển thị đúng theo lựa chọn.  | Phân trang không hoạt động. Không thể chuyển trang. Số lượng sản phẩm hiển thị không đúng.          |

### 1.3 HIỂN THỊ CHI TIẾT SẢN PHẨM

#### 1.3.1 Thông tin màn hình:

| Screen        | Chi tiết sản phẩm                                                                                     |
| ------------- | ----------------------------------------------------------------------------------------------------- |
| Description   | Hiển thị các thông tin chi tiết về sản phẩm như hình ảnh, thông số, chất liệu, reviews của khách hàng |
| Screen Access | User click vào sản phẩm từ danh sách hoặc trang chủ, truy cập **/user/products/[id]**                 |

#### 1.3.2 Chi tiết thành phần màn hình:

| Item                    | Type           | Data                                                                      | Description                               |
| ----------------------- | -------------- | ------------------------------------------------------------------------- | ----------------------------------------- |
| **Breadcrumb**          | Navigation     | Trang chủ > Sản phẩm > Gundam RX-78-2                                     | Đường dẫn điều hướng                      |
| **Nút Quay lại**        | Button         | ← Quay lại                                                                | Nút quay về trang trước                   |
| **Khu vực hình ảnh**    | Gallery        | Hình ảnh chính và các hình ảnh phụ                                        | Khu vực hiển thị hình ảnh sản phẩm        |
| **Hình ảnh chính**      | Image          | Hình ảnh lớn của sản phẩm                                                 | Ảnh chính được hiển thị                   |
| **Hình ảnh phụ**        | Thumbnail Grid | Các hình ảnh nhỏ để chọn                                                  | Các ảnh phụ để người dùng chọn xem        |
| **Nút phóng to**        | Button         | Zoom icon                                                                 | Nút phóng to hình ảnh                     |
| **Thông tin sản phẩm**  | Card           | Tên, thương hiệu, giá, đánh giá, mô tả                                    | Card chứa thông tin cơ bản của sản phẩm   |
| **Tên sản phẩm**        | Text           | Gundam RX-78-2                                                            | Tên đầy đủ của sản phẩm                   |
| **Thương hiệu**         | Text           | Bandai                                                                    | Thương hiệu sản xuất                      |
| **Series**              | Text           | Mobile Suit Gundam                                                        | Series mà sản phẩm thuộc về               |
| **Scale**               | Text           | 1/144                                                                     | Tỷ lệ mô hình                             |
| **Danh mục**            | Badge          | Gundam                                                                    | Danh mục sản phẩm                         |
| **Giá hiện tại**        | Text           | 1.200.000đ                                                                | Giá bán hiện tại                          |
| **Giá gốc**             | Text           | 1.500.000đ                                                                | Giá gốc trước khi giảm giá                |
| **Phần trăm giảm giá**  | Badge          | -20%                                                                      | Phần trăm giảm giá                        |
| **Đánh giá**            | Stars + Text   | 4.8 (1250 đánh giá)                                                       | Điểm đánh giá và số lượng đánh giá        |
| **Mô tả ngắn**          | Text           | Mô hình Gundam RX-78-2 kinh điển với thiết kế chi tiết và chất lượng cao. | Mô tả ngắn gọn về sản phẩm                |
| **Số lượng**            | Input Group    | Nút giảm, ô nhập số, nút tăng                                             | Điều khiển số lượng mua                   |
| **Nút Giảm**            | Button         | -                                                                         | Nút giảm số lượng                         |
| **Ô nhập số lượng**     | Input          | 1                                                                         | Ô hiển thị và nhập số lượng               |
| **Nút Tăng**            | Button         | +                                                                         | Nút tăng số lượng                         |
| **Nút Thêm giỏ hàng**   | Button         | Thêm vào giỏ hàng                                                         | Nút thêm sản phẩm vào giỏ hàng            |
| **Nút Mua ngay**        | Button         | Mua ngay                                                                  | Nút chuyển đến trang thanh toán           |
| **Nút Yêu thích**       | Button         | Thêm vào yêu thích                                                        | Nút thêm sản phẩm vào danh sách yêu thích |
| **Nút Chia sẻ**         | Button         | Chia sẻ                                                                   | Nút chia sẻ sản phẩm                      |
| **Thông tin bổ sung**   | Card           | Vận chuyển, Bảo hành, Đổi trả                                             | Thông tin về dịch vụ đi kèm               |
| **Vận chuyển**          | Text + Icon    | Miễn phí vận chuyển cho đơn hàng từ 500.000đ                              | Thông tin về phí vận chuyển               |
| **Bảo hành**            | Text + Icon    | Bảo hành 12 tháng                                                         | Thông tin về chế độ bảo hành              |
| **Đổi trả**             | Text + Icon    | Đổi trả trong 7 ngày                                                      | Thông tin về chính sách đổi trả           |
| **Tabs thông tin**      | Tabs           | Mô tả, Thông số kỹ thuật, Đánh giá, Hỏi đáp                               | Các tab chứa thông tin chi tiết           |
| **Tab Mô tả**           | Tab            | Mô tả chi tiết sản phẩm                                                   | Tab chứa mô tả đầy đủ về sản phẩm         |
| **Mô tả chi tiết**      | Text           | Mô tả đầy đủ về sản phẩm, tính năng, đặc điểm                             | Nội dung mô tả chi tiết                   |
| **Tab Thông số**        | Tab            | Thông số kỹ thuật                                                         | Tab chứa thông số kỹ thuật của sản phẩm   |
| **Bảng thông số**       | Table          | Tỷ lệ, Chiều cao, Chất liệu, Số bộ phận, Độ khó, Độ tuổi                  | Bảng liệt kê các thông số kỹ thuật        |
| **Tỷ lệ**               | Text           | 1/144                                                                     | Tỷ lệ của mô hình                         |
| **Chiều cao**           | Text           | 12.5cm                                                                    | Chiều cao của mô hình                     |
| **Chất liệu**           | Text           | PS (Polystyrene)                                                          | Chất liệu chính của mô hình               |
| **Số bộ phận**          | Text           | 15 bộ phận                                                                | Số lượng bộ phận cần lắp ráp              |
| **Độ khó**              | Text           | Trung bình                                                                | Mức độ khó của việc lắp ráp               |
| **Độ tuổi**             | Text           | 8+ tuổi                                                                   | Độ tuổi phù hợp                           |
| **Tab Đánh giá**        | Tab            | Đánh giá khách hàng                                                       | Tab chứa các đánh giá của khách hàng      |
| **Tổng quan đánh giá**  | Card           | Điểm trung bình, Phân bố sao, Số lượng đánh giá                           | Thông tin tổng quan về đánh giá           |
| **Điểm trung bình**     | Text           | 4.8/5.0                                                                   | Điểm đánh giá trung bình                  |
| **Phân bố sao**         | Bar Chart      | Biểu đồ phân bố số lượng đánh giá theo từng mức sao                       | Biểu đồ thể hiện phân bố đánh giá         |
| **Danh sách đánh giá**  | List           | Các đánh giá của khách hàng                                               | Danh sách các đánh giá chi tiết           |
| **Đánh giá khách hàng** | Card           | Tên khách, điểm, bình luận, ngày, xác thực                                | Thẻ chứa thông tin một đánh giá           |
| **Tên khách hàng**      | Text           | Nguyễn Văn A                                                              | Tên người đánh giá                        |
| **Điểm đánh giá**       | Stars          | 5 sao                                                                     | Điểm đánh giá của khách hàng              |
| **Bình luận**           | Text           | Sản phẩm rất đẹp, chất lượng tốt, đáng mua                                | Nội dung bình luận của khách hàng         |
| **Ngày đánh giá**       | Text           | 15/01/2024                                                                | Ngày khách hàng đánh giá                  |
| **Xác thực mua hàng**   | Badge          | Đã mua hàng                                                               | Nhãn xác thực khách hàng đã mua sản phẩm  |
| **Tab Hỏi đáp**         | Tab            | Câu hỏi và trả lời                                                        | Tab chứa các câu hỏi thường gặp           |
| **Danh sách câu hỏi**   | Accordion      | Các câu hỏi và câu trả lời                                                | Danh sách các câu hỏi thường gặp          |
| **Câu hỏi**             | Text           | Sản phẩm có kèm keo dán không?                                            | Nội dung câu hỏi                          |
| **Câu trả lời**         | Text           | Có, sản phẩm kèm keo dán và dụng cụ cần thiết                             | Nội dung câu trả lời                      |

#### 1.3.3 Hành động và xử lý:

| Action Name                    | Description                                                                                                                                                                                                                                                                                                                                                        | Success                                                                                                                         | Failure                                                                                                         |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Hiển thị chi tiết sản phẩm** | Hiển thị đầy đủ thông tin chi tiết về một sản phẩm cụ thể bao gồm hình ảnh, thông tin cơ bản (tên, thương hiệu, giá, đánh giá), mô tả chi tiết, thông số kỹ thuật, đánh giá của khách hàng và câu hỏi thường gặp. Người dùng có thể xem nhiều hình ảnh sản phẩm, điều chỉnh số lượng mua và thực hiện các hành động như thêm vào giỏ hàng, yêu thích hoặc chia sẻ. | Thông tin sản phẩm hiển thị đầy đủ và chính xác. Hình ảnh load nhanh và rõ nét. Các tab thông tin hoạt động mượt mà.            | Không thể tải thông tin sản phẩm. Hình ảnh không hiển thị. Thông tin hiển thị không chính xác.                  |
| **Xem hình ảnh sản phẩm**      | Cho phép người dùng xem nhiều hình ảnh của sản phẩm thông qua gallery. Người dùng có thể click vào các thumbnail để thay đổi hình ảnh chính, phóng to hình ảnh để xem chi tiết và duyệt qua các hình ảnh khác nhau. Gallery hỗ trợ hiển thị hình ảnh với chất lượng cao và tải nhanh.                                                                              | Hình ảnh hiển thị rõ nét và nhanh chóng. Chuyển đổi giữa các hình ảnh mượt mà. Chức năng phóng to hoạt động tốt.                | Hình ảnh không tải được. Chuyển đổi hình ảnh bị lag. Chức năng phóng to không hoạt động.                        |
| **Điều chỉnh số lượng**        | Cho phép người dùng điều chỉnh số lượng sản phẩm muốn mua thông qua các nút tăng/giảm hoặc nhập trực tiếp. Số lượng tối thiểu là 1 và tối đa là số lượng tồn kho hiện có. Hệ thống sẽ kiểm tra và thông báo nếu số lượng vượt quá tồn kho.                                                                                                                         | Số lượng được điều chỉnh chính xác. Hệ thống kiểm tra tồn kho đúng cách. Thông báo rõ ràng khi vượt quá tồn kho.                | Không thể điều chỉnh số lượng. Hệ thống không kiểm tra tồn kho. Thông báo không rõ ràng.                        |
| **Thêm vào giỏ hàng**          | Cho phép người dùng thêm sản phẩm với số lượng đã chọn vào giỏ hàng. Hệ thống sẽ kiểm tra tồn kho, cập nhật giỏ hàng và hiển thị thông báo xác nhận. Nếu sản phẩm đã có trong giỏ hàng, hệ thống sẽ cộng dồn số lượng.                                                                                                                                             | Sản phẩm được thêm vào giỏ hàng thành công. Số lượng được cộng dồn đúng cách. Thông báo xác nhận rõ ràng.                       | Không thể thêm sản phẩm vào giỏ hàng. Số lượng không được cộng dồn. Thông báo lỗi không rõ ràng.                |
| **Thêm vào yêu thích**         | Cho phép người dùng thêm sản phẩm vào danh sách yêu thích để theo dõi sau này. Sản phẩm đã yêu thích sẽ có trạng thái khác biệt và có thể được xóa khỏi danh sách yêu thích. Hệ thống lưu trữ danh sách yêu thích của từng người dùng.                                                                                                                             | Sản phẩm được thêm vào danh sách yêu thích thành công. Trạng thái yêu thích được cập nhật. Có thể xóa khỏi danh sách yêu thích. | Không thể thêm vào danh sách yêu thích. Trạng thái không được cập nhật. Không thể xóa khỏi danh sách yêu thích. |
| **Xem đánh giá khách hàng**    | Hiển thị các đánh giá và bình luận của khách hàng đã mua sản phẩm. Bao gồm điểm đánh giá, nội dung bình luận, ngày đánh giá và thông tin xác thực mua hàng. Hệ thống hiển thị tổng quan về đánh giá và phân bố điểm số.                                                                                                                                            | Đánh giá khách hàng hiển thị đầy đủ và chính xác. Tổng quan đánh giá rõ ràng. Thông tin xác thực mua hàng chính xác.            | Không thể tải đánh giá khách hàng. Tổng quan đánh giá không chính xác. Thông tin xác thực không đúng.           |
| **Xem thông số kỹ thuật**      | Hiển thị bảng thông số kỹ thuật chi tiết của sản phẩm bao gồm tỷ lệ, chiều cao, chất liệu, số bộ phận, độ khó lắp ráp và độ tuổi phù hợp. Thông tin này giúp người dùng hiểu rõ hơn về sản phẩm trước khi quyết định mua.                                                                                                                                          | Thông số kỹ thuật hiển thị đầy đủ và chính xác. Bảng thông tin rõ ràng và dễ đọc.                                               | Thông số kỹ thuật không đầy đủ. Bảng thông tin khó đọc. Thông tin không chính xác.                              |
