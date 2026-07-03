# Total Variation (TV) Regularization

Details TV regularization as a spatial smoothing and high-frequency noise filter.

---

## Architecture Diagram

```mermaid
flowchart LR
    Pixel[Pixel Grid] --> DiffX[Horizontal Deltas]
    Pixel --> DiffY[Vertical Deltas]
    DiffX & DiffY --> Sum[L1 / L2 Summation]
    Sum --> TV[TV Loss]
```

---

## Detailed Explanation

### Overview
Total Variation (TV) regularization is a classic smoothing constraint that penalizes rapid, high-frequency pixel variations to prevent noise.

### Key Mechanics
- Measures differences between adjacent pixels.
- Acts as a low-pass filter to reduce checkerboard and grid artifacts.

### Pros & Cons
- **Pros:** Reduces noise and artifacts, enforces local spatial consistency.
- **Cons:** Can over-smooth real textures, making details look plasticky if over-penalized.

---

[← Back to README](../README.md)
