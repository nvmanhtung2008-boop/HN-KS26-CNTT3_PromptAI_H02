# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:** Nguyễn Văn Mạnh Tùng
- **Lớp:** HN-KS26-CNTT3
- **Link repository Pha2:https://github.com/nvmanhtung2008-boop/HN-KS26-CNTT3_PromptAI_H02.git**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):Gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "một bạn đi xe lăn"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/5x93BXBP3fcz   

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền vé người lớn:**
* Đoàn mua vé cả ngày (VECN) với đơn giá 250.000 đồng/vé người lớn.
* Số lượng: 8 người lớn.
* Tiền vé người lớn = $8 \times 250.000 = 2.000.000$ đồng.


2. **Tiền vé trẻ em:**
* 4 trẻ em cao 1,05 m, 1,15 m, 1,2 m và 1,3 m đều nằm trong khoảng từ 1 m đến 1,4 m nên tính 60% giá vé người lớn: $250.000 \times 60\% = 150.000$ đồng/vé.
* 2 bé cao dưới 1 m được miễn phí (0 đồng).
* Tiền vé trẻ em = $(4 \times 150.000) + (2 \times 0) = 600.000$ đồng.


3. **Tổng vé:**
* Tổng tiền vé trước khi giảm = Tiền vé người lớn + Tiền vé trẻ em = $2.000.000 + 600.000 = 2.600.000$ đồng.


4. **Giảm giá đoàn:**
* Đoàn có 8 người lớn, đủ điều kiện hưởng ưu đãi đoàn từ 8 người lớn trở lên (giảm 10% trên tiền vé).
* Số tiền được giảm = $2.600.000 \times 10\% = 260.000$ đồng.
* Tiền vé sau giảm = $2.600.000 - 260.000 = 2.340.000$ đồng.


5. **Phụ thu:**
* Đoàn thuê 6 áo phao với giá 40.000 đồng/chiếc (không áp dụng giảm giá).
* Phụ thu = $6 \times 40.000 = 240.000$ đồng.


6. **Tổng tiền:**
* Tổng tiền = Tiền vé sau giảm + Phụ thu = $2.340.000 + 240.000 = 2.580.000$ đồng.



[RESULT: 2.580.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/UhKKZqMdL8FA

### b) Kiểm tra kết quả AI

Kết quả AI đã đúng 

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
[
  {
    "loai_su_co": "dong_khu_choi",
    "so_khach": 4,
    "so_khu_bi_dong": 2,
    "tom_tat": "Khu trượt nước chính và khu sóng nhân tạo đóng cửa cả ngày 02/11/2026 không thông báo trước trên website; tổng mức đền bù dự kiến 480.000 đồng (cần Giám đốc vận hành duyệt trước khi gửi khách)."
  },
  {
    "loai_su_co": "nhan_vien",
    "so_khach": 4,
    "so_khu_bi_dong": 0,
    "tom_tat": "Khách hàng khen ngợi nhân viên cứu hộ chu đáo và không có phàn nàn về nhân viên (không áp dụng đền bù)."
  },
  {
    "loai_su_co": "khac",
    "so_khach": 4,
    "so_khu_bi_dong": 0,
    "tom_tat": "Khách hàng đề nghị công viên có phương án giải quyết thỏa đáng; chuyển bộ phận Chăm sóc khách hàng phối hợp xử lý."
  }
]
```

**Link trò chuyện:**https://share.gemini.google/sIQX0QmtqebL

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0/5.0 *(Chưa thể xác minh)* | Trích: *"Vé chiều bên em 150k thôi ạ"*, *"Mưa mà đóng cửa thì bên em hoàn tiền mặt 100% cho chị nha."* Lý do: Hệ thống chưa được cung cấp bảng giá và chính sách thời tiết chuẩn để đối chiếu tính chính xác. | Đối chiếu lại bảng giá vé chiều và chính sách hoàn/đổi vé chính thức của công ty trước khi gửi khách hàng. |
| **Đầy đủ (30%)** | 2.0/3.0 | Trích: *"Cần gì ới em nhé!"* Lý do: Đã trả lời 2 câu hỏi về giá và chính sách mưa, nhưng thiếu bước chủ động mời khách cung cấp ngày chơi và số lượng vé để hỗ trợ đặt vé. | *"Nếu chị có nhu cầu đặt vé, vui lòng cho em xin thông tin ngày dự kiến tham quan và số lượng vé để em hỗ trợ giữ chỗ cho chị ạ."* |
| **Giọng điệu (20%)** | 0.5/2.0 | Trích: *"Hello chị!"*, *"mát rượi luôn"*, *"cho chị nha"*, *"Cần gì ới em nhé!"* Lý do: Sử dụng nhiều từ ngữ suồng sã, thiếu trang trọng và không phù hợp với tiêu chuẩn giao tiếp chuyên nghiệp. | *"Chào chị ạ. Giá vé buổi chiều hiện tại là [giá chuẩn]. Trong trường hợp cơ sở đóng cửa do thời tiết, bên em sẽ áp dụng [chính sách chuẩn]. Chị vui lòng phản hồi nếu cần hỗ trợ thêm ạ."* |
| **Tổng điểm** | **2.5/10** | *(Chưa tính 5.0 điểm tiêu chí Đúng thông tin do thiếu dữ liệu chuẩn để đối chiếu)* | Bổ sung thông tin chuẩn để hoàn tất đánh giá và yêu cầu nhân viên điều chỉnh văn phong chuyên nghiệp hơn. |
```

**Link trò chuyện:**https://share.gemini.google/45z2DHi2CYo5
