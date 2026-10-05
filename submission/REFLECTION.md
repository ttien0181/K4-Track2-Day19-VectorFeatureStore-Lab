# Reflection — Lab 19

**Tên:** Hoàng Anh Tú
**Cohort:** 4
**Path đã chạy:** Lite (uv, Windows)

---

## Câu hỏi (≤ 200 chữ)

> Trên golden set 50 queries, mode nào thắng ở loại query nào (`exact` /
> `paraphrase` / `mixed`), và tại sao? Khi nào bạn **không** dùng hybrid
> (i.e. khi nào pure BM25 hoặc pure vector là lựa chọn đúng)?

Trên 50 câu hỏi chuẩn, Hybrid đạt Precision@10 **78,6%**, hơn BM25 **77,8%** và vector **73,2%**. Với `exact`, BM25 và Hybrid cùng **96,7%**, hơn vector **88,7%** vì từ khóa kỹ thuật trùng văn bản. Với `mixed`, Hybrid đạt **100%**, hơn BM25 **97,0%** và vector **98,5%** nhờ RRF kết hợp hai tín hiệu. Riêng `paraphrase`, BM25 **33,3%**, Hybrid **32,0%**, vector **24,0%**: model Lite `bge-small-en-v1.5` thiên tiếng Anh, nên chưa biểu diễn tốt câu tiếng Việt diễn đạt lại.

Tôi dùng BM25 thuần khi truy vấn chứa mã hoặc thuật ngữ chính xác và ưu tiên độ trễ thấp. Tôi chỉ dùng vector thuần nếu phép đo trên dữ liệu thực cho thấy tìm kiếm ngữ nghĩa vượt tìm kiếm từ khóa, chẳng hạn sau khi chọn embedding đa ngữ phù hợp. Hybrid hữu ích nhất khi câu hỏi có cả từ khóa cụ thể lẫn ý diễn đạt khác.

---

## Điều ngạc nhiên nhất khi làm lab này

Trên chính tập dữ liệu này, vector không thắng nhóm `paraphrase` như kỳ vọng; kết quả đo quan trọng hơn giả định về thuật toán.

---

## Bonus challenge

- [ ] Đã làm bonus (không thuộc phạm vi bài nộp này)
