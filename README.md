<p align="center">
  <img src="docs/banner.svg" alt="Analog Electronics Lab — LTspice Workspace — LM324 / LM339 / NE555 — HCMUS FETEL" width="100%" />
</p>

<h2 align="center">⚡ Thực Hành Điện Tử Tương Tự — HCMUS FETEL ⚡</h2>

<p align="center">
  <img src="https://img.shields.io/badge/Môn%20học-Thực%20hành%20Điện%20tử%20Tương%20tự-0f766e?style=for-the-badge" alt="Môn học" />
  <img src="https://img.shields.io/badge/Công%20cụ-LTspice%20(SPICE)-1d4ed8?style=for-the-badge&logo=texasinstruments&logoColor=white" alt="LTspice" />
  <img src="https://img.shields.io/badge/IC%20chính-LM324%20•%20LM339%20•%20NE555-7c3aed?style=for-the-badge" alt="IC chính" />
  <img src="https://img.shields.io/badge/Số%20bài-8%20bài%20mô%20phỏng-D95319?style=for-the-badge" alt="8 bài" />
  <img src="https://img.shields.io/badge/Status-Lab%20workspace%20hoàn%20chỉnh-22c55e?style=for-the-badge" alt="Status" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Trường-VNUHCM%20•%20HCMUS-003366?style=flat-square" alt="HCMUS" />
  <img src="https://img.shields.io/badge/Khoa-Điện%20tử%20Viễn%20thông%20(FETEL)-2563eb?style=flat-square" alt="FETEL" />
  <img src="https://img.shields.io/badge/Chuyên%20ngành-Kỹ%20thuật%20Điện%20tử%20Viễn%20thông-0f766e?style=flat-square" alt="ĐTVT" />
  <img src="https://img.shields.io/badge/Hệ-Chất%20lượng%20cao%20•%20K2022-D95319?style=flat-square" alt="K2022 CLC" />
</p>

<p align="center">
  <a href="https://github.com/lhlizdabezt/ThucHanhDienTuTuongTu">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=3600&pause=900&color=8B0000&center=true&vCenter=true&multiline=true&width=860&height=70&lines=LTspice+simulations+%E2%80%A2+Op-amp+%E2%80%A2+Comparator+%E2%80%A2+Oscillator+%E2%80%A2+Filter;From+Kirchhoff+formulas+to+real+waveforms+%E2%80%A2+8+labs+%E2%80%A2+~30+schematics" alt="Motion tagline" />
  </a>
</p>

---

## 🎯 Tổng quan

Repository tổng hợp **toàn bộ workspace thực hành môn Điện tử Tương tự** tại Khoa Điện tử Viễn thông — HCMUS, bao gồm:

- 🧪 **~30 schematic LTspice** (`.asc`) cho **8 bài thực hành** — từ làm quen op-amp đến mạch chuyển đổi tín hiệu.
- 🔬 **SPICE macromodel + symbol** cho LM324 (op-amp) và LM339 (comparator) — dùng được offline, không phụ thuộc thư viện ngoài.
- 📊 **Kết quả mô phỏng** (`.raw`, `.log`, `.op.raw`, `.db`) — waveform, operating point và log tự động sinh sau khi `Run` schematic.
- 📕 **Tài liệu lý thuyết & hướng dẫn lab** (PDF) — đề cương, lời giải Bài 5 (slew rate, Schmitt, dao động), datasheet TI gốc.

Bộ workspace này được thiết kế để **ai mở ra cũng chạy lại được mô phỏng** — đối chiếu giữa công thức lý thuyết, tham số linh kiện và kết quả thực tế trên LTspice.

---

## 📑 Mục lục

- [Cây thư mục](#-cây-thư-mục)
- [Tóm tắt 8 bài thực hành](#-tóm-tắt-8-bài-thực-hành)
- [Linh kiện & mô hình SPICE](#-linh-kiện--mô-hình-spice)
- [Cách mở và chạy lại mô phỏng](#️-cách-mở-và-chạy-lại-mô-phỏng)
- [Ghi chú khi đọc kết quả](#-ghi-chú-khi-đọc-kết-quả)
- [Tài liệu tham khảo trong repo](#-tài-liệu-tham-khảo-trong-repo)
- [Bản quyền & học thuật](#-bản-quyền--học-thuật)

---

## 🗂️ Cây thư mục

```text
ThucHanhDienTuTuongTu/
├── README.md                            # Tài liệu này
├── RELEASE_NOTES.md                     # Ghi chú release v1.0.0
├── docs/
│   └── banner.svg                       # Banner README (offline)
│
├── Labs Dientu_tuongtu_unlocked.pdf     # ✦ Đề cương + hướng dẫn 8 bài (unlocked)
├── LYTHUYET.pdf                         # ✦ Tóm tắt lý thuyết op-amp / comparator / 555 / LDO / DAC
├── Bai 5 Cau 2.pdf                      # ✦ Lời giải Bài 5 — Câu 2 (Schmitt trigger / nguỡng)
├── Bai 5 Cau 3.pdf                      # ✦ Lời giải Bài 5 — Câu 3 (dao động NE555 / LM339)
├── LM324 Texas.pdf                      # ✦ Datasheet Texas Instruments — LM324 quad op-amp
├── LM339N texas.pdf                     # ✦ Datasheet Texas Instruments — LM339 quad comparator
│
└── CoHa/                                # Toàn bộ schematic + macromodel + simulation output
    ├── LM324.cir   /  LM324.asy         # SPICE macromodel + symbol LTspice cho LM324
    ├── LM339.cir   /  LM339.asy         # SPICE macromodel + symbol LTspice cho LM339
    │
    ├── BAI 1 CHUAN BI & THUC HANH.asc
    ├── BAI 2 CHUAN BI 2.asc             /  BAI 2 THUC HANH 1.asc … THUC HANH 4.asc
    ├── BAI 3 CHUAN BI 1.asc / CHUAN BI 3.asc / THUC HANH 1.asc … THUC HANH 3.asc
    ├── BAI 4 CHUAN BI 2.asc / CHUAN BI 3.asc / THUC HANH 1.asc … THUC HANH 3.asc
    ├── BAI 5 CHUAN BI 1.asc / THUC HANH 1.asc
    ├── BAI 6 … BAI 8 *.asc              # Mạch phi tuyến, nguồn, chuyển đổi tín hiệu
    │
    └── *.raw / *.log / *.op.raw / *.db  # Artifact mô phỏng — tự sinh lại khi Run schematic
```

> 💡 Mở `CoHa/` bằng LTspice là chạy được luôn — không cần copy thư viện vào thư mục cài đặt LTspice, vì `.asy` và `.cir` đã được đặt cùng workspace.

---

## 📚 Tóm tắt 8 bài thực hành

<table>
  <thead>
    <tr>
      <th>Bài</th>
      <th>Chủ đề kỹ thuật</th>
      <th>Mạch mô phỏng tiêu biểu</th>
      <th>Lệnh SPICE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>1</b></td>
      <td><b>Làm quen LTspice &amp; op-amp</b></td>
      <td>Khuếch đại đảo / không đảo dùng <code>LM324</code>, nguồn đối xứng ±12 V, kích sin/xung</td>
      <td><code>.tran</code> · <code>.ac</code></td>
    </tr>
    <tr>
      <td align="center"><b>2</b></td>
      <td><b>Đáp ứng op-amp &amp; slew rate</b></td>
      <td>Mạch khuếch đại tín hiệu sin/xung, quan sát biến dạng do giới hạn tốc độ đáp ứng của <code>LM324</code></td>
      <td><code>.tran</code></td>
    </tr>
    <tr>
      <td align="center"><b>3</b></td>
      <td><b>Mạch cộng — trừ &amp; so sánh</b></td>
      <td>Tổng hợp tín hiệu (summing amp), comparator/Schmitt trigger dùng <code>LM339</code>, ngưỡng tham chiếu</td>
      <td><code>.tran</code> · <code>.dc</code></td>
    </tr>
    <tr>
      <td align="center"><b>4</b></td>
      <td><b>Mạch lọc tích cực</b></td>
      <td>Lọc thông thấp / thông cao / thông dải bậc 1–2, mạng R-C ghép với <code>LM324</code></td>
      <td><code>.ac</code> Bode</td>
    </tr>
    <tr>
      <td align="center"><b>5</b></td>
      <td><b>Mạch dao động</b></td>
      <td>Dao động sóng vuông dùng <code>LM339</code> + R-C, mạch <code>NE555</code> astable — đối chiếu sai số mô phỏng vs công thức</td>
      <td><code>.tran</code></td>
    </tr>
    <tr>
      <td align="center"><b>6</b></td>
      <td><b>Mạch phi tuyến</b></td>
      <td>Chỉnh lưu chính xác, diode-op-amp clipper/limiter, bias BJT, mạch hồi tiếp âm/dương</td>
      <td><code>.tran</code> · <code>.dc</code></td>
    </tr>
    <tr>
      <td align="center"><b>7</b></td>
      <td><b>Nguồn &amp; mạch ứng dụng</b></td>
      <td>Bơm điện tích, nguồn tham chiếu, <b>LDO</b> bằng op-amp + MOSFET, mạch diode-tụ tạo điện áp cao</td>
      <td><code>.tran</code> · <code>.op</code></td>
    </tr>
    <tr>
      <td align="center"><b>8</b></td>
      <td><b>Mạch chuyển đổi tín hiệu</b></td>
      <td>Mạng điện trở <b>DAC</b> R-2R, level shifter, ADC kiểu so sánh dùng <code>LM339</code></td>
      <td><code>.tran</code> · <code>.dc</code></td>
    </tr>
  </tbody>
</table>

---

## 🔌 Linh kiện &amp; mô hình SPICE

| Linh kiện       | Vai trò                                                                 | File macromodel / symbol                         |
| --------------- | ----------------------------------------------------------------------- | ------------------------------------------------ |
| **LM324**       | Op-amp công suất thấp — khuếch đại, lọc, cộng/trừ, chỉnh lưu chính xác | `CoHa/LM324.cir` · `CoHa/LM324.asy`              |
| **LM339**       | Comparator 4 kênh ngõ ra open-collector — Schmitt, dao động sóng vuông  | `CoHa/LM339.cir` · `CoHa/LM339.asy`              |
| **NE555**       | Timer chế độ astable — đối chiếu với dao động dùng LM339                | LTspice built-in                                 |
| `1N4148`        | Diode tín hiệu — clipper, chỉnh lưu, mạch phi tuyến                     | LTspice built-in                                 |
| Schottky diode  | Sụt áp thấp cho mạch bơm điện tích, LDO                                 | LTspice built-in                                 |
| `2N3904` BJT    | Bias transistor cho mạch khuếch đại / công tắc                          | LTspice built-in                                 |
| `IRF530` MOSFET | Pass-element trong mạch LDO Bài 7                                       | LTspice built-in                                 |
| R, C            | Mạng phụ thuộc — định nghĩa hằng số thời gian, tần số cắt, hệ số Q       | LTspice built-in                                 |

> ⚠️ **Lưu ý LM339:** ngõ ra open-collector — luôn kéo lên qua điện trở `R_pull` ~10 kΩ về VCC khi dùng làm Schmitt trigger hoặc dao động.

---

## 🛠️ Cách mở và chạy lại mô phỏng

### 1. Cài đặt
- **Hệ điều hành:** Windows / macOS / Linux (qua Wine)
- **Phần mềm:** [LTspice XVII trở lên](https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html) — miễn phí, do Analog Devices phát hành.

### 2. Mở schematic

```text
1. Clone repo:    git clone https://github.com/lhlizdabezt/ThucHanhDienTuTuongTu
2. Mở LTspice  →  File → Open → chọn file trong CoHa/, ví dụ:
                  CoHa/BAI 5 THUC HANH 1.asc
3. LTspice tự nhận LM324.asy / LM339.asy / .cir trong cùng thư mục.
4. Bấm Run (icon ⚡ hoặc phím Alt+R) → mở waveform viewer.
```

### 3. Đo đại lượng

| Đại lượng cần đo               | Cách lấy trong LTspice                                              |
| ------------------------------ | ------------------------------------------------------------------- |
| Biên độ, tần số, chu kỳ        | Click chuột trên waveform → cursor → đọc cursor 1 / cursor 2        |
| Pha tín hiệu                   | Chế độ `.ac` → bấm tab phase trong waveform viewer                  |
| Ngưỡng chuyển trạng thái       | `.dc` sweep → đọc giao điểm với trục Y                              |
| Slew rate                      | Phóng to cạnh xung → đo dV/dt qua cursor                            |
| Tần số cắt / Bode plot         | `.ac dec 100 1 1Meg` → đọc -3 dB point trên đồ thị magnitude        |

### 4. Lệnh mô phỏng thường dùng

```spice
.tran 0 20m 0 10u           ; transient 20ms, max timestep 10µs
.ac dec 100 1 1Meg          ; AC sweep 1Hz → 1MHz, 100 điểm/decade
.dc V1 -12 12 0.1           ; quét nguồn V1 từ -12V → 12V, bước 0.1V
.op                         ; tính operating point DC
.meas tran Vpp PP V(out)    ; đo peak-to-peak ngõ ra
```

---

## 📝 Ghi chú khi đọc kết quả

- 📂 File `.asc` được LTspice/Windows lưu với mã hóa khác nhau; **nên mở bằng LTspice** thay vì text editor để tránh hỏng ký tự.
- 🔄 Các file `.raw`, `.log`, `.op.raw`, `.db` là **artifact mô phỏng** — tự động tạo lại khi `Run` schematic. Có thể xóa nếu muốn workspace gọn lại.
- ⚙️ Kết quả phụ thuộc vào: macromodel, timestep, tham số nguồn, giá trị linh kiện và các giới hạn không lý tưởng của IC (offset, slew rate, GBW, ngõ ra ZL).
- 🔁 Với **LM339**: ngõ ra open-collector → cần điện trở kéo lên (`R_pull` ~10 kΩ về VCC) khi thiết kế Schmitt/dao động.
- ⏱️ Với **NE555** và mạch tần số cao (> 100 kHz): nên giảm `maximum timestep` xuống ≤ 1 µs để waveform không bị lấy mẫu quá thưa.
- 🎚️ Với **mạch lọc tích cực**: chọn `.ac dec 100 1 1Meg` để đường Bode mượt; tránh `.ac lin` vì phân giải kém ở tần số thấp.

---

## 📖 Tài liệu tham khảo trong repo

| Tài liệu                                       | Nội dung                                                                       |
| ---------------------------------------------- | ------------------------------------------------------------------------------ |
| `Labs Dientu_tuongtu_unlocked.pdf`             | Đề cương + hướng dẫn 8 bài lab (bản unlocked, copy/paste được)                 |
| `LYTHUYET.pdf`                                 | Tóm tắt lý thuyết — op-amp ideal/real, slew rate, GBW, comparator, NE555, LDO, DAC R-2R |
| `Bai 5 Cau 2.pdf` · `Bai 5 Cau 3.pdf`          | Lời giải chi tiết Bài 5 — Schmitt trigger, mạch dao động LM339 / NE555         |
| `LM324 Texas.pdf`                              | Datasheet **Texas Instruments LM324** — quad op-amp, low-power                 |
| `LM339N texas.pdf`                             | Datasheet **Texas Instruments LM339N** — quad comparator, open-collector       |

---

## 📦 Release

- **`v1.0.0`** (2026-05-13) — Initial public lab workspace
  - Đầy đủ schematic LTspice cho 8 bài thực hành
  - Macromodel + symbol LM324 / LM339
  - Mô phỏng output, log, operating point đính kèm
  - Tài liệu hướng dẫn lab, lý thuyết, lời giải Bài 5, datasheet TI

Xem thêm: [RELEASE_NOTES.md](RELEASE_NOTES.md)

---

## 🔗 Liên quan trong portfolio

- 📡 [`TruyenThongSo`](https://github.com/lhlizdabezt/TruyenThongSo) — Truyền thông số (MATLAB) — AWGN, BER, QPSK, LDPC
- 🧠 [`embedded-systems-fpga-review-labs`](https://github.com/lhlizdabezt/embedded-systems-fpga-review-labs) — Hệ thống nhúng FPGA (Quartus, Verilog, Nios II)
- 🩺 [`DoAnDienTuYSinh_STM32_MAX30100_LCD`](https://github.com/lhlizdabezt/DoAnDienTuYSinh_STM32_MAX30100_LCD) — Điện tử y sinh (STM32 + MAX30100)
- 📚 [`HCMUS-DTVT-BaoCao-Templates`](https://github.com/lhlizdabezt/HCMUS-DTVT-BaoCao-Templates) — Mẫu KLTN/BCTT + Typst Guide

---

## ⚖️ Bản quyền &amp; học thuật

Tài liệu PDF, datasheet và schematic được giữ trong repository này để phục vụ **mục đích học tập, đối chiếu mô phỏng và báo cáo môn học** trong khuôn khổ Khoa Điện tử Viễn thông — HCMUS.

- Datasheet **LM324 / LM339**: bản quyền © **Texas Instruments Inc.** — được phân phối miễn phí qua [ti.com](https://www.ti.com/).
- Tài liệu **đề cương lab + lý thuyết**: bản quyền © **Khoa Điện tử Viễn thông — HCMUS** — mirror nội bộ để học viên truy cập nhanh.
- **Schematic LTspice + ghi chú trong README**: © 2026 Lương Hải Long. Không tái sử dụng cho mục đích thương mại hoặc nộp lại như bài thực hành của bạn.

LTspice là phần mềm miễn phí của Analog Devices — không được bundle phần mềm vào repo.

---

<p align="center">
  <sub>📡 HCMUS · FETEL · Bộ môn ĐTVT · Khóa 2022 CLC · Reproducible analog lab workspace</sub>
</p>

<p align="center">
  <i>&ldquo;Từ công thức Kirchhoff đến waveform LTspice — đo được, đối chiếu được, báo cáo được.&rdquo;</i>
</p>
