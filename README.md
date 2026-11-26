# DK AI Collaboration

Ứng dụng web tĩnh tiếng Việt giúp chuyển nhiệm vụ qua lại giữa Gemini và ChatGPT.

## Tính năng
- Gửi yêu cầu trực tiếp tới Gemini API.
- Chọn model và vai trò (phản biện, nghiên cứu, lập trình, sáng tạo).
- Tạo gói prompt để gửi sang ChatGPT.
- Tạo gói chuyển kết quả Gemini quay lại ChatGPT.
- API key chỉ giữ trong bộ nhớ trang; không ghi vào localStorage hoặc repository.

## Chạy bằng GitHub Pages
1. Vào **Settings → Pages** của repository.
2. Ở **Build and deployment**, chọn **Deploy from a branch**.
3. Chọn branch `main`, folder `/(root)`, rồi Save.
4. Chờ GitHub Pages triển khai; trang thường có địa chỉ `https://khanhcute111.github.io/DK-AI-Collaboration/`.

## Sử dụng
1. Tạo Gemini API key trong Google AI Studio: https://aistudio.google.com/app/apikey
2. Mở trang web, nhập key vào ô Gemini API key.
3. Chọn model, vai trò, nhập nhiệm vụ rồi nhấn **Gửi cho Gemini**.
4. Dùng **Tạo nội dung chuyển lại ChatGPT**, sao chép và dán vào cuộc trò chuyện ChatGPT.
5. ChatGPT trả lời xong, bạn có thể tiếp tục chuyển kết quả về Gemini bằng cách nhập phần phản hồi đó vào nhiệm vụ mới.

## Giới hạn cần biết
- Đây là quy trình chuyển giao thủ công. ChatGPT trên website/app ChatGPT không tự động nhận hoặc gửi tin nhắn cho trang này.
- Muốn tự động điều phối ChatGPT API ↔ Gemini API cần OpenAI API key và một backend trung gian; ChatGPT subscription không bao gồm OpenAI API usage.
- Gemini API có thể có hạn mức miễn phí tùy model, khu vực và điều kiện tài khoản. Không cam kết miễn phí vô hạn.
- Bản GitHub Pages gọi Gemini trực tiếp từ trình duyệt. API key không được lưu vào repo nhưng có thể bị lộ trên thiết bị/trình duyệt đang sử dụng hoặc qua extension độc hại. Chỉ dùng key cá nhân, đặt hạn mức và không chia sẻ link kèm key. Với dịch vụ công khai nhiều người dùng, cần chuyển sang backend proxy và quản lý bí mật phía máy chủ.

## Công nghệ
HTML, CSS, JavaScript thuần; không cần build step hay thư viện ngoài.