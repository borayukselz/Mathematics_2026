# Exercise 14: Rotation Matrices

### Given Matrix Definition

**General Rotation Matrix R(θ):**
[  cos(θ)  -sin(θ) ]
[  sin(θ)   cos(θ) ][cite: 16]

**Rotation Matrix R(α):**
[  cos(α)  -sin(α) ]
[  sin(α)   cos(α) ][cite: 16]

**Rotation Matrix R(β):**
[  cos(β)  -sin(β) ]
[  sin(β)   cos(β) ][cite: 16]

---

### 1. Trigonometric Angle-Sum Identities

To prove the matrix relationship, we use the standard trigonometric sum formulas[cite: 16]:
1. **Cosine Sum Formula:** cos(α + β) = cos(α)cos(β) - sin(α)sin(β)[cite: 16]
2. **Sine Sum Formula:** sin(α + β) = sin(α)cos(β) + cos(α)sin(β)[cite: 16]

---

### 2. Compute Matrix Product R(α)R(β)

* **Step-by-Step Multiplication:**
  Multiply Row i of R(α) by Column j of R(β)[cite: 16]:

  * **Top-Left Entry (1,1):**
    (Row 1 of R(α) × Column 1 of R(β))
    = cos(α)cos(β) + (-sin(α))sin(β)
    = **cos(α)cos(β) - sin(α)sin(β)**

  * **Top-Right Entry (1,2):**
    (Row 1 of R(α) × Column 2 of R(β))
    = cos(α)(-sin(β)) + (-sin(α))cos(β)
    = -cos(α)sin(β) - sin(α)cos(β)
    = **-(sin(α)cos(β) + cos(α)sin(β))**

  * **Bottom-Left Entry (2,1):**
    (Row 2 of R(α) × Column 1 of R(β))
    = sin(α)cos(β) + cos(α)sin(β)
    = **sin(α)cos(β) + cos(α)sin(β)**

  * **Bottom-Right Entry (2,2):**
    (Row 2 of R(α) × Column 2 of R(β))
    = sin(α)(-sin(β))
