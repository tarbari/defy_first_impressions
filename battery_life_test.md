# Dygma Defy battery life tests

---

## First test

#### Settings

| Name               | Value |
| ------------------ | ----- |
| Mode               | RF    |
| LED brightness     | 10%   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low   |
| Firmware           | 1.0.0 |

#### Log

| Date       | Time  | Event             | Battery level |
| ---------- | ----- | ----------------- | ------------- |
| 2023-10-08 | 10:00 | On                | 100%          |
| 2023-10-08 | 23:00 | Off               | 2/3 lights\*  |
| 2023-10-09 | 09:00 | On                | 2/3 lights\*  |
| 2023-10-09 | 23:30 | Off               | 1/3 lights\*  |
| 2023-10-10 | 11:00 | On                | 1/3 lights\*  |
| 2023-10-10 | 23:00 | Stopped using\*\* | 35%           |
| 2023-10-11 | 10:00 | On                | 22%           |
| 2023-10-11 | 16:00 | Battery check     | 10%           |

`Total: 45.5 hours`

\* Battery level percentage not available due to bug in Bazecor  
\*\* Forgot to turn keeb off for the night

---

## Second test

#### Settings

| Name               | Value |
| ------------------ | ----- |
| Mode               | RF    |
| LED brightness     | 0%\*  |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low   |
| Firmware           | 1.0.0 |

\*Even when 0% brightness the LEDs did not turn off.  
Turned all LEDs to color black, except for one key on each side to keep track of the layer I'm using.

| Date       | Time  | Event         | Battery level  |
| ---------- | ----- | ------------- | -------------- |
| 2023-10-12 | 14:00 | On            | 100%           |
| 2023-10-12 | 17:00 | Off           | 90%            |
| 2023-10-12 | 20:30 | On            | 90%\*          |
| 2023-10-13 | 01:30 | Off           | 90%            |
| 2023-10-14 | 09:00 | On            | 90%            |
| 2023-10-14 | 11:00 | Off           | 73%            |
| 2023-10-14 | 22:30 | On            | 73%            |
| 2023-10-15 | 02:30 | Off           | 71%            |
| 2023-10-15 | 12:00 | On            | 71%            |
| 2023-10-16 | 01:30 | Off           | 47%            |
| 2023-10-16 | 12:00 | On            | 47%            |
| 2023-10-16 | 18:00 | Off           | 37%            |
| 2023-10-17 | 11:30 | On            | 37%            |
| 2023-10-17 | 16:30 | Off           | 37%\*\*        |
| 2023-10-17 | 20:00 | On            | 37%            |
| 2023-10-18 | 02:00 | Off           | 37%            |
| 2023-10-18 | 13:30 | On            | 37%            |
| 2023-10-19 | 01:00 | Off           | 27%            |
| 2023-10-19 | 10:30 | On            | 27%            |
| 2023-10-19 | 16:00 | Battery check | 17% / 9%\*\*\* |

`Total: 61 hours`

\*After this event I quickly tested reflashing keyboard with Bazecor 1.3.5 and during the about 1 minute battery went back to 100%, but I did not do a force read so this was most probably a wrong reading.  
\*\* Tried re-reading the battery level, but even after powercycle it insisted 37%  
\*\*\* Righ half battery drained more than left.

---

## Third test

```
It seems the battery was not fully charged when I began this test.

Normally I make sure the battery is full by plugging the keyboard in wired,
check battery level in Bazecor, force read battery level and make sure it is
still 100%. After this I close Bazecor, unplug Neuron, make sure the wireless
buttons are off, plug Neuron, start Bazecor, and read the battery levels again.
I might have failed to do that this time.

I'm still leaving this test in
```

#### Settings

| Name               | Value |
| ------------------ | ----- |
| Mode               | BT    |
| LED brightness     | 10%   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low\* |
| Firmware           | 1.1.0 |

\* This should not affect BT connections

| Date       | Time  | Event         | Battery level |
| ---------- | ----- | ------------- | ------------- |
| 2023-10-27 | 16:00 | On            | 100%          |
| 2023-10-27 | 23:30 | Off           | 37%           |
| 2023-10-28 | 12:30 | On            | 37%           |
| 2023-10-29 | 01:30 | Off           | 29% / 36%\*   |
| 2023-10-29 | 17:00 | On            | 29% / 36%\*   |
| 2023-10-29 | 22:00 | Off           | 22% / 29%\*   |
| 2023-10-30 | 09:00 | Battery check | 15% / 29%\*\* |

`Total: 25.5 hours`

\* Left side battery first
\*\* Left side drained during the night?

---

## Fourth test

#### Settings

| Name               | Value |
| ------------------ | ----- |
| Mode               | BT    |
| LED brightness     | 10%   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low\* |
| Firmware           | 1.1.0 |

\* This should not affect BT connections

| Date       | Time  | Event | Battery level  |
| ---------- | ----- | ----- | -------------- |
| 2023-10-30 | 17:00 | On    | 100%           |
| 2023-10-30 | 21:00 | Off   | 100%           |
| 2023-10-31 | 10:00 | On    | 100%           |
| 2023-10-31 | 16:00 | Off   | 90%            |
| 2023-11-01 | 10:00 | On    | 59%\*          |
| 2023-11-01 | 15:00 | Off   | 37% / 47%      |
| 2023-11-01 | 17:30 | On    | 37% / 47%      |
| 2023-11-01 | 21:30 | Off   | 37% / 47%      |
| 2023-11-02 | 16:00 | On    | 37% / 37%      |
| 2023-11-02 | 21:30 | Off   | 37% / 37%      |
| 2023-11-03 | 08:30 | On    | 37% / 37% \*\* |
| 2023-11-03 | 17:00 | Off   | 15% / 27%      |

`Total: 33 hours`

\* The battery seems to drain when neuron is connected to the base,  
 and even if the keyboard is switched off
\*\* Left the neuron attached in the left base again, but no draining occured

---

## Fifth test

#### Settings

| Name               | Value |
| ------------------ | ----- |
| Mode               | BT    |
| LED brightness     | 10%   |
| LED timeout        | Never |
| Layer change pulse | On    |
| RF coverage        | Low\* |
| Firmware           | 1.1.0 |

\* This should not affect BT connections

| Date       | Time  | Event | Battery level |
| ---------- | ----- | ----- | ------------- |
| 2023-11-04 | 11:30 | On    | 100%          |
| 2023-11-05 | 03:00 | Off   | 47%           |
| 2023-11-05 | 12:30 | On    | 47%           |
| 2023-11-05 | 21:30 | Off   | 47%           |
| 2023-11-06 | 08:30 | On    | 47%           |
| 2023-11-06 | 10:30 | Off   | 37%           |
