

## Phần 1 – Đề xuất 2 cách gán nhãn

### Cách A – Gán nhãn theo phép thử chung (test-based)

Mọi hạng mục, bất kể bộ phận nào đề xuất, đều đi qua **cùng một bộ câu hỏi** gắn với bản phát hành cuối Sprint tới:
- Thiếu hạng mục này thì bản phát hành có chạy được / dùng được / không gây hại cho khách không?
- Đã có cách xử lý tạm thời chưa?
- Hạng mục có gắn với mục tiêu của bản phát hành ("Tháng khuyến mãi") không?

Không chạy được hoặc gây hại, và không có cách thay thế → **Must**. Còn lại xếp Should / Could / Won't theo mức giá trị và mức độ gắn với bản phát hành.

### Cách B – Gán nhãn theo đề xuất và bỏ phiếu của các bộ phận (stakeholder-driven)

Mỗi bộ phận (Marketing, Chăm sóc khách hàng, Dev...) tự đề xuất nhãn cho hạng mục mình quan tâm. Đức tổng hợp, nhãn nào được nhiều bộ phận ủng hộ hoặc bộ phận nào nhấn mạnh mạnh nhất thì thắng.

---

## Phần 2 – So sánh 2 cách

| Tiêu chí | Cách A – Phép thử chung | Cách B – Bộ phận đề xuất / bỏ phiếu |
|----------|-------------------------|--------------------------------------|
| **Khách quan khi nhiều bộ phận cùng đề xuất** | **(+)** Cùng một bộ câu hỏi cho mọi hạng mục, Marketing đòi #6 hay CSKH đòi #5 đều phải trả lời giống nhau, không thắng nhờ nói to. | **(–)** Kết quả phụ thuộc bộ phận nào vận động mạnh hơn. Marketing và CSKH đều đòi Must, dễ thành nhiều Must cùng lúc và tranh cãi kéo dài. |
| **Bảo vệ được hạng mục bắt buộc như #1** | **(+)** #1 đang thu sai tiền khách, thiếu thì không thể phát hành và không có cách thay thế, nên qua phép thử là Must dù không bộ phận nào "đòi". | **(–)** #1 là lỗi kỹ thuật, không bộ phận nào đứng ra bảo vệ nên có thể bị chen lấn bởi các Must có người vận động (#5, #6). |

Mình chọn **Cách A** vì thắng cả 2 tiêu chí.

---

## Phần 3 – Áp dụng Cách A

### Gán nhãn 6 hạng mục

| # | Hạng mục | Điểm | Nhãn | Lý do (gắn với bản phát hành "Tháng khuyến mãi") |
|---|----------|------|------|--------------------------------------------------|
| 1 | Sửa lỗi hiển thị sai cước sau khuyến mãi | 2 | **Must** | Đang thu sai tiền khách, thiếu thì không thể phát hành chương trình khuyến mãi và không có cách xử lý tạm. |
| 2 | Áp mã khuyến mãi khi đặt xe | 2 | **Must** | Là chức năng cốt lõi của "Tháng khuyến mãi", không có thì chương trình không vận hành được. |
| 3 | Thanh toán bằng ví RikkeiPay | 3 | **Should** | Quan trọng và đi tiếp sau bước áp mã, nhưng khách vẫn trả được tiền mặt nên bản phát hành vẫn chạy được. |
| 4 | Hẹn giờ đặt xe trước | 3 | **Could** | Có giá trị cho khách nhưng không gắn với chương trình khuyến mãi, thiếu thì bản phát hành vẫn chạy bình thường. |
| 5 | Chat với tài xế | 3 | **Won't** (lần này) | CSKH muốn Must nhưng đã có cách xử lý tạm là khách vẫn gọi điện được, và không thuộc mục tiêu của bản phát hành. |
| 6 | Giao diện trang trí cho chương trình | 2 | **Won't** (lần này) | Nghe rất "đúng dịp" nhưng thiếu nó bản phát hành vẫn chạy được, không ảnh hưởng tiền hay chức năng của khách. |

### Danh sách vào Sprint (vừa 10 điểm)

| Nhãn | Hạng mục | Điểm |
|------|----------|------|
| Must | #1 Sửa lỗi hiển thị sai cước | 2 |
| Must | #2 Áp mã khuyến mãi | 2 |
| Should | #3 Thanh toán ví RikkeiPay | 3 |
| Could | #4 Hẹn giờ đặt xe | 3 |
| | **Tổng** | **10** |

Thứ tự cắt khi trễ: **#4 (Could) trước, rồi đến #3 (Should)**. #1 và #2 luôn giữ.

### Tỷ lệ Must

**Must = 2 + 2 = 4 điểm → 4 / 10 = 40% năng lực.**

Mình ghi rõ chỗ này vì thấp hơn mốc "khoảng 60%": phép thử chỉ cho ra 2 hạng mục Must thật sự (#1, #2). Mình không kéo #5 hay #6 lên Must cho đủ 60% vì như vậy là gán sai bản chất, đúng cái bẫy của đề. Mốc 60% dùng như mức trần để còn chỗ cắt khi trễ, và 40% vẫn trong mức đó, phần Should + Could (6 điểm) là vùng đệm.

### Báo bên liên quan về hạng mục Won't

- **Chăm sóc khách hàng (#5):** chat với tài xế chưa làm ở bản này vì khách vẫn gọi điện được. Đề xuất đưa vào Sprint sau.
- **Marketing (#6):** giao diện trang trí chưa làm ở bản này vì không ảnh hưởng chức năng và tiền của khách, nhường năng lực cho #1 và #2.
