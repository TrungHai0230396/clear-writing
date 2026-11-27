# clear-writing

Skill này giúp Claude viết như một người nắm việc đang nói với đồng nghiệp: điều chính nói trước, mỗi ý một đoạn, câu đủ chủ ngữ và bổ ngữ, chữ thường ngày. Người đọc đọc một lần là hiểu, và biết mình cần làm gì tiếp.

Claude dùng skill cho mọi thứ viết ra cho người khác đọc: câu trả lời trong chat, lời báo lại việc đã làm, tin nhắn soạn hộ, commit, mô tả thay đổi, thông báo, hướng dẫn.

## Ví dụ

Người làm vận hành hỏi Claude: "idempotency key là gì?"

Một câu trả lời kiểu máy viết:

> Idempotency key là một cơ chế quan trọng trong thiết kế API, nhằm đảm bảo một thao tác chỉ được thực thi đúng một lần duy nhất ngay cả khi request bị gửi lặp lại do sự cố mạng hoặc cơ chế retry. Cụ thể, client sinh ra một định danh duy nhất và đính kèm vào header của request; server lưu định danh này cùng kết quả xử lý, từ đó nhận diện request trùng lặp và trả về kết quả đã lưu thay vì xử lý lại.

Câu trả lời theo skill:

> Idempotency key là một mã riêng gắn vào mỗi lần bấm, để hệ thống nhận ra "lần bấm này tôi xử lý rồi".
>
> Ví dụ: khách bấm "Đổi quà", mạng chậm nên khách bấm thêm lần nữa. Hai lần bấm đó mang cùng một mã, nên hệ thống chỉ trừ điểm một lần và trả cho khách đúng kết quả của lần bấm đầu.
>
> Không có mã này thì khách bị trừ điểm hai lần.

## Cài vào Claude Code

Chạy lệnh sau để tải skill vào thư mục skill của Claude Code:

```bash
git clone https://github.com/TrungHai0230396/clear-writing.git ~/.claude/skills/clear-writing
```

Sau đó bạn mở một phiên Claude Code mới. Claude sẽ tự gọi skill khi thấy có việc cần viết, hoặc bạn gõ `/clear-writing` để gọi thẳng.

Nếu muốn Claude viết theo skill ở mọi phiên, bạn thêm dòng sau vào file `~/.claude/CLAUDE.md`:

```
@~/.claude/skills/clear-writing/SKILL.md
```

Khi skill có bản mới, bạn chạy lệnh sau để cập nhật:

```bash
git -C ~/.claude/skills/clear-writing pull
```

## Cài vào app Claude

Nếu bạn dùng Claude trên web hoặc ứng dụng máy tính, bạn làm theo các bước sau:

1. Tải file [clear-writing.zip](https://github.com/TrungHai0230396/clear-writing/releases/latest/download/clear-writing.zip).
2. Vào Settings > Capabilities, bật mục "Code execution and file creation". Bản mới của app gọi mục này là "Create and edit files".
3. Vào Customize > Skills, bấm dấu +, chọn "Create skill", rồi chọn "Upload a skill" và chọn file vừa tải.

Cài xong, bạn mở cuộc trò chuyện mới thì Claude mới dùng skill. Khi skill có bản mới, bạn tải file zip mới và tải lên lại.

## Các file trong kho

- `SKILL.md`: sáu thói quen viết, cách chọn giọng và độ dài theo từng loại bài, và các ví dụ trước và sau.
- `references/vi-du-theo-loai.md`: ví dụ cho bảy loại bài khác. Claude đọc file này khi viết một loại bài lần đầu trong phiên.

## Giấy phép

Skill dùng giấy phép MIT, nên ai cũng được dùng, sửa và chia sẻ lại.
