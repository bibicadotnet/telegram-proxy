# telegram-link-redirector

Tạo 1 thay thế `t.me`, vì các link Telegram `t.me` đã bị chặn tại Việt Nam

# Cài đặt

- [Fork](https://github.com/bibicadotnet/telegram-link-redirector/fork) repository này về tài khoản của bạn
- Triển khai lên Cloudflare Pages -> Cloudflare Workers & Pages -> importing Git repository này vào phần Pages (nên dùng trên tài khoản Cloudflare phụ, để tránh các giới hạn request hàng ngày)
- Cấu hình subdomain phụ cho gọn URL

# Sử dụng

- Hỗ trợ các link dạng
```
https://t.me/+qllIQbJTrj84NDFl
https://t.me/bibica_net
https://t.me/socks?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
............
```
- ví dụ nếu bạn dùng 1 sub domain phụ `t.bibica.net`, các link `t.me` lúc này sẽ thành
```
https://t.bibica.net/+qllIQbJTrj84NDFl
https://t.bibica.net/bibica_net
https://t.bibica.net/socks?server=165.121.164.165&port=16554&user=rPXLEwZ4mzVo&pass=h18jPdIeWe36Fjd8
............
```
- Trên trình duyệt có thể dùng thêm extension Redirector, giúp tạo Redirect Rule, khi gõ vào trình duyệt, `t.me` tự chuyển sang `t.bibica.net`, cấu hình có sẵn trong repository

# Ghi chú

Ban đầu thuần túy proxy các link từ Telegram sang 1 domain mới, để tránh vấn đề nhà mạng chặn, mà hôm nay mình nhận được thông báo 

<p align="center">
  <img src="https://raw.githubusercontent.com/bibicadotnet/telegram-link-redirector/refs/heads/main/2025-05-31_03-51-47.png" alt="Demo Image" width="600"/>
</p>

Nôm na Cloudflare nhận được 1 số báo cáo, nói các link từ dịch vụ của họ là trang giả mạo, nên để đỡ lằng nhằng, mọi link chuyển về trang chủ Telegram sẽ được chuyển về repository này
