# QUẢN LÝ SẢN PHẨM

_Dựa trên tài liệu yêu cầu - Chức năng quản lý sản phẩm của Admin_

## MỤC LỤC

1. [Chức năng quản lý sản phẩm](#1-chức-năng-quản-lý-sản-phẩm)
   - 1.1 [Danh sách sản phẩm](#11-danh-sách-sản-phẩm)
     - 1.1.1 [Định dạng 1.png](#111-định-dạng-1png)
     - 1.1.2 [Định dạng 2.png](#112-định-dạng-2png)
     - 1.1.3 [Định dạng 3.png](#113-định-dạng-3png)
   - 1.2 [Thêm sản phẩm mới](#12-thêm-sản-phẩm-mới)
     - 1.2.1 [Định dạng 1.png](#121-định-dạng-1png)
     - 1.2.2 [Định dạng 2.png](#122-định-dạng-2png)
     - 1.2.3 [Định dạng 3.png](#123-định-dạng-3png)
   - 1.3 [Chỉnh sửa sản phẩm](#13-chỉnh-sửa-sản-phẩm)
     - 1.3.1 [Định dạng 1.png](#131-định-dạng-1png)
     - 1.3.2 [Định dạng 2.png](#132-định-dạng-2png)
     - 1.3.3 [Định dạng 3.png](#133-định-dạng-3png)

---

## 1. CHỨC NĂNG QUẢN LÝ SẢN PHẨM

### 1.1 DANH SÁCH SẢN PHẨM

#### 1.1.1 Định dạng 1.png:

| Screen        | Danh sách sản phẩm                                                                                               |
| ------------- | ---------------------------------------------------------------------------------------------------------------- |
| Description   | Hiển thị danh sách tất cả sản phẩm trong hệ thống, cho phép quản trị viên xem, tìm kiếm, lọc và quản lý sản phẩm |
| Screen Access | Admin chọn **Sản phẩm** trên sidebar\*\*                                                                         |

#### 1.1.2 Định dạng 2.png:

| Item                   | Type         | Data                                                                                           | Description                                                          |
| ---------------------- | ------------ | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **Tiêu đề trang**      | Text         | Quản lý sản phẩm                                                                               | Tiêu đề chính của trang quản lý sản phẩm                             |
| **Mô tả chức năng**    | Text         | Quản lý và theo dõi tất cả sản phẩm trong hệ thống                                             | Mô tả ngắn gọn về mục đích của trang                                 |
| **Thống kê tổng quan** | Card Group   | Tổng sản phẩm: 150<br>Đang bán: 120<br>Hết hàng: 15<br>Ngừng bán: 10<br>Tổng giá trị: 2.5B VNĐ | Hiển thị các chỉ số thống kê nhanh về tình hình sản phẩm             |
| **Tìm kiếm sản phẩm**  | Input (Text) |                                                                                                | Ô nhập liệu để tìm kiếm sản phẩm theo tên, mã sản phẩm hoặc danh mục |
| **Bộ lọc trạng thái**  | Dropdown     | Tất cả<br>Đang bán<br>Hết hàng<br>Ngừng bán<br>Chờ duyệt                                       | Lọc danh sách sản phẩm theo trạng thái                               |
| **Bộ lọc danh mục**    | Dropdown     | Tất cả<br>Gundam<br>Figure<br>Mô hình xe<br>Máy bay<br>Phụ kiện                                | Lọc danh sách sản phẩm theo danh mục                                 |
| **Danh sách sản phẩm** | Table        | Hình ảnh<br>Tên sản phẩm<br>Mã sản phẩm<br>Danh mục<br>Giá<br>Trạng thái<br>Kho<br>Thao tác    | Hiển thị các sản phẩm dưới dạng bảng                                 |
| **Hình ảnh**           | Image        | [Hình ảnh sản phẩm]                                                                            | Hình ảnh đại diện của sản phẩm                                       |
| **Tên sản phẩm**       | Text         | Gundam RX-78-2 Master Grade                                                                    | Tên đầy đủ của sản phẩm                                              |
| **Mã sản phẩm**        | Text         | GUN001                                                                                         | Mã định danh duy nhất của sản phẩm                                   |
| **Danh mục**           | Badge        | Gundam                                                                                         | Danh mục sản phẩm thuộc về                                           |
| **Giá**                | Text         | 1.500.000 VNĐ                                                                                  | Giá bán của sản phẩm                                                 |
| **Trạng thái**         | Badge        | Đang bán<br>Hết hàng<br>Ngừng bán<br>Chờ duyệt                                                 | Trạng thái hiện tại của sản phẩm                                     |
| **Kho**                | Text         | 25                                                                                             | Số lượng tồn kho hiện tại                                            |
| **Thao tác**           | Button Group | Xem chi tiết, Chỉnh sửa, Xóa                                                                   | Các nút để thực hiện thao tác trên sản phẩm                          |
| **Nút thêm mới**       | Button       | Thêm sản phẩm mới                                                                              | Nút để tạo sản phẩm mới                                              |
| **Phân trang**         | Pagination   | Trang 1/10                                                                                     | Điều hướng giữa các trang danh sách sản phẩm                         |

#### 1.1.3 Định dạng 3.png:

| Action Name                | Description                                                                                                                                                                                                                                                                                                                                                                                                             | Success                                                                                                                     | Failure                                                                                                               |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Xem danh sách sản phẩm** | Hiển thị danh sách tất cả sản phẩm trong hệ thống với thông tin chi tiết. Cho phép quản trị viên xem hình ảnh, tên, mã sản phẩm, danh mục, giá, trạng thái và số lượng tồn kho. Cung cấp tính năng tìm kiếm theo tên sản phẩm, mã sản phẩm hoặc danh mục. Hỗ trợ lọc theo trạng thái (Đang bán, Hết hàng, Ngừng bán, Chờ duyệt) và danh mục sản phẩm. Hiển thị thống kê tổng quan về số lượng sản phẩm và tổng giá trị. | Hiển thị danh sách sản phẩm với đầy đủ thông tin. Tìm kiếm và lọc hiển thị kết quả chính xác theo tiêu chí đã chọn.         | Không tìm thấy sản phẩm nào theo tiêu chí tìm kiếm hoặc lọc. Lỗi khi tải dữ liệu danh sách sản phẩm từ hệ thống.      |
| **Tìm kiếm sản phẩm**      | Cho phép quản trị viên tìm kiếm sản phẩm theo các tiêu chí khác nhau. Hỗ trợ tìm kiếm theo tên sản phẩm, mã sản phẩm, danh mục hoặc mô tả sản phẩm. Tìm kiếm real-time khi người dùng nhập từ khóa. Hiển thị kết quả tìm kiếm ngay lập tức và cập nhật danh sách sản phẩm.                                                                                                                                              | Hiển thị danh sách sản phẩm phù hợp với từ khóa tìm kiếm. Tìm kiếm nhanh và chính xác theo các tiêu chí đã chọn.            | Không tìm thấy sản phẩm nào phù hợp với từ khóa tìm kiếm. Lỗi khi thực hiện tìm kiếm do vấn đề kết nối hoặc dữ liệu.  |
| **Lọc sản phẩm**           | Cung cấp các bộ lọc để quản trị viên có thể lọc danh sách sản phẩm theo nhu cầu. Bao gồm bộ lọc theo trạng thái (Đang bán, Hết hàng, Ngừng bán, Chờ duyệt). Bộ lọc theo danh mục (Gundam, Figure, Mô hình xe, Máy bay, Phụ kiện). Bộ lọc theo khoảng giá. Bộ lọc theo mức độ ưu tiên (Cao, Trung bình, Thấp).                                                                                                           | Hiển thị danh sách sản phẩm đã được lọc theo tiêu chí đã chọn. Bộ lọc hoạt động chính xác và cập nhật kết quả ngay lập tức. | Bộ lọc không hoạt động hoặc hiển thị kết quả không chính xác. Lỗi khi áp dụng bộ lọc do vấn đề dữ liệu hoặc hệ thống. |

### 1.2 THÊM SẢN PHẨM MỚI

#### 1.2.1 Định dạng 1.png:

| Screen        | Thêm sản phẩm mới                                                                        |
| ------------- | ---------------------------------------------------------------------------------------- |
| Description   | Form cho phép quản trị viên thêm sản phẩm mới vào hệ thống với đầy đủ thông tin chi tiết |
| Screen Access | Admin click vào nút **Thêm sản phẩm mới** từ danh sách sản phẩm                          |

#### 1.2.2 Định dạng 2.png:

| Item                   | Type         | Data                                                                                              | Description                                                |
| ---------------------- | ------------ | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **Tiêu đề trang**      | Text         | Thêm sản phẩm mới                                                                                 | Tiêu đề trang thêm sản phẩm                                |
| **Thông tin cơ bản**   | Card         | Tên sản phẩm<br>Mã sản phẩm<br>Danh mục<br>Mô tả ngắn<br>Mô tả chi tiết<br>Thương hiệu<br>Xuất xứ | Hiển thị các thông tin cơ bản về sản phẩm                  |
| **Tên sản phẩm**       | Textbox      | Gundam RX-78-2 Master Grade                                                                       | Tên đầy đủ của sản phẩm                                    |
| **Mã sản phẩm**        | Textbox      | GUN001                                                                                            | Mã định danh duy nhất của sản phẩm                         |
| **Danh mục**           | Dropdown     | Gundam, Figure, Mô hình xe, Máy bay, Phụ kiện                                                     | Danh mục sản phẩm thuộc về                                 |
| **Mô tả ngắn**         | Textarea     | Mô hình Gundam RX-78-2 phiên bản Master Grade                                                     | Mô tả ngắn gọn về sản phẩm                                 |
| **Mô tả chi tiết**     | Textarea     | Mô hình Gundam RX-78-2 Master Grade với chi tiết cao, có thể tháo lắp và sơn màu...               | Mô tả chi tiết về sản phẩm                                 |
| **Thương hiệu**        | Textbox      | Bandai                                                                                            | Thương hiệu sản xuất sản phẩm                              |
| **Xuất xứ**            | Textbox      | Nhật Bản                                                                                          | Quốc gia sản xuất sản phẩm                                 |
| **Thông tin bán hàng** | Card         | Giá bán<br>Giá nhập<br>Lợi nhuận<br>Đơn vị<br>Trạng thái<br>Ưu tiên                               | Hiển thị thông tin về giá cả và trạng thái bán hàng        |
| **Giá bán**            | Number       | 1.500.000                                                                                         | Giá bán cho khách hàng                                     |
| **Giá nhập**           | Number       | 1.200.000                                                                                         | Giá nhập từ nhà cung cấp                                   |
| **Lợi nhuận**          | Text         | 300.000 (20%)                                                                                     | Lợi nhuận dự kiến từ sản phẩm                              |
| **Đơn vị**             | Dropdown     | Cái, Bộ, Hộp                                                                                      | Đơn vị tính của sản phẩm                                   |
| **Trạng thái**         | Dropdown     | Đang bán, Hết hàng, Ngừng bán, Chờ duyệt                                                          | Trạng thái hiện tại của sản phẩm                           |
| **Ưu tiên**            | Dropdown     | Cao, Trung bình, Thấp                                                                             | Mức độ ưu tiên của sản phẩm                                |
| **Hình ảnh sản phẩm**  | File Upload  | [Upload hình ảnh]                                                                                 | Upload hình ảnh đại diện và hình ảnh chi tiết của sản phẩm |
| **Hành động**          | Button Group | Lưu sản phẩm<br>Lưu nháp<br>Hủy bỏ                                                                | Các nút chức năng để thực hiện các thao tác trên sản phẩm  |
| **Lưu sản phẩm**       | Button       |                                                                                                   | Lưu sản phẩm vào hệ thống                                  |
| **Lưu nháp**           | Button       |                                                                                                   | Lưu sản phẩm dưới dạng nháp                                |
| **Hủy bỏ**             | Button       |                                                                                                   | Hủy bỏ việc thêm sản phẩm và quay lại danh sách            |

#### 1.2.3 Định dạng 3.png:

| Action Name                  | Description                                                                                                                                                                                                                                                                                                                        | Success                                                                                                  | Failure                                                                                                            |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Thêm sản phẩm mới**        | Cho phép quản trị viên thêm sản phẩm mới vào hệ thống với đầy đủ thông tin. Bao gồm thông tin cơ bản (tên, mã, danh mục, mô tả), thông tin bán hàng (giá, trạng thái), và hình ảnh sản phẩm. Hệ thống tự động tính toán lợi nhuận dự kiến. Kiểm tra tính hợp lệ của dữ liệu nhập vào. Tự động tạo mã sản phẩm nếu không được nhập. | Sản phẩm được thêm thành công vào hệ thống. Hiển thị thông báo xác nhận và chuyển về danh sách sản phẩm. | Dữ liệu nhập vào không hợp lệ. Mã sản phẩm đã tồn tại. Lỗi khi upload hình ảnh. Lỗi khi lưu sản phẩm vào hệ thống. |
| **Lưu nháp sản phẩm**        | Cho phép quản trị viên lưu sản phẩm dưới dạng nháp khi chưa hoàn thiện thông tin. Sản phẩm nháp sẽ không hiển thị cho khách hàng và có thể chỉnh sửa sau. Hiển thị trạng thái "Nháp" trong danh sách sản phẩm.                                                                                                                     | Sản phẩm được lưu dưới dạng nháp thành công. Có thể tiếp tục chỉnh sửa sau.                              | Không thể lưu nháp do lỗi hệ thống. Dữ liệu không hợp lệ.                                                          |
| **Upload hình ảnh sản phẩm** | Cho phép quản trị viên upload hình ảnh đại diện và hình ảnh chi tiết cho sản phẩm. Hỗ trợ các định dạng JPG, PNG, GIF. Tự động resize hình ảnh theo kích thước chuẩn. Hiển thị preview hình ảnh trước khi lưu.                                                                                                                     | Hình ảnh được upload thành công và hiển thị preview. Hình ảnh được lưu vào hệ thống.                     | File không đúng định dạng. Kích thước file quá lớn. Lỗi khi upload do vấn đề kết nối.                              |

### 1.3 CHỈNH SỬA SẢN PHẨM

#### 1.3.1 Định dạng 1.png:

| Screen        | Chỉnh sửa sản phẩm                                                                   |
| ------------- | ------------------------------------------------------------------------------------ |
| Description   | Form cho phép Admin chỉnh sửa thông tin sản phẩm đã có trong hệ thống                |
| Screen Access | Admin click vào nút **Chỉnh sửa** từ danh sách sản phẩm hoặc trang chi tiết sản phẩm |

#### 1.3.2 Định dạng 2.png:

| Item                   | Type     | Data                                                                            | Description                                              |
| ---------------------- | -------- | ------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Tiêu đề Modal**      | Text     | Chỉnh sửa sản phẩm                                                              | Tiêu đề của trang chỉnh sửa sản phẩm                     |
| **Thông tin sản phẩm** | Text     | Mã: GUN001<br>Tên: Gundam RX-78-2 Master Grade<br>Trạng thái hiện tại: Đang bán | Hiển thị tóm tắt thông tin sản phẩm đang chỉnh sửa       |
| **Form chỉnh sửa**     | Form     | Tất cả các trường từ form thêm sản phẩm với dữ liệu hiện tại                    | Form chứa tất cả thông tin sản phẩm có thể chỉnh sửa     |
| **Lịch sử thay đổi**   | Table    | Thời gian, Người thay đổi, Trường thay đổi, Giá trị cũ, Giá trị mới             | Hiển thị lịch sử các thay đổi đã thực hiện trên sản phẩm |
| **Ghi chú thay đổi**   | Textarea |                                                                                 | Vùng nhập lý do thay đổi thông tin sản phẩm              |
| **Nút Hủy**            | Button   |                                                                                 | Hủy chỉnh sửa và quay lại danh sách                      |
| **Nút Lưu thay đổi**   | Button   |                                                                                 | Lưu các thay đổi và cập nhật sản phẩm                    |

#### 1.3.3 Định dạng 3.png:

| Action Name                       | Description                                                                                                                                                                                                                                                                                                                      | Success                                                                                                                         | Failure                                                                                                           |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Chỉnh sửa thông tin sản phẩm**  | Cho phép quản trị viên chỉnh sửa tất cả thông tin của sản phẩm đã có trong hệ thống. Bao gồm thông tin cơ bản, thông tin bán hàng, hình ảnh và trạng thái. Hệ thống tự động tính toán lại lợi nhuận khi thay đổi giá. Ghi lại lịch sử thay đổi với thông tin người thực hiện và thời gian. Kiểm tra tính hợp lệ của dữ liệu mới. | Thông tin sản phẩm được cập nhật thành công. Lịch sử thay đổi được ghi lại. Hiển thị thông báo xác nhận.                        | Dữ liệu mới không hợp lệ. Không có quyền chỉnh sửa sản phẩm. Lỗi khi cập nhật thông tin vào hệ thống.             |
| **Xem lịch sử thay đổi sản phẩm** | Hiển thị lịch sử chi tiết các thay đổi đã thực hiện trên sản phẩm. Bao gồm thông tin về thời gian, người thực hiện, trường được thay đổi, giá trị cũ và giá trị mới. Hiển thị theo thứ tự thời gian từ mới nhất đến cũ nhất. Cho phép xem chi tiết từng thay đổi.                                                                | Hiển thị đầy đủ lịch sử thay đổi sản phẩm. Thông tin chi tiết về từng thay đổi được hiển thị chính xác.                         | Không thể tải lịch sử thay đổi do lỗi hệ thống. Lịch sử hiển thị không đầy đủ hoặc không chính xác.               |
| **Cập nhật trạng thái sản phẩm**  | Cho phép quản trị viên thay đổi trạng thái sản phẩm (Đang bán, Hết hàng, Ngừng bán, Chờ duyệt). Yêu cầu nhập lý do thay đổi trạng thái. Tự động ghi lại lịch sử thay đổi. Có thể gửi thông báo cho khách hàng về việc thay đổi trạng thái sản phẩm.                                                                              | Trạng thái sản phẩm được cập nhật thành công. Lịch sử thay đổi được ghi lại. Thông báo được gửi cho khách hàng (nếu được chọn). | Không thể cập nhật trạng thái do lỗi hệ thống. Trạng thái mới không hợp lệ. Lỗi khi gửi thông báo cho khách hàng. |
