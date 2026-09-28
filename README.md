# BÁO CÁO BÀI TẬP VỀ NHÀ — TỔNG HỢP 2 MÔN

| Thông tin | Nội dung |
|---|---|
| **Môn học** | Lập trình Web **+** An toàn và Bảo mật Thông tin |
| **Lớp** | 59KMT |
| **Giảng viên hướng dẫn** | Đỗ Duy Cốp |
| **Sinh viên thực hiện** | Trần Văn Khải |
| **MSSV** | K235480106035 |
| **Deadline** | 23h59 ngày 28/9/2026 |
| **Hình thức** | Push lên GitHub (public) |

---

## 1. Giới thiệu
Repository này **tổng hợp 2 đợt bài tập** của 2 môn. Mỗi môn nằm trong một thư mục riêng,
có **báo cáo (README) đầy đủ**, code, bằng chứng chạy và ảnh minh chứng.

## 2. Mục lục

| Thư mục | Môn học | Nội dung chính | Báo cáo |
|---|---|---|---|
| [`BAITAP_LTW/`](BAITAP_LTW/) | Lập trình Web | Docker Compose (nginx, Node-RED, MariaDB, phpMyAdmin, cloudflared) + API Node-RED, 2 website / 2 domain | [README](BAITAP_LTW/README.md) |
| [`BAITAP_ATTT/`](BAITAP_ATTT/) | An toàn và Bảo mật Thông tin | DES/AES (cài đặt AES), RSA (sinh khóa), 3 mô hình RSA, so sánh RSA–AES, hybrid | [README](BAITAP_ATTT/README.md) |

## 3. Cấu trúc thư mục

```text
BAITAP/
├── README.md                 # báo cáo tổng hợp (file này)
├── BAITAP_LTW/               # Môn Lập trình Web
│   ├── README.md
│   ├── bt01_docker-compose/
│   ├── bt02_nodered-api/
│   ├── evidence/
│   └── images/
└── BAITAP_ATTT/              # Môn An toàn và Bảo mật Thông tin
    ├── README.md
    ├── bt01_des-aes/
    ├── bt02_rsa-keygen/
    ├── bt03_rsa-models-hybrid/
    ├── evidence/
    └── images/
```

## 4. Cách chạy (tóm tắt)

**Lập trình Web** — dựng hệ thống Docker:
```bash
cd BAITAP_LTW/bt01_docker-compose
cp .env.example .env      # điền token Cloudflare + mật khẩu DB
docker compose up -d
```

**An toàn & Bảo mật** — chạy các bài mã hóa:
```bash
cd BAITAP_ATTT
pip3 install pycryptodome
bash run-all.sh
```

## 5. Tiến độ

- [x] Môn Lập trình Web: Bài 1 (Docker Compose + 2 website/2 domain) và Bài 2 (API Node-RED + JS)
- [x] Môn An toàn & Bảo mật: Bài 1 (DES/AES), Bài 2 (RSA), Bài 3 (mô hình RSA + so sánh + hybrid)
- [x] README báo cáo cho từng môn
- [x] Ảnh minh chứng / bằng chứng chạy
- [ ] Bổ sung ảnh chụp màn hình cho môn ATTT (đang bổ sung)

## 6. Kết quả nổi bật

| Môn | Kết quả |
|---|---|
| Lập trình Web | 2 website chạy trên `web1/web2.kh4idev.id.vn` (HTTPS qua Cloudflare Tunnel), API `/api/tacke` trả JSON |
| An toàn & Bảo mật | AES-128 đạt vector FIPS-197; RSA-2048 sinh khóa OK; 3 mô hình RSA hợp lệ; hybrid RSA+AES OK |

---
*Báo cáo được trình bày bởi Trần Văn Khải — MSSV: K235480106035.*
