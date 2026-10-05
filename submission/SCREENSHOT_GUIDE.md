# Hướng dẫn tự chụp ảnh minh chứng

Các notebook `notebooks/01_*.ipynb` đến `08_*.ipynb` đã lưu output sau khi chạy. Trong VS Code, mở từng tệp `.ipynb` và kéo đến ô output được nêu dưới đây. Nếu VS Code hỏi kernel, chọn `.venv\Scripts\python.exe`. Dùng **Win + Shift + S**, chụp vùng gồm tiêu đề mục và kết quả đọc được, rồi lưu PNG vào `submission/screenshots/`. Không cần chạy lại notebook chỉ để chụp.

| Notebook | Nội dung cần hiện rõ trong ảnh | Tên ảnh gợi ý |
|---|---|---|
| NB1 | `Indexed: 1000 vectors`, top 5 của truy vấn trực tiếp và top 5 truy vấn paraphrase (5 kết quả `cloud`) | `nb1_indexed_1000.png` |
| NB2 | Bảng Precision@10 trung bình của Keyword, Semantic, Hybrid và bảng theo `exact`/`paraphrase`/`mixed` | `nb2_precision_table.png` |
| NB3 | Mẫu `/search` có `latency_ms`, bảng P50/P95/P99 cho ba mode và dòng `PASS — hybrid P99 < 50ms` | `nb3_latency_p99.png` |
| NB4 | `feast apply` hiện đủ 3 feature views; log materialize; online lookup với P99 < 10 ms; bảng Point in Time có 3 dòng | `nb4_feast_materialize.png` |
| NB5 | Bảng recall theo độ chọn lọc và over-fetch ladder với `fetch_k=500` đạt recall 1,00 | `nb5_filtered_search.png` |
| NB6 | Bảng ba chiến lược cùng ngân sách 16 tài liệu, trace thử lại sau filter rỗng, và output `features` + `doc_ids` | `nb6_agent_retrieval.png` |
| NB7 | Bảng ngưỡng gồm hai cột tiết kiệm/trả lời sai và demo `namespaced=False` rò, `True` trả MISS | `nb7_semantic_cache.png` |
| NB8 | Bảng target encoding gap, tỷ lệ rò cùng AUC Point in Time/latest, và hai ratio khác nhau của cùng `u_000` | `nb8_feature_engineering.png` |

Nếu các kết quả của một notebook không vừa trong một ảnh, chụp thêm ảnh thứ hai với hậu tố `_2.png`. Đặc biệt NB4 có nhiều output dài; ưu tiên ảnh rõ chữ thay vì cố thu nhỏ tất cả vào một khung. Giữ nguyên output thật của notebook và điền họ tên trong `submission/REFLECTION.md` trước khi nộp.
