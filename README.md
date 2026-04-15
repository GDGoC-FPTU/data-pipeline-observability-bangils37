[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574028&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** 26ai.anhnb@vinuni.edu.vn
**Name:** Nguyen Bang Anh

---

## Mo ta

Thí nghiệm ETL Pipeline để biết ảnh hướng của dữ liệu đến chất lượng của AI Agent.

Các bước:
1. Extract: Đọc file JSON
2. Validate: Kiểm tra dữ liệu
3. Transform: Chuẩn hóa và tính toán
4. Load: Lưu CSV
5. Test: So sánh Agent với dữ liệu sạch vs dữ liệu xấu

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
python .\generate_garbage.py    
python .\agent_simulation.py   
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Ket qua ETL Pipeline:

- Dau vao: 5 record tu raw_data.json
- Hop le: 3 record
- Loai bo: 2 record (ID=3 gia am, ID=4 khong category)

Du lieu sau xu ly:
  1. Laptop 1200 dollar giam 10% = 1080 dollar
  2. Chair 45 dollar giam 10% = 40.50 dollar
  3. Monitor 300 dollar giam 10% = 270 dollar

Test Agent:
  - Du lieu sach: Agent tra loi chinh xac - Laptop 1200 dollar la toc nhat
  - Du lieu xau: Agent crash - khong the xu ly string price

Ket luan: Du lieu chat luong anh huong lon toi AI. Du lieu xau lam AI xau.
