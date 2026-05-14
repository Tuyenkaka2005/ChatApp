<img width="210"  alt="9f17ea04-e5e7-45ab-8bf0-f92a1cbbc167" src="https://github.com/user-attachments/assets/768e2de7-f790-4841-b6b0-1de87b7bf817" />
<img width="210" alt="497212c9-62f6-4688-92c4-becd25a103ff" src="https://github.com/user-attachments/assets/32286979-45f4-4ed9-8b26-27137e3bd777" />

# LAB 7 — CHAT UI APP 💬
*SwiftUI Realtime UI & Messaging Experience*

Một ứng dụng mô phỏng giao diện nhắn tin (Chat UI) đạt chuẩn production-level được xây dựng hoàn toàn bằng **SwiftUI**. Dự án tập trung vào trải nghiệm UI/UX thời gian thực (Realtime UI), tối ưu hóa hiệu năng danh sách và tuân thủ các nguyên tắc Clean Code.

---

## 🌟 Tính năng nổi bật (Features)

* **Chat Bubbles Phân loại:** Tin nhắn của người dùng hiện tại (bên phải/màu xanh) và người khác (bên trái/màu xám).
* **Tự động cuộn (Auto-scroll to bottom):** Tự động cuộn xuống tin nhắn mới nhất khi có tin nhắn mới hoặc khi đối tác đang gõ phím nhờ ứng dụng `ScrollViewReader`.
* **Hiệu ứng gõ phím (Typing Indicator):** Hiển thị trạng thái "Typing..." kèm animation mượt mà khi người khác đang soạn tin.
* **Xử lý Bàn phím (Keyboard Handling):** Thanh nhập liệu (Input Bar) luôn được đẩy lên trên bàn phím một cách hoàn hảo nhờ `safeAreaInset`.
* **Tối ưu Hiệu năng (High Performance):** Sử dụng `LazyVStack` để render danh sách tin nhắn, đảm bảo ứng dụng không bị lag khi lịch sử trò chuyện kéo dài.
* **Hỗ trợ Giao diện (Dark/Light Mode):** Màu sắc và độ tương phản được tinh chỉnh tự động để hiển thị rõ ràng trên cả hai chế độ.
* **Trạng thái Trống (Empty State):** Giao diện chào mừng thân thiện khi chưa có tin nhắn nào sử dụng `ContentUnavailableView`.

---

## 📁 Cấu trúc Thư mục (Folder Structure)

Dự án áp dụng kiến trúc chuẩn, phân tách rõ ràng giữa Dữ liệu (Model), Logic (ViewModel) và Giao diện (View/Components):

```text
ChatApp/
│
├── Models/
│   ├── Message.swift             # Model định nghĩa cấu trúc một tin nhắn
│   └── User.swift                # Model định nghĩa thông tin người dùng
│
├── ViewModels/
│   └── ChatViewModel.swift       # Quản lý state, xử lý gửi tin và giả lập phản hồi
│
├── Views/
│   ├── ChatView.swift            # Màn hình chính chứa danh sách tin nhắn
│   ├── MessageBubble.swift       # Giao diện đóng gói của một bong bóng chat
│   ├── MessageInputView.swift    # Thanh nhập liệu và nút gửi
│   └── TypingIndicatorView.swift # Giao diện thông báo trạng thái đang gõ
│
├── Components/
│   ├── AvatarView.swift          # Component hiển thị ảnh đại diện (Avatar)
│   ├── TimestampView.swift       # Component hiển thị thời gian gửi
│   └── EmptyChatView.swift       # Màn hình hiển thị khi danh sách chat trống
│
└── ChatApp.swift                 # Entry-point khởi chạy ứng dụng
