# RW-MPJPE Weights

---

## 📑 Contents

1. [Background](#background)  
2. [Definition](#definition)  
3. [Weight Table](#weight-table)  
4. [Usage](#usage)  

---

## 🧾 Background

Standard **MPJPE (Mean Per Joint Position Error)** treats all joints equally.  
However, in clinical in-bed monitoring, **pressure ulcers** vary across body parts.  
Therefore, we propose **RW-MPJPE (Risk-Weighted MPJPE)**, incorporating **nurse-assigned weights** to reflect clinical importance.

---

## 📐 Definition

RW-MPJPE is defined as:

$$
\text{RW-MPJPE} = \frac{\sum_{i=1}^N w_i \cdot d_i}{\sum_{i=1}^N w_i}
$$

Where:
- $d_i$ = per-joint position error (mm)  
- $w_i$ = weight assigned by ICU nurse experts  
- $N$ = total number of joints  

---

## 📊 Weight Table

| ID  | Joint Name        | Weight |
|----:|-------------------|-------:|
|  0 | Pelvis             | 10     |
|  1 | Left Hip           | 5      |
|  2 | Right Hip          | 5      |
|  3 | Lumbar 1 (Lower)   | 1      |
|  4 | Left Knee          | 2      |
|  5 | Right Knee         | 2      |
|  6 | Lumbar 2 (Middle)  | 1      |
|  7 | Left Ankle         | 4      |
|  8 | Right Ankle        | 4      |
|  9 | Thoracic (Upper)   | 1      |
| 10 | Left Forefoot/Toe  | 0.5    |
| 11 | Right Forefoot/Toe | 0.5    |
| 12 | Neck               | 1      |
| 13 | Left Clavicle      | 0.5    |
| 14 | Right Clavicle     | 0.5    |
| 15 | Head               | 3      |
| 16 | Left Shoulder      | 0.5    |
| 17 | Right Shoulder     | 0.5    |
| 18 | Left Elbow         | 0.5    |
| 19 | Right Elbow        | 0.5    |
| 20 | Left Wrist         | 1      |
| 21 | Right Wrist        | 1      |
| 22 | Left Hand (Palm)   | 2      |
| 23 | Right Hand (Palm)  | 2      |

---

## ⚙️ Usage

- Apply the weight table above to compute RW-MPJPE.  
- Useful for experiments requiring **clinical relevance** in joint-level accuracy.  

---
