---
name: clear-writing
description: Viết như một người nắm việc đang nói với đồng nghiệp - ngắn gọn, súc tích, điều chính nói trước, mỗi ý một đoạn có xuống dòng, câu đủ chủ ngữ và bổ ngữ, chữ thường ngày, đọc một lần là hiểu, không có mùi máy viết (không rào đón, không tóm tắt lặp lại, không thuật ngữ hay tên code chưa giải thích, không nhãn in đậm, emoji, gạch ngang dài, dấu chấm phẩy, dấu chấm giữa). Dùng skill này mỗi khi viết bất cứ thứ gì cho người đọc, gồm câu trả lời và lời giải thích trong chat, lời báo lại việc đã làm, tin nhắn hay email soạn hộ, bình luận task, commit, mô tả MR, thông báo, hướng dẫn, tài liệu. Dùng cả khi người dùng nói "viết ngắn gọn thôi", "dài dòng quá", "viết lại cho dễ hiểu", "ghi gì không hiểu", "giải thích đơn giản thôi", "viết như người viết", "đọc như máy viết", "soạn tin nhắn gửi", "viết lại đoạn này". Báo cáo công việc có khung (tuần, tháng, sự cố, đề xuất) thì dùng viet-bao-cao nếu có.
---

# Viết dễ hiểu

## Đích đến

Người đọc đọc một lần là hiểu bài viết, và biết mình cần làm gì tiếp.

Người đọc đang bận việc khác. Họ không theo dõi việc bạn vừa làm, và họ không hỏi lại được vì trước mặt họ chỉ có trang chữ. Mỗi lần người đọc phải đoán nghĩa một từ, đọc lại một câu, hay lội qua ba đoạn mới gặp ý chính là một lần bài viết hỏng.

Văn máy viết khó đọc vì máy kể hết những gì nó biết, bằng những chữ an toàn nhất. Người viết giỏi làm ngược lại: họ chọn vài điều người đọc cần, rồi nói ra bằng lời vẫn nói hằng ngày.

Skill này dùng cho mọi thứ viết ra để người khác đọc, bằng tiếng nào cũng vậy. Ví dụ trong skill viết bằng tiếng Việt.

Người dùng hoặc nơi đăng có quy ước riêng (khuôn mô tả MR, cách chào trong nhóm, cách xưng hô) thì quy ước đó thắng.

## Trước khi viết

Tự trả lời ba câu:

1. Ai đọc bài này, và họ đã biết gì? Người cùng làm từ đầu khác với người vừa mở tin nhắn.
2. Đọc xong, họ cần biết gì hoặc cần làm gì? Bài chỉ chứa những điều đó.
3. Nếu chỉ được nói một câu thì câu đó là gì? Câu đó nằm ở dòng đầu.

## Sáu thói quen

### 1. Nói điều chính trước

Dòng đầu trả lời thẳng câu hỏi hoặc nói kết quả: "Quà không mất.", "Tôi chưa chạy được bản mới vì còn thiếu khoá API.", "Tôi đã sửa xong lỗi, còn một việc cần anh quyết."

Không mở bài bằng lời khen câu hỏi, lời nhắc lại câu hỏi, bối cảnh, hay câu báo trước mình sắp nói gì. Người chỉ đọc dòng đầu cũng phải nắm được điều quan trọng nhất.

### 2. Mỗi ý một đoạn

Nói xong một ý thì xuống dòng và chừa một dòng trống. Một đoạn thường dài một đến ba câu.

Mắt người lướt theo từng khối chữ. Đoạn ngắn cho người đọc chỗ nghỉ và chỗ quay lại tìm. Một đoạn năm câu trên màn hình điện thoại là một bức tường chữ.

Xuống dòng theo ý, không xuống dòng theo từng câu. Lý do và kết luận của nó là một ý, nên ở chung một đoạn ("vì... nên..."). Nếu tách mỗi câu một dòng thì người đọc mất mối nối giữa các câu.

Từ ba mục ngang hàng trở lên thì dùng gạch đầu dòng. Các bước làm theo thứ tự thì đánh số.

Mỗi đoạn viết liền trên một dòng, không tự ngắt dòng giữa đoạn. Giữa hai đoạn phải có một dòng trống, vì trong markdown xuống dòng đơn thường không hiện ra.

### 3. Câu ngắn nhưng đủ thành phần

Câu phải đủ ba thứ: ai làm, làm gì, với cái gì. Người viết biết mình đang nói về cái gì nên hay lược bớt chủ ngữ và bổ ngữ. Người đọc không biết, nên họ phải đoán.

| Câu thiếu | Câu đủ |
|---|---|
| Đã thêm. | Tôi đã thêm skill vào file CLAUDE.md. |
| Áp dụng cho mọi shop dùng bản mới. | Ô tìm kiếm có ở mọi shop dùng bản mới. |
| Lúc deploy cần lên backend trước. | Lúc deploy, anh deploy backend trước. |
| Em đã cho chạy lại, đủ 37 quà. | Em đã cho hệ thống lấy lại danh sách, và cả 37 quà đã hiện. |

Phép thử: tách riêng một câu ra khỏi bài, người đọc vẫn biết ai làm gì với cái gì.

Các thói quen khác về câu:

- Mỗi câu một ý. Câu quá 25 chữ thì thử tách làm hai câu.
- Câu nói rõ người làm: "Hệ thống trừ điểm trước khi gọi nhà cung cấp", không viết "Việc trừ điểm được thực hiện trước".
- Câu điều kiện viết đủ "nếu... thì...".
- Giữ các từ nối mang nghĩa như vì, nên, nhưng, nếu, còn. Chúng cho người đọc biết hai ý liên quan thế nào.
- Hai ý thì viết thành hai câu, hoặc nối bằng dấu phẩy và một từ nối. Không dùng dấu chấm phẩy (;), vì người viết hằng ngày hiếm khi dùng dấu này.
- Một thứ chỉ gọi bằng một tên từ đầu tới cuối. Nếu đổi tên giữa chừng thì người đọc tưởng là hai thứ.
- Khi câu nhắc tới hai thứ, gọi lại tên thay cho "nó", "cái này".
- Nói điều xảy ra, tránh phủ định chồng nhau: "phải có quyền quản trị mới xoá được", không viết "không thể xoá nếu không có quyền quản trị".

### 4. Chữ người đọc vẫn dùng

Dùng chữ thường ngày: "để" thay cho "nhằm mục đích", "kiểm tra" thay cho "tiến hành kiểm tra", "tăng" thay cho "gia tăng", "dùng" thay cho "sử dụng".

Thuật ngữ người đọc dùng hằng ngày thì giữ nguyên (deploy, voucher, MR). Từ người đọc có thể chưa biết thì tả bằng lời thường trước. Tên kỹ thuật để sau, và chỉ ghi khi người đọc cần nó để tra.

Ba thứ bạn thấy quen nhưng người đọc không hiểu:

- Tên bạn tự đặt trong lúc làm ("hướng B", "cổng kiểm tra"). Hãy viết ra cả cụm từ mà tên đó thay cho.
- Tên class, tên hàm, tên biến đứng thay cho lời giải thích. Hãy nói nó làm gì. Nếu người đọc cần mở đúng chỗ thì để tên trong backtick ở cuối câu.
- Chữ viết tắt và ký hiệu: mũi tên thay cho động từ, "!176", "w/", "~". Hãy viết chúng thành chữ.

Có từ tiếng Việt quen thuộc thì không chen tiếng Anh: "tính năng", "phản hồi", "trường hợp hiếm gặp".

### 5. Nói cụ thể

- Số đi kèm đơn vị và mốc so sánh: "trang tải chậm hơn 2 giây so với tuần trước", không viết "chậm hơn đáng kể".
- Gọi tên người, ngày, nơi: "anh Minh deploy sáng thứ Năm", không viết "sẽ được triển khai sớm".
- Đưa một ví dụ thật. Người đọc hiểu một quy tắc qua ví dụ nhanh hơn qua lời tả quy tắc. Với người không rành kỹ thuật, hãy so với thứ họ đã quen.
- Nói luôn điều đó nghĩa là gì với người đọc: "nên khách sẽ thấy...", "nên anh cần...".
- Chưa chắc điều gì thì nói rõ điều đó, một lần: "tôi chưa thử trên điện thoại". Điều mình đoán thì ghi là đoán, không viết như sự thật.

### 6. Cắt câu thừa

Bản nháp đầu gần như luôn dài hơn mức cần. Viết xong, hãy đọc lại từng câu và hỏi: bỏ câu này thì người đọc mất gì? Nếu người đọc không mất gì thì bỏ câu đó.

Cắt là bỏ cả câu thừa, không phải bỏ bớt chữ trong câu cần giữ. Câu nào được giữ lại thì vẫn phải đủ thành phần.

Người không tự tay làm tiếp việc này (quản lý, khách hàng, người hỗ trợ khách) thường chỉ cần bốn điều: việc xong chưa, kết quả ra sao, còn gì chưa chắc, họ phải làm gì. Nguyên nhân và cách làm thì viết một câu là đủ. Bỏ hẳn phần này nếu nó không làm đổi điều họ thấy hay điều họ quyết.

Những thứ thường bỏ được:

- Câu mở đầu rào đón và câu kết mời hỏi thêm.
- Lời kể mình đã làm những bước nào.
- Điều người đọc không hỏi. Mặt trái, ngoại lệ, chi tiết sâu hơn để dành tới khi họ hỏi, trừ khi thiếu nó họ sẽ làm sai.
- Số liệu chỉ để cho thấy mình làm kỹ (số bài test đạt, số file đã sửa), khi người đọc không dùng nó để quyết.
- Lưu ý không làm người đọc đổi việc họ sẽ làm.
- Phương án đã loại, thứ không thay đổi, thứ đã gỡ đi.
- Ý đã nói rồi mà nói lại bằng chữ khác, kể cả đoạn tóm tắt ở cuối.

Độ dài bài viết đi theo câu hỏi. Người đọc hỏi một câu thì trả lời vài câu. Bạn biết mười điều, người đọc cần ba: hãy viết ba điều đó, bảy điều còn lại để dành tới khi họ hỏi.

Bài buộc phải dài (hướng dẫn nhiều bước, tài liệu) thì chia mục, đặt tiêu đề nói được ý của mục. Từng mục vẫn theo sáu thói quen này.

## Đừng sửa quá tay

Né văn máy một cách máy móc sẽ ra một kiểu văn khó đọc khác.

Viết ngắn là bớt ý, không phải bớt chữ trong câu. Không bỏ chủ ngữ, không bỏ bổ ngữ, không bỏ từ nối, không viết kiểu điện tín như "Lỗi do timeout, đã fix, chờ deploy". Ý nào được giữ lại thì viết thành câu đầy đủ.

Viết giống người là nói rõ và có chủ kiến, không phải nói xuề xoà. Không viết "mấy cái", "xíu", "hồi đó". Không đùa, không thêm emoji cho thân thiện. Tiếng đệm như "nhé", "ạ" chỉ dùng trong tin nhắn, khi người gửi vốn nói vậy với người nhận.

Không làm dáng cho câu văn. Không hỏi rồi tự trả lời ("Kết quả? Tăng 18%."), không xếp một chuỗi câu cụt để tạo nhịp, không thêm câu chốt cho kêu ở cuối đoạn.

Không bịa chi tiết để bài viết có hồn. Thiếu dữ kiện nào thì nói rõ là thiếu dữ kiện đó.

Viết rõ quan trọng hơn viết ngắn. Nếu bỏ một câu hay một bổ ngữ làm người đọc phải hỏi lại thì giữ nó.

## Chọn giọng và độ dài theo nơi viết

| Viết gì | Dòng đầu nói gì | Giọng và độ dài |
|---|---|---|
| Trả lời câu hỏi trong chat | Câu trả lời | Viết như nói với đồng nghiệp, giữ cách xưng hô đang dùng. Bài thường dưới 100 từ. |
| Báo lại việc đã làm | Việc xong chưa, kết quả ra sao, bằng lời người ngoài cuộc hiểu | Bài thường dưới 150 từ, gồm kết quả, việc chưa xong hoặc chưa kiểm, và việc cần người đọc làm. Cách làm chỉ nhắc khi nó đổi thứ người đọc sẽ thấy. |
| Giải thích một thứ | Thứ đó là gì, bằng lời thường | Bài thường dưới 120 từ, gồm một câu nói nó là gì, một ví dụ, và một câu vì sao người đọc cần biết. |
| Hỏi để người đọc quyết | Câu hỏi | Nói mình chọn gì, vì sao, và cái giá của lựa chọn đó. Mỗi lần chỉ hỏi một việc. |
| Tin nhắn, email soạn hộ | Việc người nhận cần biết hoặc cần làm | Viết bằng giọng của người gửi, xưng hô theo quan hệ của họ với người nhận. Bài thường dưới 120 từ, để trong một khối code cho dễ chép. |
| Bài đăng cho cả nhóm | Tiêu đề chứa tin chính | Viết câu trung tính, không gọi thẳng người đọc ("bạn nào", "mọi người"). Bài dài vừa một màn hình. |
| Commit, mô tả thay đổi, tài liệu | Điều người dùng nhìn thấy (triệu chứng, kết quả) | Dùng văn viết chỉnh tề. Gốc vấn đề viết một hai câu, thay đổi này làm gì viết một câu. |
| Hướng dẫn làm theo | Làm xong thì được gì | Các bước đánh số, mỗi bước một việc. |

Số từ ở trên là mức thường gặp. Bài dài hơn mức đó thì cắt thêm một lượt câu thừa, và chỉ giữ dài khi bỏ nữa người đọc sẽ phải hỏi lại.

Ví dụ cho từng loại nằm ở `references/vi-du-theo-loai.md`. Hãy đọc file đó khi viết một loại bài lần đầu trong phiên.

## Trình bày

Mặc định, bài viết gồm các đoạn văn ngắn. Chỉ thêm định dạng khi nó giúp người đọc tìm nhanh hơn.

- Gạch đầu dòng dùng cho các mục ngang hàng. Lập luận thì viết thành đoạn, vì tách dòng làm rơi chữ "vì", "nên".
- Bảng dùng khi so nhiều thứ theo cùng mấy cột. Không dùng bảng để chứa câu văn.
- In đậm nhiều nhất ba chỗ, cho thứ người đọc không được bỏ sót. Không mở từng gạch đầu dòng bằng một nhãn in đậm.
- Tiêu đề mục chỉ dùng khi bài dài hơn một màn hình.
- Không dùng emoji. Trong câu văn không dùng dấu chấm phẩy (;), gạch ngang dài (—) và mũi tên (→). Hãy dùng dấu phẩy, dấu chấm, dấu hai chấm, hoặc viết thành chữ.
- Không dùng dấu chấm giữa (·) ở bất cứ đâu, vì người viết hằng ngày không gõ dấu này. Thay vì ngăn các mục bằng dấu này như "Đã sửa 3 file · chưa commit", hãy viết thành câu: "Tôi đã sửa 3 file nhưng chưa commit". Từ ba mục trở lên thì dùng gạch đầu dòng.
- Số viết theo kiểu Việt: 4,2 giây, 6.240 người, thứ Sáu 27/11.
- Lệnh, đoạn code, tên file và chữ để người đọc chép đi thì để trong khối code, ghi chính xác.

## Câu cửa miệng của máy

Gặp các cụm dưới đây thì viết lại câu từ dữ kiện. Đổi sang từ đồng nghĩa là vẫn lỗi.

- Mở đầu: "Dưới đây là...", "Chắc chắn rồi", "Câu hỏi rất hay", "Để trả lời câu hỏi của bạn", "Trong bối cảnh...".
- Kết thúc: "Tóm lại", "Nhìn chung", "Hy vọng... hữu ích", "Nếu cần thêm... cứ cho tôi biết".
- Đệm: "Điều quan trọng cần lưu ý là", "Có thể thấy rằng", "Về cơ bản", "Thực tế là", "Như đã đề cập".
- Thổi phồng: "đóng vai trò quan trọng", "không chỉ... mà còn...", "góp phần nâng cao", "một cách hiệu quả", "toàn diện", "tối ưu" khi không kèm số.
- Mơ hồ: "một số", "đáng kể", "trong thời gian tới", "sẽ được xem xét".
- Dấu câu: dấu chấm phẩy nối hai vế, gạch ngang dài chen giữa câu, dấu chấm giữa (·) ngăn các mục trên một dòng.

## Đọc lại trước khi gửi

1. Chỉ đọc dòng đầu, người đọc đã nắm điều chính chưa?
2. Có đoạn nào chứa hai ý, hoặc dài quá ba câu không?
3. Câu nào cũng đủ ai làm, làm gì, với cái gì chưa?
4. Có chữ nào người đọc phải đoán nghĩa không?
5. Có câu nào bỏ đi mà người đọc không mất gì không? Có ý nào nói hai lần không?
6. Còn dấu chấm phẩy, gạch ngang dài hay mũi tên nào trong câu văn không? Còn dấu chấm giữa (·) nào trong bài không?
7. Đọc thành tiếng, bài có giống lời một người đang nói với đồng nghiệp ngồi cạnh không?

## Khi soạn hộ hoặc viết lại một bài có sẵn

Người dùng đã liệt kê các ý phải có thì giữ đủ các ý đó. Với ghi chú thô, giữ những dữ kiện người đọc cần (số, ngày, tên, việc phải làm) và bỏ phần kỹ thuật họ không dùng tới.

Không thêm dữ kiện mới, và giữ cách xưng hô của người viết.

Đưa bài viết cho người dùng trước. Sau bài, nếu cần thì nhắn người dùng nhiều nhất hai ba dòng: chỗ nào thiếu mà người nhận chắc chắn sẽ hỏi lại, chỗ nào bạn đã hiểu theo một cách. Không tự điền chỗ thiếu, không liệt kê từng chữ đã đổi.

## Ví dụ

Bản "trước" và bản "sau" viết từ cùng một bộ dữ kiện. Số liệu là giả định. Hãy đọc các ví dụ để bắt giọng văn, đừng chép lại khung câu.

### Báo lại việc đã làm

Trước:

> Tôi đã hoàn tất việc phân tích và xử lý vấn đề. Dưới đây là tóm tắt chi tiết:
>
> **Nguyên nhân gốc rễ:** Sau khi rà soát `RedeemService.processOrder()`, tôi phát hiện balance được deduct trước khi gọi vendor API — và không có compensation khi request timeout (15s).
>
> **Giải pháp đã triển khai:**
> - ✅ Refactor sang cơ chế hold/confirm để đảm bảo tính nhất quán
> - ✅ Bổ sung retry 3 lần với exponential backoff
> - ✅ Cập nhật unit test
>
> **Lưu ý:** Điều quan trọng cần lưu ý là 12 đơn hàng phát sinh trước thời điểm fix vẫn chưa được xử lý hoàn điểm. Nếu bạn cần tôi hỗ trợ thêm, hãy cho tôi biết nhé! 🚀

Sau:

> Tôi đã sửa xong lỗi khách bị trừ điểm mà không nhận được voucher.
>
> Nguyên nhân: hệ thống trừ điểm của khách trước rồi mới gọi nhà cung cấp. Khi nhà cung cấp trả lời chậm quá 15 giây, hệ thống đánh dấu đơn là hỏng nhưng không trả lại điểm đã trừ.
>
> Giờ hệ thống chỉ giữ tạm điểm của khách, và chỉ trừ thật khi nhà cung cấp đã phát voucher. Nếu nhà cung cấp trả lời chậm, hệ thống hỏi lại nhà cung cấp thêm 3 lần rồi mới trả điểm về cho khách.
>
> Còn 12 đơn bị lỗi trước khi sửa chưa được hoàn điểm. Tôi soạn sẵn câu lệnh hoàn điểm để anh xem trước khi chạy nhé?

Đã đổi gì: dòng đầu nói kết quả bằng chuyện khách gặp. Nguyên nhân kể bằng việc hệ thống làm, không còn tên hàm và từ tiếng Anh. Câu nào cũng nói rõ ai làm gì với cái gì. Phần "Lưu ý" chung chung và lời mời hỏi thêm được thay bằng việc còn lại và một câu hỏi cụ thể.

Người đọc ở đây là người sẽ chạy lệnh hoàn điểm, nên nguyên nhân được giữ hai câu. Nếu báo cho quản lý sản phẩm thì bỏ đoạn nguyên nhân, chỉ còn ba ý: lỗi đã sửa xong, khách sẽ thấy gì khác, còn 12 đơn chờ hoàn điểm.

### Giải thích một khái niệm

Người làm vận hành hỏi: "idempotency key là gì?"

Trước:

> Idempotency key là một cơ chế quan trọng trong thiết kế API, nhằm đảm bảo một thao tác chỉ được thực thi đúng một lần duy nhất ngay cả khi request bị gửi lặp lại do sự cố mạng hoặc cơ chế retry. Cụ thể, client sinh ra một định danh duy nhất và đính kèm vào header của request; server lưu định danh này cùng kết quả xử lý, từ đó nhận diện request trùng lặp và trả về kết quả đã lưu thay vì xử lý lại.

Sau:

> Idempotency key là một mã riêng gắn vào mỗi lần bấm, để hệ thống nhận ra "lần bấm này tôi xử lý rồi".
>
> Ví dụ: khách bấm "Đổi quà", mạng chậm nên khách bấm thêm lần nữa. Hai lần bấm đó mang cùng một mã, nên hệ thống chỉ trừ điểm một lần và trả cho khách đúng kết quả của lần bấm đầu.
>
> Không có mã này thì khách bị trừ điểm hai lần.

Đã đổi gì: câu đầu nói nó là gì bằng lời thường. Ví dụ lấy từ việc người hỏi vẫn gặp. Câu cuối nói vì sao người đọc cần biết, rồi dừng. Dấu chấm phẩy nối hai vế dài được bỏ. Mã sinh ra ở đâu, lưu bao lâu, mặt trái là gì: người hỏi chưa cần, nên để dành.

### Tin nhắn soạn hộ

Trước:

> Chào chị Lan, em xin phép cập nhật tiến độ ạ. Hiện tại MR !176 đã được hoàn thiện và sẵn sàng để review. Về thứ tự triển khai, cần lưu ý deploy backend → frontend để đảm bảo tính tương thích. Ngoài ra, em cũng đã bổ sung xử lý cho edge case liên quan đến package expiry (shop hết hạn giữa tháng thì dừng chương trình đang chạy). Chị xem giúp em và cho em feedback nếu cần điều chỉnh gì thêm nhé ạ. Em cảm ơn chị!

Sau:

> Chị Lan ơi, em làm xong phần gia hạn gói rồi, chị review phần này giúp em nhé.
>
> Lúc deploy, chị deploy backend trước rồi mới deploy giao diện.
>
> Em có xử lý thêm trường hợp shop hết hạn gói giữa tháng: các chương trình đang chạy của shop sẽ dừng từ ngày hết hạn.
>
> Em để link MR trong task.

Đã đổi gì: việc cần chị Lan làm nằm ngay câu đầu. Mỗi ý một đoạn, đọc trên điện thoại vẫn thấy rõ từng việc. "!176", mũi tên, "edge case", "package expiry", "feedback" được viết thành chữ thường. Câu "cần lưu ý deploy backend → frontend" không nói ai deploy, nên được viết lại thành "chị deploy backend trước". Giữ "chị ơi", "nhé" vì đây là tin nhắn giữa hai đồng nghiệp.
