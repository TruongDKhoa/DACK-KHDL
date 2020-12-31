# DACK-KHDL

# ########################################################################
# ########################                        ########################
# #############                                            ###############
# ############# Đồ án cuối kì Khoa học dữ liệu và Ứng dụng ###############
# #############                                            ###############
# ########################                        ########################
# ########################################################################

# Thành viên:
# + 1512261 - Trương Đăng Khoa - 1512261@student.hcmus.edu.vn - 0377432455
# + 1512455 - Trần Hồ Thiện Sinh - 1512455@student.hcmus.edu.vn - 0911356655

# 1. Câu hỏi được đặt ra là gì?
# - Câu hỏi được đặt ra ở đây là Làm thế nào để có thể dự đoán giá chung cho một chiếc xe ô tô cũ thông qua những yếu tố cụ thể loại xe, hãng xe, màu sắc, số #
# kilomet đã đi được...?

# 2. Nếu trả lời được câu hỏi thì có ý nghĩa gì?
# - Nếu như trả lời được câu hỏi này thì sẽ giúp được cho cả người mua lẫn người bán có thể dự đoán được giá xe một cách dễ dàng
# + Về người mua: thông qua thông tin cung cấp từ xe, họ có thể dự đoán nhanh về giá thành trước khi đi đến cửa hàng mua
# cũng như tránh được việc bị lừa đảo từ cửa hàng.
# + Về người bán: giúp hộ đánh giá nhanh được chiếc xe mình cần mua để bán lại trước khi dùng tới kinh nghiệm thực tiễn.

# 3. Cách thức thu nhập dữ liệu như thế nào? (từ đâu, parse HTML hay API, tham khảo từ đâu,...)
# - Dữ liệu được nhóm thu thập từ trang BONBANH.COM thông qua phương thức parse HTML.

# 4. Tổng quan dữ liệu thu nhập được có bao nhiêu dòng, cột và cột cần dự đoán là gì. 
# - Dữ liệu thô ban đầu thu thập được là: 
#  + ~20000 dòng 
#  + 11 cột: price, car, madeIn, status, carType, km, carColor, carSeat, engine, gear, wheeldrive.
# - Dữ liệu sau khi xử lí được là: 
#  + ~11050 dòng 
#  + 11 cột: price, car, madeIn, status, carType, km, carColor, carSeat, engine, gear, wheeldrive.
# - Cột cần dự đoán ở đây là price.

# 5. Với mỗi cột dữ liệu thu nhập có ý nghĩa gì, kiểu dữ liệu và ví dụ.
# ----------------------------------------------------------------------------------------------------------------
#       Tên cột        |         Ý nghĩa            |       Kiểu dữ liệu         |            Ví dụ
# ----------------------------------------------------------------------------------------------------------------
#    price             |  Giá tiền                  |   number                   |  7.640.000.000
#    car               |  Tên model xe              |   string                   |  Ford Ranger Limited 2.0L
#    madeIn            |  Xuất xử                   |   string                   |  Nhập khẩu
#    status            |  Tình trạng xe             |   string                   |  Xe mới
#    carType           |  Loại xe                   |   string                   |  SUV
#    km                |  Số km xe đi đươc          |   number                   |  200
#    carColor          |  Màu xe                    |   string                   |  Xanh dương
#    carSeat           |  Số chỗ ngồi               |   number                   |  4
#    engine            |  Động cơ                   |   string                   |  Dầu 2.0L
#    gear              |  Hộp số                    |   string                   |  Số tự động
#    wheelDrive        |  Cấu trúc vận hành         |   string                   |  4WD - Chuyển động 4 bánh.
# ----------------------------------------------------------------------------------------------------------------


# 6. Tự đánh giá đồ án (kết quả, thiếu sót, cần làm gì phát triển thêm,..).
# - Kết quả: Tỉ lệ dự đoán đúng cao với độ chênh lệch giá tiền khá thấp.
# - Thiếu sót: Thể hiện thông qua biểu đồ còn ít cũng như chưa đánh giá hết được dữ liệu của từng cột so với giá thành.
# - Cần phát triển: 
#   + Minh họa thông qua nhiều biểu đồ hơn.
#   + Phân tích thêm dữ liệu của các cột còn lại.
#   + Áp dụng nhiều mô hình máy học hơn để đánh giá.
#   + Sẽ phân tích thêm về hình ảnh của xe.

# 7. Phân công công việc.
# - Sinh: crawl thông tin chi tiết về xe, tiền xử lí dữ liệu, viết báo cáo.
# - Khoa: crawl thông tin chung về xe, phân tích dữ liệu, viết báo cáo.

# 8. Hướng dẫn chạy các file notebook (tất cả các quy trình, cả code thu nhập dữ liệu) Dữ liệu thu nhập được sẽ lưu trong (các) file .csv.
# - Step 1: Cài một số thư viện hỗ trợ chạy project.
#    + pip install beautifulsoup4
#    + pip install matplotlib
#    + pip install scikit-learn
#    + pip install xgboost
# - Step 2: Chạy jupiter note thông qua cmd: jupiter notebook.
# - Step 3: Chạy file crawl data (Optional).
# - Step 4: Chạy file phantichdata.ipynb 
# - Step 5: Chạy file tienxuly.ipynb 
# - Step 6: Chạy file learning.ipynb 

# ################ Kết thúc ######################

# Cám ơn Thầy đã xem - Happy New Year Thầy :)
# Khoa - Sinh.
