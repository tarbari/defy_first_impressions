# Battery life tests

---

## First test
#### Settings
| Name               | Value |
|--------------------|-------|
| LED brightness     | 5%    |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low   |

#### Log
| Date       | Time  | Event | Battery level |
|------------|-------|-------|---------------|
| 2023-10-08 | 10:00 | On    | 100%          |
| 2023-10-08 | 23:00 | Off   | 2/3 lights*   |
| 2023-10-09 | 09:00 | On    | 2/3 lights*   |
| 2023-10-09 | 23:30 | Off   | 1/3 lights*   |

\* Battery level percentage not available due to bug in Bazecor
