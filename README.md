### Renewable energy data analytics

[**Interactive Portfolio**](https://kwwaleszczynski-del.github.io/) · [**LinkedIn**](https://www.linkedin.com/in/kw00)

Analytics for solar, wind and battery assets: performance verification, fault detection, power market analysis and dashboards. Every project below is written from scratch on open data or on a disclosed synthetic plant and can be rerun from its repository, with tests and CI.

#### Start here

Six projects to look at first. The first three come with a short case study written for asset owners: the problem, the data, the numbers and what they mean for a decision.

- **[PV budget bridge: monthly P50 to actual waterfall and sensor QC](https://github.com/kwwaleszczynski-del/pv-budget-bridge)** · [case study](https://kwwaleszczynski-del.github.io/case-studies/pv-budget-bridge.html) · [live page](https://kwwaleszczynski-del.github.io/pv-budget-bridge/)  
  Splits every month's gap to the P50 budget into kWh by cause (weather, availability, curtailment, soiling, snow, data gaps) and checks the irradiance sensor first; outage and curtailment losses come back within 0.5 % of a known truth.
- **[Wind turbine downtime, causes and availability](https://github.com/kwwaleszczynski-del/wind-downtime-availability)** · [case study](https://kwwaleszczynski-del.github.io/case-studies/wind-downtime-availability.html) · [live page](https://kwwaleszczynski-del.github.io/wind-downtime-availability/)  
  Shows that the category a stop is booked under moves warranty availability more than detecting the stop does: grid and curtailment stops booked as turbine faults turn 97.9 % into 93.5 % for one open farm-year.
- **[Grid battery operations against warranty and LTSA](https://github.com/kwwaleszczynski-del/bess-ops-warranty)** · [case study](https://kwwaleszczynski-del.github.io/case-studies/bess-ops-warranty.html) · [live page](https://kwwaleszczynski-del.github.io/bess-ops-warranty/)  
  Checks round-trip efficiency, availability, cycles and capacity tests against warranty and LTSA terms, and shows why the metering point matters: 55 Australian grid batteries convert at about 0.92 but deliver 0.82 at the meter.
- **[Kelmarsh wind farm in a laptop-GPU LES](https://github.com/kwwaleszczynski-del/wind-les-gpu)** · [live page](https://kwwaleszczynski-del.github.io/wind-les-gpu/)  
  A second opinion on the wake loss in a yield assessment: a home-made LES on a laptop GPU, with no tuned wake parameter, gives 9.8 % against 9.2 % measured in six years of SCADA.
- **[res-asset-kpi: KPI library for PV, wind and BESS](https://github.com/kwwaleszczynski-del/res-asset-kpi)** · [docs](https://kwwaleszczynski-del.github.io/res-asset-kpi/)  
  The monthly indicators of PV, wind and battery assets (PR, contract availability, budget bridge, RTE, cycles, capacity tests) as one tested library on PyPI with a DOI, so a report can be reproduced and audited.
- **[A citable forecast benchmark for the Polish grid](https://github.com/kwwaleszczynski-del/pl-forecast-bench)** · [live page](https://kwwaleszczynski-del.github.io/pl-forecast-bench/)  
  Before paying for a forecast, compare it with the free PSE plan under the same as-of rule: intraday models beat the plan by 20-26 %, but day-ahead nothing that respects the 10:00 issue time beats it for volumes.

#### All 46 projects

Grouped by topic; click a group to open it. Every card links to the repository and, where there is one, to its live page. The same list with filters is on the [interactive portfolio](https://kwwaleszczynski-del.github.io/).

<details>
<summary><b>Solar PV</b> · 7 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-budget-bridge"><img src="https://kwwaleszczynski-del.github.io/img/pv-budget-bridge.webp" alt="PV budget bridge: monthly P50 to actual waterfall and sensor QC"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-budget-bridge">PV budget bridge: monthly P50 to actual waterfall and sensor QC</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-budget-bridge/">live page</a><br><sub>Recovers injected outages and curtailment within 0.5 % on synthetic truth and flags clock shifts, sensor tilt errors and pyranometer drift across three multi-year NREL PVDAQ rooftops.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-shade-fingerprint"><img src="https://kwwaleszczynski-del.github.io/img/pv-shade-fingerprint.webp" alt="PV shading from AC power alone"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-shade-fingerprint">PV shading from AC power alone</a></b><br><sub>A building's silhouette recovered with mask IoU 0.93 and 0.8 deg RMSE on simulated systems, then run on two years of a real PVDAQ roof.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-tracker-shading-3d"><img src="https://kwwaleszczynski-del.github.io/img/pv-tracker-shading-3d.webp" alt="Single-axis trackers in 3D"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-tracker-shading-3d">Single-axis trackers in 3D</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-tracker-shading-3d/">live page</a><br><sub>Backtracking gives +4.3 % DC yield over true tracking on flat ground (1255 vs 1204 kWh/kWp).</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-outage-classifier"><img src="https://kwwaleszczynski-del.github.io/img/pv-outage-classifier.webp" alt="PV outages: detection, cause and availability"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-outage-classifier">PV outages: detection, cause and availability</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-outage-classifier/">live page</a><br><sub>Requiring events of at least 1 h lifts the hybrid detector's event precision from 0.14 to 0.74 and cuts false alarms from 2.9 to 0.13 per device-year; thresholds tuned on simulation give 257 alarms per inverter-year on real roofs, a short site set-up brings it to 6 with all real outages still found.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-thermal-check"><img src="https://kwwaleszczynski-del.github.io/img/pv-thermal-check.webp" alt="PV thermal check: modules, inverter, transformer"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-thermal-check">PV thermal check: modules, inverter, transformer</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-thermal-check/">live page</a><br><sub>The back-of-module sensor saw only about half of the real heating: thermal losses are 10.5 % a year, not 6.7 %; temperature-corrected PR cuts the seasonal spread from 13.1 to 4.8 pp.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-string-iv-faults"><img src="https://kwwaleszczynski-del.github.io/img/pv-string-iv-faults.webp" alt="PV string fault diagnosis from inverter MPPT voltage and current"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-string-iv-faults">PV string fault diagnosis from inverter MPPT voltage and current</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-string-iv-faults/">live page</a><br><sub>Held-out macro-F1 is 0.694 with 7 % false alarms on healthy windows: shorted diodes are counted exactly in 97.9 % of detected cases and series resistance is estimated within about 10 %, but 1 % soiling stays hidden in string-to-string mismatch (F1 0.25).</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-canopy-pac-verification"><img src="https://kwwaleszczynski-del.github.io/img/pv-canopy-pac-verification.webp" alt="Off-site canopy vs row-to-row shading in an autumn IEC 61724-1 PV acceptance test"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-canopy-pac-verification">Off-site canopy vs row-to-row shading in an autumn IEC 61724-1 PV acceptance test</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-canopy-pac-verification/">live page</a><br><sub>Row-to-row shading under flat-terrain backtracking, not the forest, drives the shortfall (2.05 pp vs 0.18 pp; estimated 1.78 and 0.22). Excluding canopy-shaded intervals turns a failed PAC into a pass, and the raycaster matches SCADA dropouts at interval F1 0.82 but only R² 0.12.</sub></td>
<td width="50%"></td>
</tr>
</table>
</details>

<details>
<summary><b>Wind</b> · 8 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-les-gpu"><img src="https://kwwaleszczynski-del.github.io/img/wind-les-gpu.webp" alt="Kelmarsh wind farm in a laptop-GPU LES"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-les-gpu">Kelmarsh wind farm in a laptop-GPU LES</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-les-gpu/">live page</a><br><sub>With no parameter fitted to the measured losses the LES predicts 9.79 % farm wake loss against 9.24 % measured in 159,289 SCADA records (sector RMSE 2.2 pp vs 2.6 pp for PyWake Gaussian) in 81 s per wind direction on a 6 GB laptop GPU.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-bayes-twin"><img src="https://kwwaleszczynski-del.github.io/img/wind-bayes-twin.webp" alt="A Bayesian digital twin of a wind farm"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-bayes-twin">A Bayesian digital twin of a wind farm</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-bayes-twin/">live page</a><br><sub>On 624 injected faults it names the right cause in 95 % of detections against 72 % for CUSUM and NBM charts, with 0.50 false alarms per turbine-year against 2.08.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-downtime-availability"><img src="https://kwwaleszczynski-del.github.io/img/wind-downtime-availability.webp" alt="Wind turbine downtime, causes and availability"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-downtime-availability">Wind turbine downtime, causes and availability</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-downtime-availability/">live page</a><br><sub>The pitch / rotor-speed signature finds stops with F1 0.80-0.91 without training, while the usual "power ≤ 0" rule raises 4,833 alarms for 1,412 logged stops; booking grid and curtailment stops as turbine faults cuts warranty availability from 97.9 % to 93.5 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-om-reliability"><img src="https://kwwaleszczynski-del.github.io/img/wind-om-reliability.webp" alt="Wind turbine O&amp;M reliability from status and alarm logs"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-om-reliability">Wind turbine O&amp;M reliability from status and alarm logs</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-om-reliability/">live page</a><br><sub>7 of 69 codes cause 80 % of Kelmarsh stop hours; 43 % of Penmanshiel failures repeat the same code within 7 days of restart (3.5 % by chance), and Crow-AMSAA separates improving fleets (Kelmarsh beta 0.82) from deteriorating ones (Penmanshiel beta 1.12).</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-wake-aware-verification"><img src="https://kwwaleszczynski-del.github.io/img/wind-wake-aware-verification.webp" alt="WARP: wake-aware turbine verification"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-wake-aware-verification">WARP: wake-aware turbine verification</a></b><br><sub>On 288 faults injected into 2019-2020 data it finds a 3 % anemometer bias in 83 % of cases and a derating to 95 % of rated power in 94 %, where the neighbour index finds 4 %; yaw faults are found every time, partly by construction.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-thermal-nbm"><img src="https://kwwaleszczynski-del.github.io/img/wind-thermal-nbm.webp" alt="Drivetrain temperatures: early fault detection"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-thermal-nbm">Drivetrain temperatures: early fault detection</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-thermal-nbm/">live page</a><br><sub>A +5 °C drift is caught in 97-99 % of cases within about 20 days by every method; on CARE the temperature-only models are precise but miss faults no thermometer can see.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-power-curve-kelmarsh"><img src="https://kwwaleszczynski-del.github.io/img/wind-power-curve-kelmarsh.webp" alt="Wind power curves (IEC 61400-12-1)"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-power-curve-kelmarsh">Wind power curves (IEC 61400-12-1)</a></b><br><sub>Caught a silent change of the SCADA wind speed definition that made the turbines look up to 14 % better than they were.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-wake-shadow"><img src="https://kwwaleszczynski-del.github.io/img/wind-wake-shadow.webp" alt="Wakes and shadow flicker"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-wake-shadow">Wakes and shadow flicker</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-wake-shadow/">live page</a><br><sub>The worst case exceeds 30 h/year on 2.4 km² up to 860 m from the nearest turbine; sunshine, operation and rotor orientation bring the expected hours to 20 % of that.</sub></td>
</tr>
</table>
</details>

<details>
<summary><b>Biogas</b> · 3 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-biogas-siting"><img src="https://kwwaleszczynski-del.github.io/img/pl-biogas-siting.webp" alt="Untapped biogas potential in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-biogas-siting">Untapped biogas potential in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-biogas-siting/">live page</a><br><sub>About 2.2 billion m³ of methane a year sits in farm residues and existing plants digest about 1.4 % of the manure; of 816 MWe within reach of published grid nodes only 473 MWe fits their free capacity.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-biogas-flex"><img src="https://kwwaleszczynski-del.github.io/img/pl-biogas-flex.webp" alt="What is a flexible biogas plant worth?"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-biogas-flex">What is a flexible biogas plant worth?</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-biogas-flex/">live page</a><br><sub>Twice the engine capacity and 12 h of gas storage add about 360 thousand PLN a year on a forecast alone (86 % of perfect foresight); with only 2 h of storage the extra engines earn less than a third of that.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/biogas-digester-twin"><img src="https://kwwaleszczynski-del.github.io/img/biogas-digester-twin.webp" alt="Which method catches a sick digester first?"></a><br><b><a href="https://github.com/kwwaleszczynski-del/biogas-digester-twin">Which method catches a sick digester first?</a></b> · <a href="https://kwwaleszczynski-del.github.io/biogas-digester-twin/">live page</a><br><sub>Twice-weekly FOS/TAC warns before the yield loss in 1 % of upsets; PCA on online signals does it in 75 % with 0.7 false alarms a year, and the EKF twin names all 20 CH4 analyser drifts as instrument faults without any failure examples.</sub></td>
<td width="50%"></td>
</tr>
</table>
</details>

<details>
<summary><b>Storage &amp; markets</b> · 13 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-power-market-live"><img src="https://kwwaleszczynski-del.github.io/pl-power-market-live/thumb.webp" alt="Polish power market, live"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-power-market-live">Polish power market, live</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-power-market-live/">live page</a><br><sub>No server and no database: GitHub Actions rebuilds a static page from cached monthly Parquet files.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-capture-price"><img src="https://kwwaleszczynski-del.github.io/img/pl-capture-price.webp" alt="How solar eats its own price in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-capture-price">How solar eats its own price in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-capture-price/">live page</a><br><sub>In 2025 PV captured 64 % of the average price and wind 94 %; every 10 pp of PV share costs PV about 0.20 of value factor.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-bess-revenue-stack"><img src="https://kwwaleszczynski-del.github.io/img/pl-bess-revenue-stack.webp" alt="Battery revenue stacking in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-bess-revenue-stack">Battery revenue stacking in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-bess-revenue-stack/">live page</a><br><sub>Over the last 12 months a 2-hour battery could stack about 3.3 m PLN/MW against 0.38 m from arbitrage alone, but a fleet of 1 GW cuts that by about 70 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-bess-paper-trading"><img src="https://kwwaleszczynski-del.github.io/img/pl-bess-paper-trading.webp" alt="Battery paper trading, live track record"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-bess-paper-trading">Battery paper trading, live track record</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-bess-paper-trading/">live page</a><br><sub>Backtest since June 2024: forecast + MILP earns 83 % of perfect foresight (324 k PLN/MW/yr), but a plain 7-day price average does as well; live record from 28 Oct 2026.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-bess-saturation"><img src="https://kwwaleszczynski-del.github.io/img/pl-bess-saturation.webp" alt="When batteries flatten their own spreads"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-bess-saturation">When batteries flatten their own spreads</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-bess-saturation/">live page</a><br><sub>At 2025 prices a 2-hour battery earns 308 k PLN/MW alone, 203 k at 2 GW of fleet and 72 k at 10 GW; the marginal value of the fleet turns negative near 10 GW.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/cable-pooling-sizer"><img src="https://kwwaleszczynski-del.github.io/img/cable-pooling-sizer.webp" alt="Cable pooling: PV, wind and storage behind one connection"></a><br><b><a href="https://github.com/kwwaleszczynski-del/cable-pooling-sizer">Cable pooling: PV, wind and storage behind one connection</a></b> · <a href="https://kwwaleszczynski-del.github.io/cable-pooling-sizer/">live page</a><br><sub>Best oversizing is 1.75-2.5x the connection without a battery and 2.25-3.25x with one; accepting 8-18 % curtailment is optimal, and for PV-heavy plants most of it falls in negative-price hours.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/nem-battery-behaviour"><img src="https://kwwaleszczynski-del.github.io/img/nem-battery-behaviour.webp" alt="How real batteries trade"></a><br><b><a href="https://github.com/kwwaleszczynski-del/nem-battery-behaviour">How real batteries trade</a></b><br><sub>The six largest batteries earn 11-51 % of their perfect-foresight optimum; the gap is split into capacity offered, volume and timing.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-soc-soh-degradation"><img src="https://kwwaleszczynski-del.github.io/img/bess-soc-soh-degradation.webp" alt="Battery state of charge and ageing"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-soc-soh-degradation">Battery state of charge and ageing</a></b><br><sub>SoC from 5-minute market data tracks the operator's SoC within 2.7-3.8 percentage points (RMSE).</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-ops-warranty"><img src="https://kwwaleszczynski-del.github.io/img/bess-ops-warranty.webp" alt="Grid battery operations against warranty and LTSA"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-ops-warranty">Grid battery operations against warranty and LTSA</a></b> · <a href="https://kwwaleszczynski-del.github.io/bess-ops-warranty/">live page</a><br><sub>Across 55 NEM batteries conversion RTE is 0.92, but metered RTE is 0.82 median (0.75 for 1 h, 0.88 for 4 h) because of auxiliaries and standby drain; PASA technical availability is 95.8 % median while commercial offered availability is 78.1 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-capacity-augmentation"><img src="https://kwwaleszczynski-del.github.io/img/bess-capacity-augmentation.webp" alt="Battery ageing vs capacity market obligation"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-capacity-augmentation">Battery ageing vs capacity market obligation</a></b> · <a href="https://kwwaleszczynski-del.github.io/bess-capacity-augmentation/">live page</a><br><sub>Under a strict reading of the four-hour rule a battery built to nominal energy is short in year one; +20 % headroom lasts 7-10 years, and full arbitrage leaves 62-68 % SoH after 17 years.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-hems-mpc"><img src="https://kwwaleszczynski-del.github.io/img/pl-hems-mpc.webp" alt="Home and C&amp;I energy management on 15-minute Polish prices"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-hems-mpc">Home and C&amp;I energy management on 15-minute Polish prices</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-hems-mpc/">live page</a><br><sub>Over Oct 2025 - Sep 2026 the noisy-forecast MILP cuts a dynamic-tariff house's annual cost by 37.4 % (2,378 PLN/yr); on the commercial site a causal ratio rule puts 88.5 % of working days in K1, against a perfect-foresight MILP bound of 98.4 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-thermal-aux-load"><img src="https://kwwaleszczynski-del.github.io/img/bess-thermal-aux-load.webp" alt="Container thermal balance, HVAC auxiliary load and net RTE of a grid battery"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-thermal-aux-load">Container thermal balance, HVAC auxiliary load and net RTE of a grid battery</a></b> · <a href="https://kwwaleszczynski-del.github.io/bess-thermal-aux-load/">live page</a><br><sub>Net RTE at the PCC is 92.4 % at 1 cycle/day with 0.18 C peaks and 88.2 % at the rated 0.5 C; at 0.35 cycles/day it is 89.8 %, because fixed transformer and control loads, not winter, weigh on low cycling. Reported fleet averages are nearer 82 %, so the model is an optimistic bound.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-cppa-shaping-risk"><img src="https://kwwaleszczynski-del.github.io/img/pl-cppa-shaping-risk.webp" alt="Corporate PPA structuring and shaping risk on Polish power prices"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-cppa-shaping-risk">Corporate PPA structuring and shaping risk on Polish power prices</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-cppa-shaping-risk/">live page</a><br><sub>In 2025 a baseload PPA cost a pure PV seller 153.5 PLN/MWh of shaping cost against 27.0 for pure wind, with no interior optimum: cost and P90 are best at 100 % wind, while 24/7 hourly matching peaks at a mix (76.6 % at 80 % wind, 84.2 % with a 4 h battery).</sub></td>
<td width="50%"></td>
</tr>
</table>
</details>

<details>
<summary><b>Power system &amp; resource</b> · 8 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-res-forecast-climate"><img src="https://kwwaleszczynski-del.github.io/img/pl-res-forecast-climate.webp" alt="Wind and solar outlook for Poland, live"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-res-forecast-climate">Wind and solar outlook for Poland, live</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-res-forecast-climate/">live page</a><br><sub>Day-ahead nMAE 11.3 % for solar and 19.8 % for wind over a 12-month test that uses only weather runs published by the 08:40 UTC issue time; the forecast beats climatology by 57-65 % in CRPS.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-forecast-bench"><img src="https://kwwaleszczynski-del.github.io/img/pl-forecast-bench.webp" alt="A citable forecast benchmark for the Polish grid"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-forecast-bench">A citable forecast benchmark for the Polish grid</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-forecast-bench/">live page</a><br><sub>Intraday models beat the PSE plan by 20-26 %; day-ahead nothing that respects the 10:00 issue time beats it for volumes, and the price is the one task a foundation model wins (Chronos-2 with weather covariates, 88.5 PLN/MWh MAE, 9 % better than gradient boosting).</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/poland-mix-sandbox"><img src="https://kwwaleszczynski-del.github.io/img/poland-mix-sandbox.webp" alt="Build Poland&#x27;s power mix with sliders"></a><br><b><a href="https://github.com/kwwaleszczynski-del/poland-mix-sandbox">Build Poland's power mix with sliders</a></b> · <a href="https://kwwaleszczynski-del.github.io/poland-mix-sandbox/">live page</a><br><sub>Coal out by 2030 without new firm capacity leaves 6-10 TWh unserved in every weather year; the 2040 plan makes curtailment the main issue (17-24 % of wind and PV).</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-res-reliability-markov"><img src="https://kwwaleszczynski-del.github.io/img/pl-res-reliability-markov.webp" alt="Capacity credit of wind and PV in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-res-reliability-markov">Capacity credit of wind and PV in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-res-reliability-markov/">live page</a><br><sub>Reproduces the IEEE RTS-79 reference LOLE exactly; wind ELCC about 26.5 % and PV about 10 %. On open farm data an uncalibrated ERA5 + catalogue-curve model misses ELCC by -1.4 to +5.3 points, while failures that cluster in strong wind change it by only 0.02 points.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-flexibility-ramps"><img src="https://kwwaleszczynski-del.github.io/img/pl-flexibility-ramps.webp" alt="Ramps and flexibility needs of the Polish grid"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-flexibility-ramps">Ramps and flexibility needs of the Polish grid</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-flexibility-ramps/">live page</a><br><sub>The evening ramp grew from 1.5 to 4.3 GW between 2021 and 2025; the P99 hourly ramp is 3.2 GW, against 4.6 GW PSE expects for 2030.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-res-curtailment"><img src="https://kwwaleszczynski-del.github.io/img/pl-res-curtailment.webp" alt="PV and wind curtailed by the Polish TSO"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-res-curtailment">PV and wind curtailed by the Polish TSO</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-res-curtailment/">live page</a><br><sub>1.8 TWh curtailed in 2026 to 25 Oct, 50 % more than a year earlier; 98 % for balancing reasons and most of it at positive prices.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/era5-check-pl"><img src="https://kwwaleszczynski-del.github.io/img/era5-check-pl.webp" alt="How good is ERA5 in Poland?"></a><br><b><a href="https://github.com/kwwaleszczynski-del/era5-check-pl">How good is ERA5 in Poland?</a></b> · <a href="https://kwwaleszczynski-del.github.io/era5-check-pl/">live page</a><br><sub>ERA5 overstates 10 m wind by 8 % (median), about 15 % in wind energy; the matrix MCP method cuts the energy error from 41 % to 5 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-grid-connection-ncrfg"><img src="https://kwwaleszczynski-del.github.io/img/pl-grid-connection-ncrfg.webp" alt="Grid connection studies and non-firm capacity on Polish MV/110 kV feeders"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-grid-connection-ncrfg">Grid connection studies and non-firm capacity on Polish MV/110 kV feeders</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-grid-connection-ncrfg/">live page</a><br><sub>On a 14.2 km overhead feeder cos-phi(P) and Q(U) lift hosting capacity from 2.30 MW to 3.21 and 3.11 MW, but cost capacity on a thermally limited cable feeder; on a PVGIS profile a 70 % export cap curtails 6.53 % of PV energy, and pooling wind behind the same 21.54 MW connection carries 1.99 times the energy of firm PV.</sub></td>
</tr>
</table>
</details>

<details>
<summary><b>Monitoring</b> · 3 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/res-uplift-verification"><img src="https://kwwaleszczynski-del.github.io/img/res-uplift-verification.webp" alt="Did the upgrade work? Causal O&amp;M verification"></a><br><b><a href="https://github.com/kwwaleszczynski-del/res-uplift-verification">Did the upgrade work? Causal O&amp;M verification</a></b> · <a href="https://kwwaleszczynski-del.github.io/res-uplift-verification/">live page</a><br><sub>A +3 % uplift needs about 9 weeks to prove with five control turbines, +1 % stays unproven after a year; on real events before/after reports -3.2 % to +3.0 % where the turbines came back within ±1 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/grafana-fleet-as-code"><img src="https://kwwaleszczynski-del.github.io/img/grafana-fleet-as-code.webp" alt="Fleet monitoring as code"></a><br><b><a href="https://github.com/kwwaleszczynski-del/grafana-fleet-as-code">Fleet monitoring as code</a></b><br><sub>Alerts fire on real faults, including a PV inverter that stopped producing ten days before it reported an error code.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/scada-lakehouse-streaming"><img src="https://kwwaleszczynski-del.github.io/img/scada-lakehouse-streaming.webp" alt="Streaming SCADA ingestion, event-time watermarks and a Bronze-Silver-Gold lakehouse for wind and PV"></a><br><b><a href="https://github.com/kwwaleszczynski-del/scada-lakehouse-streaming">Streaming SCADA ingestion, event-time watermarks and a Bronze-Silver-Gold lakehouse for wind and PV</a></b> · <a href="https://kwwaleszczynski-del.github.io/scada-lakehouse-streaming/">live page</a><br><sub>Across 18 simulated LTE outages, naive windowing puts a median 9.2x the true energy into the reconnect quarter-hour (185 % nMAE in affected intervals) and loses 6.0 % of fleet energy on the 25-hour DST day. Event-time windows fix both; how much of the backlog they recover depends on the watermark: 47 % of delayed minutes at 1 h, 81 % at 2 h, 99.6 % at 4 h.</sub></td>
<td width="50%"></td>
</tr>
</table>
</details>

<details>
<summary><b>Open-source tools</b> · 2 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/res-asset-kpi"><img src="https://kwwaleszczynski-del.github.io/img/res-asset-kpi.webp" alt="res-asset-kpi: KPI library for PV, wind and BESS"></a><br><b><a href="https://github.com/kwwaleszczynski-del/res-asset-kpi">res-asset-kpi: KPI library for PV, wind and BESS</a></b> · <a href="https://kwwaleszczynski-del.github.io/res-asset-kpi/">docs</a><br><sub>Extracted from six analysis projects and reproducing their results exactly (41 checks over about a million values, largest relative difference 1.3e-13); a hand-worked test for every formula, Hypothesis property tests, mypy strict, CI on Python 3.11-3.13.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pse-opendata"><img src="https://kwwaleszczynski-del.github.io/img/pse-opendata.webp" alt="pse-opendata: Python client for PSE data"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pse-opendata">pse-opendata: Python client for PSE data</a></b> · <a href="https://kwwaleszczynski-del.github.io/pse-opendata/">docs</a><br><sub>Offline tests on recorded responses plus live checks against PSE's API description; documents pitfalls such as DST labels, the 100,000-row cap and pagination that drops rows.</sub></td>
</tr>
</table>
</details>

<details>
<summary><b>Experiments</b> · 2 projects</summary>

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/fly-novelty-scada"><img src="https://kwwaleszczynski-del.github.io/img/fly-novelty-scada.webp" alt="A fly-brain novelty detector for turbine faults"></a><br><b><a href="https://github.com/kwwaleszczynski-del/fly-novelty-scada">A fly-brain novelty detector for turbine faults</a></b> · <a href="https://kwwaleszczynski-del.github.io/fly-novelty-scada/">live page</a><br><sub>Honest negative result: the fly scores 0.47 against 0.51 for k-NN (0.5 is random), real wiring does no better than shuffled, and after a year of training the filter saturates and stops alarming.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/fly-connectome-forecast"><img src="https://kwwaleszczynski-del.github.io/img/fly-connectome-forecast.webp" alt="Can a fly brain forecast wind and solar?"></a><br><b><a href="https://github.com/kwwaleszczynski-del/fly-connectome-forecast">Can a fly brain forecast wind and solar?</a></b> · <a href="https://kwwaleszczynski-del.github.io/fly-connectome-forecast/">live page</a><br><sub>No: tuned separately, the fly brain matches a random reservoir within 2 %; its compressed eigenvalue spectrum makes it robust to bad settings, not a better forecaster.</sub></td>
</tr>
</table>
</details>


**Stack:** Python · pandas · SciPy / HiGHS MILP · pvlib · PyWake · PyTorch · NumPyro / JAX · Plotly · Grafana · InfluxDB 2 / Flux · GitHub Actions · pytest  
**Open data:** PSE (Polish TSO) open API · AEMO NEM · NREL PVDAQ · Kelmarsh wind farm SCADA (Cubico, CC BY 4.0) · PVGIS · Open-Meteo / ERA5 · Met Office sunshine records · Zenodo LFP cell ageing data · IMGW-PIB synoptic stations · CERRA (Copernicus) · IEEE RTS-79 · CARE to Compare benchmark (CC BY-SA 4.0) · FlyWire connectome v783 (CC BY 4.0)
