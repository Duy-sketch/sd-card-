lấy dữ liệu pms7003 lưu vào sd card

repo này sẽ tạo file txt (nếu chưa có) vào trong sd card. Ngoài ra, kết nối uart1 với usb thì đưa lên máy tính sẽ hiện thị thông tin về sd card ( dung lượng, đã mount chưa,...) (nay lên đc r mà em quên kh cap lại=)))

thư mục core và FATFS là của nạp sd card, đã đầy đủ code

file pms7003.c là đo bụi xong qua usb to ttl đưa lên máy tính, dùng core mặc định của cubeide gen ra là đủ (trong ảnh htrc em gửi anh đã thành công)

giờ em kết hợp 2 cái lại thì chưa đc, kể cả tạo file txt

ảnh ioc đã miêu tả đầy đủ setup: spi2 của sd card, uart 1 của pms7003 chỉnh baud rate 9600, clock HSE 8x9Hz, spi2 prescaler /256 để khởi tạo đc sd card, fatfs use LFN chỉnh enabled with static và MAX_SS để 4096, còn lại để mặc định

các file liên quan đến fatfs lấy từ github https://github.com/Embetronicx/STM32/tree/master/STM32F103C8T6/SD%20Card%20STM32F103
