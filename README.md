# File-update
Code 
// Định nghĩa các chân đầu ra/vào tương tự cách cấu hình thanh ghi VIA
const int LED_PIN = 13; // Chân Output

void setup() {
  // Khởi tạo cổng Serial để giao tiếp với máy tính (Tốc độ 9600 baud)
  Serial.begin(9600);
  
  // Cấu hình chân LED là OUTPUT (Giống như đặt giá trị cho thanh ghi DDR - Data Direction Register của VIA)
  pinMode(LED_PIN, OUTPUT);
  
  Serial.println("He thong VIA gia lap da san sang.");
}

void loop() {
  // Bật chân Output (Ghi logic 1 vào thanh ghi dịch/xuất dữ liệu)
  digitalWrite(LED_PIN, HIGH);
  Serial.println("Cong VIA: Xuat tin hieu CAO (HIGH)");
  delay(1000); // Chờ 1 giây
  
  // Tắt chân Output (Ghi logic 0)
  digitalWrite(LED_PIN, LOW);
  Serial.println("Cong VIA: Xuat tin hieu THAP (LOW)");
  delay(1000);
}
