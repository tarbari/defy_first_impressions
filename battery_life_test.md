# Dygma Defy battery life tests

---

## First test
#### Settings
| Name               | Value |
|--------------------|-------|
| Mode               | RF    |
| LED brightness     | 10%   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low   |

#### Log
| Date       | Time  | Event           | Battery level |
|------------|-------|-----------------|---------------|
| 2023-10-08 | 10:00 | On              | 100%          |
| 2023-10-08 | 23:00 | Off             | 2/3 lights*   |
| 2023-10-09 | 09:00 | On              | 2/3 lights*   |
| 2023-10-09 | 23:30 | Off             | 1/3 lights*   |
| 2023-10-10 | 11:00 | On              | 1/3 lights*   |
| 2023-10-10 | 23:00 | Stopped using** | 35%           |
| 2023-10-11 | 10:00 | On              | 22%           |
| 2023-10-11 | 16:00 | Battery check   | 10%           |

\* Battery level percentage not available due to bug in Bazecor
\** Forgot to turn keeb off for the night

---

## Second test
#### Settings
| Name               | Value |
|--------------------|-------|
| Mode               | RF    |
| LED brightness     | 0%*   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low   |

\*Even when 0% brightness the LEDs did not turn off. 
Turned all LEDs to color black, except for one key on each side to keep track of the layer I'm using.


| Date       | Time  | Event           | Battery level |
|------------|-------|-----------------|---------------|
| 2023-10-12 | 14:00 | On              | 100%          |
