# Mẫu Báo Cáo Tổng Kết Đề Tài — Trường Đại Học Tây Bắc (TBU)

Đây là mẫu LaTeX chuẩn dùng cho **Báo cáo tổng kết đề tài** (đề tài môn học, đồ án...) của Trường Đại học Tây Bắc, Do tôi là Lò Mạnh Đạt tạo ra để thuận tiện cho việc làm báo cáo bằng LaTeX.

---

## 1. Cập Nhật Thông Tin Ở Đâu?

Bạn chỉ cần mở đúng các file sau để thay đổi thông tin tương ứng:

| Thông tin cần thay đổi                                    | Tệp / Thư mục cần vào | Nội dung chính                                                                                         |
| :-------------------------------------------------------- | :-------------------- | :----------------------------------------------------------------------------------------------------- |
| **Thông tin trang bìa**                                   | `thongtinbia.tex`     | Tên đề tài, Giảng viên hướng dẫn, Lớp, Nhóm và Danh sách sinh viên thực hiện (`\addstudent{...}`).     |
| **Lời cam đoan, Lời cảm ơn, Phân công việc, Từ viết tắt** | `Gioithieu_danhmuc/`  | Chỉnh sửa trực tiếp trong các file: `loicamdoan.tex`, `loicamon.tex`, `phancong.tex`, `tuviettat.tex`. |
| **Nội dung các chương**                                   | `Noidungbaocao/`      | Viết nội dung trong các file: `modau.tex`, `chuong1.tex`, `chuong2.tex`, `chuong3.tex`, `ketluan.tex`. |
| **Tài liệu tham khảo**                                    | `tailieuthamkhao.bib` | Thêm các nguồn trích dẫn tài liệu tham khảo theo định dạng BibTeX.                                     |

---

## 2. Cách Thêm File Mới / Nội Dung Mới (Chỉ 2 Bước)

Khi bạn muốn thêm một chương mới hoặc một mục riêng:

- **Bước 1: Tạo file `.tex` mới**
  - Ví dụ: Tạo file `chuong4.tex` nằm trong thư mục `Noidungbaocao/` với nội dung:
    ```latex
    \chapter{KẾT QUẢ THỰC NGHIỆM VÀ ĐÁNH GIÁ}
    \section{Môi trường thử nghiệm}
    Nội dung viết ở đây...
    ```

- **Bước 2: Nạp file vào `main.tex` bằng lệnh `\input`**
  - Mở file `main.tex`, tìm đến vị trí bạn muốn nội dung xuất hiện và chèn lệnh:
    ```latex
    \input{Noidungbaocao/chuong4.tex}
    ```

---

## 3. Quy Chuẩn Định Dạng Sẵn Có (`tbu_report.sty`)

- **Căn lề A4**: Trên `2.0 cm` — Dưới `2.0 cm` — Trái `3.0 cm` — Phải `1.5 cm`.
- **Phông chữ**: Times New Roman 12pt, giãn dòng 1.3, thụt đầu dòng 1.0 cm.
- **Khung bìa đôi**: Tự động vẽ đúng chuẩn quy định của Trường ĐH Tây Bắc.

---

## 4. Biên Dịch (Compile)

Dùng **VS Code** (tiện ích **LaTeX Workshop**) nhấn Lưu hoặc chạy lệnh terminal:

```bash
latexmk -pdf main.tex
```
