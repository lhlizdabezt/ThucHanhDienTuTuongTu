# Thuc Hanh Dien Tu Tuong Tu

Workspace thuc hanh Dien tu Tuong tu su dung LTspice de thiet ke, mo phong va doi chieu cac mach op-amp, comparator, dao dong, chinh luu, nguon on ap va chuyen doi tin hieu tuong tu.

![Course](https://img.shields.io/badge/course-Analog%20Electronics-0f766e?style=flat)
![LTspice](https://img.shields.io/badge/tool-LTspice-1d4ed8?style=flat)
![SPICE](https://img.shields.io/badge/simulation-SPICE-7c3aed?style=flat)
![Status](https://img.shields.io/badge/status-lab%20workspace-334155?style=flat)

## Tong Quan

Repository nay tong hop bai thuc hanh Dien tu Tuong tu, gom schematic LTspice, SPICE macromodel, ket qua mo phong va tai lieu tham khao. Noi dung tap trung vao viec quan sat hanh vi mach tuong tu trong mien thoi gian va mien tan so, tu do doi chieu giua cong thuc ly thuyet, tham so linh kien va ket qua mo phong.

Phan workspace phu hop de mo lai tren LTspice, kiem tra mach, chay lai `.tran`, `.ac`, `.dc`, xem waveform va su dung lam minh chung cho bao cao thuc hanh.

## Noi Dung Chinh

| Nhom noi dung | Tep/tap tin | Vai tro |
| --- | --- | --- |
| De cuong va huong dan lab | `Labs Dientu_tuongtu_unlocked.pdf` | Tai lieu huong dan thuc hanh Dien tu Tuong tu, gom cac bai LTspice va mach ung dung. |
| Ly thuyet va cau hoi chuan bi | `LYTHUYET.pdf`, `Bai 5 Cau 2.pdf`, `Bai 5 Cau 3.pdf` | Tong hop giai thich, cong thuc va nhan xet cho cac cau hoi ve slew rate, Schmitt trigger, dao dong LM339/NE555, log/anti-log, LDO va DAC. |
| Datasheet linh kien | `LM324 Texas.pdf`, `LM339N texas.pdf` | Datasheet Texas Instruments cho LM324 quad op-amp va LM339 quad comparator. |
| Thu vien LTspice | `CoHa/LM324.cir`, `CoHa/LM339.cir`, `CoHa/LM324.asy`, `CoHa/LM339.asy` | SPICE macromodel va symbol LTspice dung trong cac mach mo phong. |
| Schematic bai thuc hanh | `CoHa/*.asc` | File mach LTspice tu Bai 1 den Bai 8. |
| Ket qua mo phong | `CoHa/*.raw`, `CoHa/*.log`, `CoHa/*.op.raw`, `CoHa/*.db` | Du lieu waveform, operating point va log sinh ra sau khi chay LTspice. |

## Cau Truc Thu Muc

```text
.
|-- README.md
|-- RELEASE_NOTES.md
|-- Labs Dientu_tuongtu_unlocked.pdf
|-- LYTHUYET.pdf
|-- Bai 5 Cau 2.pdf
|-- Bai 5 Cau 3.pdf
|-- LM324 Texas.pdf
|-- LM339N texas.pdf
`-- CoHa/
    |-- LM324.cir
    |-- LM324.asy
    |-- LM339.cir
    |-- LM339.asy
    |-- BAI 1 CHUAN BI & THUC HANH.asc
    |-- BAI 2 ... BAI 8 *.asc
    |-- *.raw / *.log / *.op.raw / *.db
```

## Tom Tat Cac Bai Mo Phong

| Bai | Chu de ky thuat | Noi dung LTspice tieu bieu |
| --- | --- | --- |
| Bai 1 | Lam quen LTspice va op-amp | Mach LM324, nguon doi xung, tin hieu sin, phan tich `.ac` va `.tran`. |
| Bai 2 | Dap ung op-amp va slew rate | Cac mach khuech dai dung LM324, tin hieu sin/xung, quan sat bien dang do gioi han toc do dap ung. |
| Bai 3 | Mach cong, tru va so sanh | Mach tong hop tin hieu voi LM324, comparator/Schmitt trigger dung LM339, nguong tham chieu va tin hieu vao dang sin/xung. |
| Bai 4 | Mach loc tich cuc | Mang R-C voi LM324, khao sat dap ung tan so bang lenh `.ac`. |
| Bai 5 | Mach dao dong | Dao dong song vuong dung LM339, mach astable NE555, tinh tan so theo R-C va doi chieu sai so mo phong. |
| Bai 6 | Mach phi tuyen | Chinh luu, mach diode/op-amp, bias transistor va cac mach gioi han/khuech dai co hoi tiep. |
| Bai 7 | Nguon va mach ung dung | Mach bom dien tich/tao nguon tham chieu, LDO co op-amp, transistor/MOSFET va mang diode-tu. |
| Bai 8 | Mach chuyen doi tin hieu | Cac mang dien tro dung LM324/LM339 cho xu ly muc dien ap va chuyen doi tuong tu-so don gian. |

## Linh Kien Va Mo Hinh

- `LM324`: op-amp cong suat thap, dung cho cac mach khuech dai, mach loc, chinh luu chinh xac, mach tong/tru va mach dieu khien tuyen tinh.
- `LM339`: comparator 4 kenh ngo ra open-collector, dung cho Schmitt trigger, dao dong song vuong va cac mach so sanh nguong.
- `NE555`: timer o che do astable trong bai dao dong, dung de so sanh voi mach dao dong tao bang comparator.
- Dien tro, tu dien, diode `1N4148`, Schottky diode, BJT `2N3904`, MOSFET `IRF530` va nguon sin/xung de tao dieu kien mo phong.

## Cach Mo Va Chay Lai Mo Phong

1. Cai dat LTspice tren Windows.
2. Mo cac file schematic trong thu muc `CoHa/`.
3. Dam bao cac file `LM324.asy`, `LM339.asy`, `LM324.cir`, `LM339.cir` nam cung workspace hoac duoc LTspice nhan duong dan symbol/model.
4. Kiem tra lenh mo phong trong schematic, vi du `.tran`, `.ac`, `.dc`, `.op`.
5. Chay `Run`, mo waveform viewer va do cac dai luong can bao cao: bien do, tan so, chu ky, pha, nguong chuyen trang thai, slew rate hoac dap ung tan so.

## Ghi Chu Khi Doc Ket Qua

- Mot so file `.asc` duoc luu boi LTspice/Windows voi ma hoa khac nhau; nen mo bang LTspice thay vi sua bang text editor neu khong can thiet.
- Cac file `.raw`, `.log`, `.op.raw` va `.db` la artifact mo phong, co the duoc tao lai khi chay schematic.
- Ket qua mo phong phu thuoc vao macromodel, timestep, tham so nguon, gia tri linh kien va gioi han khong ly tuong cua IC.
- Voi LM339, can luu y ngo ra open-collector va dien tro keo len khi thiet ke mach dao dong hoac so sanh.
- Voi NE555 va cac mach tan so cao, nen giam maximum timestep de waveform khong bi lay mau qua thua.

## GitHub Metadata

**Repository description**

```text
Thuc hanh Dien tu Tuong tu: LTspice lab workspace with LM324, LM339, NE555, op-amp/comparator circuits, active filters, oscillators, rectifiers, LDO and DAC simulations.
```

**Suggested topics**

```text
analog-electronics, ltspice, spice-simulation, op-amp, comparator, lm324, lm339, ne555, active-filter, oscillator, rectifier, ldo, dac, electronics, telecommunications, hcmus
```

## Release

Release dau tien: `v1.0.0` - cong bo day du workspace thuc hanh, README, tai lieu PDF, macromodel va schematic LTspice tu Bai 1 den Bai 8.

## Luu Y Hoc Thuat

Tai lieu PDF va datasheet duoc giu trong repo de phuc vu hoc tap, doi chieu mo phong va bao cao mon hoc. Quyen tac gia cua tai lieu goc thuoc ve don vi/tac gia tuong ung.
