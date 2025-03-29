---
layout: default
title: أول مقالة
---

# AtCoder DP Editorial - شرح

**الكاتب:** Neo Wang | **تاريخ:** April 22, 2021

---

## مقدمة

المقالة دي بتشرح مسائل AtCoder DP Contest باستخدام الديناميك بروجرامينج.

## A - Frog 1 🐸

**Time Complexity:** $\mathcal{O}(N)$

نستخدم `dp[i]` لحساب أقل تكلفة للوصول للحجر `i`.

```cpp
dp[i+1] = min(dp[i+1], dp[i] + abs(A[i] - A[i+1]));
