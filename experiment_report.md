# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-2A202600136
**Name:** Nguyen Bang Anh
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

| Scenario | Agent Response | Do chinh xac | Ghi chu |
|----------|----------------|--------------|--------|
| Clean Data - Du lieu sach | Agent: Based on my data, the best choice is Laptop at $1200. | 10/10 | Chinh xac. Agent tim dung san pham electronics gia cao nhat. |
| Garbage Data - Du lieu xau | Agent Error: I'm choking on the data! (reduction operation 'argmax' not allowed for this dtype) | 1/10 | That bai. Du lieu co nhieu loi, agent crash khong tra loi. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Garbage Data voi nhieu van de:

1. Kieu du lieu sai: Price la string "ten dollars" thay vi so, loi argmax
2. ID trung lap: ID=1 xuat hien 2 lan, gay nhiem luan
3. Gia tri rong: Record co ID null va category null
4. Gia tri ngoai le: Nuclear Reactor 999999 dollar, bat thuong
5. Gia am: Ghost Item price = 0, khong hop le

Ket qua: Agent crash hoac toan. Du lieu xau lam AI vo tac dung.

---

## 3. Ket luan

**Co phai du lieu chat luong quan trong hon prompt?** - Co.

Thi nghiem chung to du lieu tot la yeu to then chot cho AI:

- Du lieu xau: Agent crash, khong tra loi, he thong vo dung
- Du lieu sach: Agent tra loi chinh xac, ket qua tin cay

Ket luan: Du lieu sach la nen tang chinh cua AI. Khong the xay dung AI tot tren du lieu xau.
