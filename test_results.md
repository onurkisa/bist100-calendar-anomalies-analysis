
# Test Results

## 1. Sample Sizes

### 1.1 Weekday groups

| Day       |   N |
| --------- | --: |
| Monday    | 535 |
| Tuesday   | 533 |
| Wednesday | 538 |
| Thursday  | 537 |
| Friday    | 533 |

### 1.2 Monthly groups

| Month     |  N |
| --------- | -: |
| January   | 11 |
| February  | 11 |
| March     | 11 |
| April     | 11 |
| May       | 11 |
| June      | 11 |
| July      | 11 |
| August    | 11 |
| September | 11 |
| October   | 10 |
| November  | 10 |
| December  | 10 |

---

## 2. Daily Continuous Returns — Assumption Checks

### 2.1 Shapiro-Wilk normality by weekday

| Day       |              Statistic |                    p-value | Decision at α = 0.05 |
| --------- | ---------------------: | -------------------------: | -------------------- |
| Friday    | **0.9313438929141539** |  **6.644562581272388e-15** | **Reject normality** |
| Monday    | **0.9545392727694750** |  **8.891068188497565e-12** | **Reject normality** |
| Tuesday   | **0.9509448782078790** | **2.6492673637911814e-12** | **Reject normality** |
| Wednesday | **0.9291176454257217** |  **2.89961267775567e-15** | **Reject normality** |
| Thursday  | **0.9405936878452577** |  **8.057565744284932e-14** | **Reject normality** |

### 2.2 Levene’s test for homogeneity of variances across weekdays

|            Statistic |                    p-value | Decision at α = 0.05   |
| -------------------: | -------------------------: | ---------------------- |
| **8.17707716604066** | **1.4964250282387501e-06** | **Reject homogeneity** |

---

## 3. Daily Continuous Returns — Omnibus Test

### 3.1 Welch’s ANOVA across weekdays

| Source | ddof1 |         ddof2 |            F |            p-unc |     np2 |
| ------ | --: | ----------: | -----------: | -----------: | -----: |
| Day    |   4 | 1332.671539 | **3.266379** | **0.011219** |   0.004837 |


**Decision:** **Reject H0** at α = 0.05. At least one weekday mean differs.

---

## 4. Daily Continuous Returns — Post hoc Tests under unequal variances

### 4.1 Games-Howell pairwise comparisons

| A            | B             |      p-value | Significant (α = 0.05) |
| ------------ | ------------- | -----------: | :--------------------- |
| Friday       | Monday        | 0.7613843463 | No                     |
| Friday       | Thursday      | 0.3494153027 | No                     |
| Friday       | Tuesday       | 0.9941253788 | No                     |
| Friday       | Wednesday     | 0.5198947141 | No                     |
| Monday       | Thursday      | 0.9916044483 | No                     |
| Monday       | Tuesday       | 0.5664562545 | No                     |
| Monday       | Wednesday     | 0.0920623841 | No                     |
| Thursday     | Tuesday       | 0.1979482776 | No                     |
| **Thursday** | **Wednesday** | **0.009568** | **Yes**                |
| Tuesday      | Wednesday     | 0.8055693746 | No                     |

### 4.2 Tamhane’s T2 pairwise comparisons

| A             | B            |      p-value | Significant (α = 0.05) |
| ------------- | ------------ | -----------: | :--------------------- |
| Friday        | Monday       | 0.7417934090 | No                     |
| Friday        | Tuesday      | 0.9967807622 | No                     |
| Friday        | Wednesday    | 0.4654272605 | No                     |
| Friday        | Thursday     | 0.2878051393 | No                     |
| Monday        | Tuesday      | 0.5169098212 | No                     |
| Monday        | Wednesday    | 0.0618185666 | No                     |
| Monday        | Thursday     | 0.9950106424 | No                     |
| Tuesday       | Wednesday    | 0.7937400960 | No                     |
| Tuesday       | Thursday     | 0.1474436273 | No                     |
| **Wednesday** | **Thursday** | **0.005418** | **Yes**                |

**Consistency:** **Both procedures identify the same single significant contrast: Thursday vs Wednesday.**

---

## 5. Daily Continuous Returns — Descriptive Means

Average daily continuous returns by weekday (percent):

| Day       |  Mean (%) |
| --------- | --------: |
| Monday    |  0.191993 |
| Tuesday   |  0.036031 |
| Wednesday | -0.066661 |
| Thursday  |  0.238877 |
| Friday    |  0.072848 |

---

## 6. Monthly Continuous Returns — Assumption Checks

### 6.1 Shapiro-Wilk normality by month

| Month     |              Statistic |          p-value | Decision at α = 0.05    |
| --------- | ---------------------: | ---------------: | ----------------------- |
| January   |     0.9291262215179441 |     0.4393528575 | Do not reject normality |
| February  |     0.9755803417739833 |     0.9366505256 | Do not reject normality |
| March     |     0.9766103821353486 |     0.9443931671 | Do not reject normality |
| April     |     0.9691363632414517 |     0.8776790854 | Do not reject normality |
| May       |     0.9225619376377341 |     0.3405589532 | Do not reject normality |
| June      |     0.9364809372860026 |     0.4800519779 | Do not reject normality |
| **July**  | **0.8423023388138726** | **0.0338518129** | **Reject normality**    |
| August    |     0.8970642934507972 |     0.1701499609 | Do not reject normality |
| September |     0.9298794813970238 |     0.4096356164 | Do not reject normality |
| October   |     0.9004958608073300 |     0.2218582534 | Do not reject normality |
| November  |     0.9191337814825234 |     0.3497869350 | Do not reject normality |
| December  |     0.9364806840502906 |     0.5145576068 | Do not reject normality |

### 6.2 Levene’s test for homogeneity of variances across months

|         Statistic |     p-value | Decision at α = 0.05      |
| ----------------: | ----------: | ------------------------- |
| 1.087209484541159 | 0.377621712 | Do not reject homogeneity |

---

## 7. Monthly Continuous Returns — Omnibus Test

### 7.1 One-way ANOVA across months

| Source |  ddof1| ddof2|    F |        p-unc | np2 | Decision at α = 0.05 |
| ------ | -----: | -----: |-----: |-------: | -------: | -------------------- |
| Month  | 11 | 116| 1.1105 | 0.359359 | 0.095275 | Do not reject H0     |


---

## 8. Monthly Continuous Returns — Descriptive Means

Average monthly continuous returns by month (percent):

| Month     |  Mean (%) |
| --------- | --------: |
| January   |  4.486714 |
| February  | -0.577258 |
| March     | -2.255233 |
| April     |  2.222791 |
| May       |  0.265743 |
| June      |  2.820928 |
| July      |  4.102846 |
| August    |  1.340776 |
| September |  0.776913 |
| October   |  0.786794 |
| November  |  6.488440 |
| December  |  3.579793 |

---

**Notes:** All decisions use two-sided tests at α = 0.05. Figures referenced in the main report are not reproduced here.
