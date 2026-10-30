# India-Stocks-2431-2460-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2431 to 2460)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2431-2460-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2431 to 2460)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2431 | `TPLPLASTEH` | TPL Plastech Limited | `TPLPLASTEH.NS` |
| 2432 | `TRACXN` | Tracxn Technologies Limited | `TRACXN.NS` |
| 2433 | `TRANSCOR` | Transcorp International Limited | `TRANSCOR.NS` |
| 2434 | `TRANSPEK` | Transpek Industry Limited | `TRANSPEK.NS` |
| 2435 | `TRANSRAILL` | Transrail Lighting Limited | `TRANSRAILL.NS` |
| 2436 | `TRANSWORLD` | TRANSWORLD SHIPPING LINES LIMITED | `TRANSWORLD.NS` |
| 2437 | `TRAVELFOOD` | Travel Food Services Limited | `TRAVELFOOD.NS` |
| 2438 | `TREEHOUSE` | Tree House Education & Accessories Limited | `TREEHOUSE.NS` |
| 2439 | `TREJHARA` | TREJHARA SOLUTIONS LIMITED | `TREJHARA.NS` |
| 2440 | `TREL` | Transindia Real Estate Limited | `TREL.NS` |
| 2441 | `TRF` | TRF Limited | `TRF.NS` |
| 2442 | `TRIGYN` | Trigyn Technologies Limited | `TRIGYN.NS` |
| 2443 | `TRITONV` | Triton Valves Limited | `TRITONV.NS` |
| 2444 | `TRIVENI` | Triveni Engineering & Industries Limited | `TRIVENI.NS` |
| 2445 | `TRIVENIPT` | Triveni Power Transmission Limited | `TRIVENIPT.NS` |
| 2446 | `TRU` | TruCap Finance Limited | `TRU.NS` |
| 2447 | `TRUALT` | TruAlt Bioenergy Limited | `TRUALT.NS` |
| 2448 | `TSFINV` | TSF INVESTMENTS LIMITED | `TSFINV.NS` |
| 2449 | `TTKHLTCARE` | TTK Healthcare Limited | `TTKHLTCARE.NS` |
| 2450 | `TTKPRESTIG` | TTK Prestige Limited | `TTKPRESTIG.NS` |
| 2451 | `TTL` | T T Limited | `TTL.NS` |
| 2452 | `TURTLEMINT` | Turtlemint Fintech Solutions Limited | `TURTLEMINT.NS` |
| 2453 | `TUTIALKA` | Tuticorin Alkali Chemicals & Fertilizers Limited | `TUTIALKA.NS` |
| 2454 | `TVSELECT` | TVS Electronics Limited | `TVSELECT.NS` |
| 2455 | `TVSHLTD` | TVS Holdings Limited | `TVSHLTD.NS` |
| 2456 | `TVSSCS` | TVS Supply Chain Solutions Limited | `TVSSCS.NS` |
| 2457 | `TVSSRICHAK` | TVS Srichakra Limited | `TVSSRICHAK.NS` |
| 2458 | `TVTODAY` | TV Today Network Limited | `TVTODAY.NS` |
| 2459 | `TVVISION` | TV Vision Limited | `TVVISION.NS` |
| 2460 | `UCAL` | UCAL LIMITED | `UCAL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream TPLPLASTEH 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2431-2460-Historical-Data/main/TPLPLASTEH/1m/2026/10/TPLPLASTEH_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
