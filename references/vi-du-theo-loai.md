# Ví dụ theo từng loại

Mỗi cặp "trước" và "sau" viết từ cùng một bộ dữ kiện. Số liệu là giả định. Hãy đọc các ví dụ để bắt giọng văn, đừng chép lại khung câu.

Mục lục:

1. Trả lời câu hỏi có hay không
2. Hỏi để người đọc quyết
3. Viết lại ghi chú kỹ thuật cho người không làm kỹ thuật
4. Bài đăng cho cả nhóm
5. Commit và mô tả thay đổi
6. Hướng dẫn làm theo
7. Email gửi đối tác

Ba loại còn lại (báo lại việc đã làm, giải thích một khái niệm, tin nhắn soạn hộ) có ví dụ ngay trong SKILL.md.

---

## 1. Trả lời câu hỏi có hay không

Người dùng hỏi: "Xoá danh mục thì quà trong đó có mất không?"

Trước:

> Đây là một câu hỏi rất hay! Để trả lời, chúng ta cần xem xét cách hệ thống xử lý mối quan hệ giữa danh mục và quà tặng. Về cơ bản, khi một danh mục bị xoá, hệ thống sẽ thực hiện soft delete đối với bản ghi danh mục, đồng thời các quà tặng thuộc danh mục đó sẽ không bị xoá mà được chuyển sang trạng thái không có danh mục. Tuy nhiên, điều quan trọng cần lưu ý là các quà này sẽ không còn hiển thị trên ứng dụng cho đến khi được gán vào một danh mục khác. Tóm lại, quà không bị mất nhưng sẽ bị ẩn. Nếu bạn cần hỗ trợ thêm về việc gán lại danh mục, hãy cho tôi biết nhé!

Sau:

> Quà không mất, nhưng sẽ bị ẩn khỏi ứng dụng.
>
> Khi bạn xoá danh mục, các quà trong danh mục đó vẫn còn nguyên, chỉ là không thuộc danh mục nào nữa. Ứng dụng chỉ hiện quà có danh mục, nên khách không thấy các quà này.
>
> Muốn khách thấy lại các quà đó thì bạn gán chúng vào một danh mục khác.

Đã đổi gì: câu trả lời lên dòng đầu, thay vì nằm sau chữ "Tóm lại" ở cuối. Bỏ lời khen câu hỏi, câu dẫn, lời mời hỏi thêm. "Soft delete" được tả thành việc xảy ra với quà, là thứ người hỏi quan tâm.

Câu trả lời ngắn vẫn có chủ ngữ. Viết "Quà không mất", không viết "Không mất".

---

## 2. Hỏi để người đọc quyết

Trước:

> Có một số phương án có thể cân nhắc cho vấn đề này:
>
> - **Phương án A:** Thêm cột mới vào bảng hiện tại. Ưu điểm: đơn giản. Nhược điểm: cần migration.
> - **Phương án B:** Tạo bảng mới. Ưu điểm: linh hoạt. Nhược điểm: phức tạp hơn.
> - **Phương án C:** Lưu trong JSON config. Ưu điểm: không cần migration. Nhược điểm: khó query.
>
> Bạn muốn chọn phương án nào?

Sau:

> Hạn dùng của gói nên lưu ở đâu: thêm một cột vào bảng gói đang có, hay tạo bảng mới?
>
> Tôi chọn thêm cột. Mỗi gói chỉ có một hạn dùng nên một cột là đủ, và ta không phải sửa các màn hình đang đọc bảng này.
>
> Bảng mới chỉ đáng làm khi một gói có nhiều kỳ hạn. Hiện chưa có yêu cầu đó.
>
> Cái giá của việc thêm cột: lúc deploy, người deploy phải chạy một lệnh sửa bảng.

Đã đổi gì: câu hỏi nằm ở dòng đầu và nói rõ đang hỏi về cái gì. Người viết nêu mình chọn gì, vì sao, và cái giá, để người đọc chỉ cần đồng ý hoặc phản bác. Phương án không ai định chọn (lưu trong cấu hình) được bỏ.

---

## 3. Viết lại ghi chú kỹ thuật cho người không làm kỹ thuật

Ghi chú gốc:

```
Cron sync catalog 02:00 fail do vendor API trả 429 (rate limit), job không retry → 37 SP mới
của vendor chưa vào DB. Chạy tay 08:20 OK. Sẽ thêm retry + backoff trong tuần.
```

Trước (dịch từng chữ, vẫn khó hiểu):

> Job đồng bộ catalog lúc 02:00 đã thất bại do API của vendor trả về mã lỗi 429 (giới hạn tần suất), và do job không có cơ chế retry nên 37 sản phẩm mới chưa được ghi nhận vào cơ sở dữ liệu. Đã tiến hành chạy thủ công lúc 08:20 và ghi nhận kết quả thành công.

Sau (gửi chị phụ trách vận hành):

> Sáng nay 37 quà mới của nhà cung cấp chưa hiện trên trang quản trị cho tới 8 giờ 20. Giờ cả 37 quà đã hiện đủ.
>
> Lý do: 2 giờ sáng hệ thống lấy danh sách quà từ nhà cung cấp như mọi ngày. Nhà cung cấp từ chối vì hệ thống gọi quá nhiều lần liên tiếp, và hệ thống không tự thử lại.
>
> Trong tuần này em thêm cho hệ thống bước tự thử lại, để lần sau không ai phải bấm chạy lại bằng tay.

Đã đổi gì: mở bằng điều người vận hành nhìn thấy (quà chưa hiện, giờ đã hiện), không mở bằng tên job. "429", "rate limit", "retry", "backoff" được tả bằng việc xảy ra. Nguyên nhân chỉ còn hai câu, vì người đọc không sửa hệ thống.

Câu "Đã tiến hành chạy thủ công" thiếu cả người làm lẫn thứ được chạy. Bản sau nói rõ từng câu: hệ thống lấy danh sách quà, nhà cung cấp từ chối, em thêm bước tự thử lại.

Viết lại không phải là dịch từng chữ sang tiếng Việt. Phải đổi từ góc nhìn của hệ thống sang góc nhìn của người đọc.

---

## 4. Bài đăng cho cả nhóm

Trước:

> 🎉 THÔNG BÁO RA MẮT TÍNH NĂNG MỚI 🎉
>
> Chào mọi người! Team rất vui mừng được thông báo tính năng Tìm kiếm ưu đãi đã chính thức ra mắt! Đây là một bước tiến quan trọng nhằm nâng cao trải nghiệm người dùng một cách toàn diện.
>
> ✨ Điểm nổi bật:
> - **Tìm kiếm thông minh:** Giúp khách hàng tìm thấy ưu đãi nhanh chóng và dễ dàng
> - **Phạm vi:** Áp dụng cho các shop sử dụng trang Ưu đãi bản mới
>
> Bạn nào chưa nắm thì trải nghiệm thử và cho team feedback nhé! 💪

Sau:

> Trang Ưu đãi có thêm ô tìm kiếm, từ hôm nay 12/11
>
> Chào cả nhà,
>
> Khách gõ tên quà hoặc tên thương hiệu vào ô tìm kiếm là thấy kết quả, không phải kéo qua từng danh mục như trước.
>
> Ô tìm kiếm có ở mọi shop đang dùng trang Ưu đãi bản mới. Shop còn dùng bản cũ thì chưa có ô này.
>
> Lưu ý khi hỗ trợ shop: ô tìm kiếm chỉ tìm trong các quà đang bật. Quà đã tắt không hiện trong kết quả, dù khách gõ đúng tên.
>
> Thắc mắc xin nhắn nhóm Sản phẩm.

Đã đổi gì: tiêu đề chứa tin chính và ngày. Thân bài nói khách làm được gì, shop nào có, và một điều người hỗ trợ cần biết. Bỏ emoji, chữ in hoa, nhãn in đậm, "bước tiến quan trọng".

Câu "Áp dụng cho các shop..." không nói cái gì được áp dụng, nên được viết lại thành "Ô tìm kiếm có ở mọi shop...". Câu không gọi thẳng người đọc ("bạn nào chưa nắm"), vì bài đăng chung có cả lãnh đạo đọc.

---

## 5. Commit và mô tả thay đổi

Trước:

> fix: handle null data in RedeemProcessingException + add optional field to LogicErrorException ctor
>
> Saga giữ order PENDING và ném REDEEM_PROCESSING với data=null. LogicErrorException nhận thêm field data optional (ctor 2 tham số giữ nguyên). Thêm endpoint GET /orders/{code}.

Sau:

> Trả mã đơn khi đơn đổi quà đang treo
>
> Gốc vấn đề: khi nhà cung cấp trả lời chậm, khách thấy báo lỗi và điểm của khách đã bị giữ, nhưng khách không có mã nào để tra lại đơn.
>
> Thay đổi này trả mã đơn kèm trong thông báo lỗi, và thêm API để tra trạng thái đơn theo mã đó (`GET /orders/{code}`).

Đã đổi gì: người review và người deploy không phải là người vừa viết code, nên dòng đầu nói chuyện xảy ra với khách. Tên class và chi tiết chữ ký hàm được bỏ, vì ai cần thì đọc diff. Tên API được giữ trong backtick vì người đọc cần nó để thử.

Giọng ở đây là văn viết chỉnh tề. Không viết "mấy cái đơn bị treo hồi trước" trong commit.

---

## 6. Hướng dẫn làm theo

Trước:

> Để có thể chạy được dự án ở local, trước tiên bạn cần đảm bảo rằng đã cài đặt Node phiên bản 20.12 trở lên, sau đó tiến hành clone repo về và chạy lệnh npm install để cài đặt các dependencies, tiếp theo cần tạo file .env từ file .env.example và điền các giá trị cần thiết, cuối cùng chạy npm run dev và truy cập vào địa chỉ localhost:5174.

Sau:

> Làm xong 4 bước này là bạn mở được trang ở localhost:5174.
>
> 1. Cài Node bản 20.12 trở lên. Kiểm tra phiên bản bằng lệnh `node -v`.
> 2. Tải mã nguồn về rồi chạy `npm install`.
> 3. Chép file `.env.example` thành `.env` và điền các giá trị còn trống.
> 4. Chạy `npm run dev`.
>
> Nếu bước 2 báo lỗi về phiên bản Node thì bạn quay lại kiểm tra bước 1.

Đã đổi gì: dòng đầu nói làm xong thì được gì. Mỗi bước một việc, đánh số, lệnh để trong backtick để chép. Thêm đúng một lưu ý cho chỗ hay vấp nhất.

Các bước là câu mệnh lệnh nên không cần chủ ngữ, nhưng vẫn phải nói rõ làm gì với cái gì: "Chép file `.env.example` thành `.env`".

---

## 7. Email gửi đối tác

Văn trang trọng vẫn theo sáu thói quen. Trang trọng nằm ở cách xưng hô và câu chỉnh tề, không nằm ở độ dài.

Trước:

> Kính gửi Quý đối tác,
>
> Lời đầu tiên, chúng tôi xin gửi lời cảm ơn chân thành đến Quý đối tác đã luôn đồng hành và tin tưởng sử dụng dịch vụ trong suốt thời gian qua. Nhằm mục đích không ngừng nâng cao chất lượng dịch vụ, chúng tôi xin trân trọng thông báo về việc tiến hành bảo trì hệ thống vào cuối tuần này. Trong thời gian bảo trì, một số tính năng có thể bị gián đoạn. Chúng tôi rất mong nhận được sự thông cảm của Quý đối tác và xin chân thành cáo lỗi vì sự bất tiện này.

Sau:

> Tiêu đề: Hệ thống đổi quà tạm ngưng từ 23 giờ thứ Bảy 28/11 đến 2 giờ Chủ nhật 29/11
>
> Kính gửi anh chị,
>
> Hệ thống đổi quà sẽ tạm ngưng từ 23 giờ thứ Bảy 28/11 đến 2 giờ sáng Chủ nhật 29/11 để chúng tôi nâng cấp máy chủ.
>
> Trong 3 giờ này khách không đổi được quà. Điểm và voucher khách đã có không bị ảnh hưởng.
>
> Anh chị không cần làm gì thêm. Nếu cửa hàng có chương trình chạy trong khung giờ này, xin anh chị báo cho chúng tôi trước thứ Năm 26/11 để chúng tôi dời lịch.
>
> Trân trọng,
> Nhóm Vận hành

Đã đổi gì: "cuối tuần này" và "một số tính năng" được thay bằng giờ cụ thể và đúng tính năng bị ngưng. Thêm điều đối tác lo nhất (điểm và voucher có mất không) và việc họ cần làm. Lời cảm ơn và lời cáo lỗi dài được bỏ, vì chúng đẩy tin chính xuống dưới.
