# EXERCISE 3
# WHEN CAN MATRICES BE MULTIPLIED?

---

## 1. GIVEN

The dimensions of the matrices are:

| Matrix | Dimensions |
|:------:|:----------:|
| A | **2 × 3** |
| B | **3 × 4** |
| C | **4 × 2** |
| D | **2 × 2** |

---

## 2. MULTIPLICATION RULE

Two matrices can be multiplied only if:

**Columns of the first matrix = Rows of the second matrix.**

General rule:

**(m × n) · (n × p) = (m × p)**

The inner dimensions must be equal.

---

## 3. SOLUTIONS

### 3.1. Product AB

- Matrix A: **2 × 3**
- Matrix B: **3 × 4**
- Compatibility: **3 = 3**

**RESULT: DEFINED**

Resulting matrix size: **2 × 4**

---

### 3.2. Product BA

- Matrix B: **3 × 4**
- Matrix A: **2 × 3**
- Compatibility: **4 ≠ 2**

**RESULT: NOT DEFINED**

The inner dimensions are different.

---

### 3.3. Product BC

- Matrix B: **3 × 4**
- Matrix C: **4 × 2**
- Compatibility: **4 = 4**

**RESULT: DEFINED**

Resulting matrix size: **3 × 2**

---

### 3.4. Product CB

- Matrix C: **4 × 2**
- Matrix B: **3 × 4**
- Compatibility: **2 ≠ 3**

**RESULT: NOT DEFINED**

The inner dimensions are different.

---

### 3.5. Product AC

- Matrix A: **2 × 3**
- Matrix C: **4 × 2**
- Compatibility: **3 ≠ 4**

**RESULT: NOT DEFINED**

The inner dimensions are different.

---

### 3.6. Product CA

- Matrix C: **4 × 2**
- Matrix A: **2 × 3**
- Compatibility: **2 = 2**

**RESULT: DEFINED**

Resulting matrix size: **4 × 3**

---

### 3.7. Product AD

- Matrix A: **2 × 3**
- Matrix D: **2 × 2**
- Compatibility: **3 ≠ 2**

**RESULT: NOT DEFINED**

The inner dimensions are different.

---

### 3.8. Product DA

- Matrix D: **2 × 2**
- Matrix A: **2 × 3**
- Compatibility: **2 = 2**

**RESULT: DEFINED**

Resulting matrix size: **2 × 3**

---

## 4. FINAL SUMMARY

| Product | Compatibility | Result | Size |
|:-------:|:-------------:|:------:|:----:|
| AB | 3 = 3 | Defined | 2 × 4 |
| BA | 4 ≠ 2 | Not defined | — |
| BC | 4 = 4 | Defined | 3 × 2 |
| CB | 2 ≠ 3 | Not defined | — |
| AC | 3 ≠ 4 | Not defined | — |
| CA | 2 = 2 | Defined | 4 × 3 |
| AD | 3 ≠ 2 | Not defined | — |
| DA | 2 = 2 | Defined | 2 × 3 |

---

## 5. CONCLUSION

Matrix multiplication depends on the compatibility of dimensions.

The number of columns in the first matrix must equal the number of rows in the second matrix.

The order of multiplication matters because changing the order can make a product undefined or produce a different matrix size.
