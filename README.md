# Gesture điều khiển âm lượng - N23DCCI006

## 1. Thông tin đề tài

- Tên đề tài: Gesture điều khiển âm lượng
- Sinh viên thực hiện: Đỗ Trần Duy Bảo
- MSSV: N23DCCI006
- Lớp: D23CQCI01-N
- Học phần: Mạng cảm biến
- GVHD: Hồ Nhựt Minh

## 2. Mô tả đề tài

Đề tài xây dựng mô hình nhận dạng cử chỉ tay bằng nền tảng Edge Impulse để mô phỏng điều khiển âm lượng. Hệ thống nhận dạng bốn cử chỉ gồm OK, stop, vẫy lên và vẫy xuống. Mô hình sử dụng FOMO để phát hiện cử chỉ tay trên ảnh camera, sau đó có thể kết hợp temporal smoothing để làm kết quả realtime ổn định hơn.

## 3. Nhãn và chức năng

| Nhãn | Chức năng mô phỏng |
|---|---|
| OK | Xác nhận / giữ trạng thái |
| STOP | Dừng thao tác điều khiển |
| WAVE_UP | Tăng âm lượng |
| WAVE_DOWN | Giảm âm lượng |

## 4. Công nghệ sử dụng

- Edge Impulse Studio
- Image data
- Object Detection
- FOMO MobileNetV2 0.35
- WebAssembly deployment
- Browser realtime testing
- Temporal smoothing

## 5. Cấu hình mô hình

- Input image size: 160 x 160
- Resize mode: Fit shortest axis
- Training cycles: 150
- Learning rate: 0.001
- Training processor: CPU
- Data augmentation: Enabled
- Model version: Quantized int8
- Output classes: OK, STOP, WAVE_UP, WAVE_DOWN

## 6. Kết quả huấn luyện

- F1 Score validation: 98.2%
- Precision non-background: 0.97
- Recall non-background: 1.00
- F1 Score non-background: 0.98
- Inferencing time: 71 ms
- Peak RAM usage: 305.5K
- Flash usage: 81.4K

## 7. Link project Edge Impulse

https://studio.edgeimpulse.com/studio/1015638

## 8. Hướng dẫn chạy demo

1. Truy cập project Edge Impulse.
2. Vào mục Deployment.
3. Chọn WebAssembly.
4. Bấm Build.
5. Bấm Launch in browser.
6. Cho phép quyền camera.
7. Thực hiện lần lượt các cử chỉ OK, STOP, WAVE_UP và WAVE_DOWN để kiểm tra realtime.

## 9. Kết luận

Mô hình đã nhận dạng được bốn cử chỉ tay phục vụ mô phỏng điều khiển âm lượng. Kết quả huấn luyện đạt F1 Score 98.2%, đáp ứng yêu cầu đề tài và có thể chạy realtime trên trình duyệt thông qua WebAssembly.