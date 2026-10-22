### Renewable energy data analytics

[**Interactive Portfolio**](https://kwwaleszczynski-del.github.io/) · [**LinkedIn**](https://www.linkedin.com/in/kw00) · [*****REMOVED*****](mailto:***REMOVED***)

Analytics for solar, wind and battery assets: performance verification, fault detection, power market analysis and dashboards. Every project below is written from scratch on open data and can be rerun from its repository, with tests and CI.

**Live pages:** [Polish power market, live](https://kwwaleszczynski-del.github.io/pl-power-market-live/) · [How solar eats its own price in Poland](https://kwwaleszczynski-del.github.io/pl-capture-price/) · [When batteries flatten their own spreads](https://kwwaleszczynski-del.github.io/pl-bess-saturation/) · [Cable pooling: PV, wind and storage behind one connection](https://kwwaleszczynski-del.github.io/cable-pooling-sizer/) · [Battery ageing vs capacity market obligation](https://kwwaleszczynski-del.github.io/bess-capacity-augmentation/) · [Single-axis trackers in 3D](https://kwwaleszczynski-del.github.io/pv-tracker-shading-3d/) · [PV thermal check: modules, inverter, transformer](https://kwwaleszczynski-del.github.io/pv-thermal-check/) · [Wakes and shadow flicker](https://kwwaleszczynski-del.github.io/wind-wake-shadow/) · [Capacity credit of wind and PV in Poland](https://kwwaleszczynski-del.github.io/pl-res-reliability-markov/) · [Ramps and flexibility needs of the Polish grid](https://kwwaleszczynski-del.github.io/pl-flexibility-ramps/) · [How good is ERA5 in Poland?](https://kwwaleszczynski-del.github.io/era5-check-pl/)  
**Own verification methods:** [Battery state of charge and ageing](https://github.com/kwwaleszczynski-del/bess-soc-soh-degradation) · [PV shading from AC power alone](https://github.com/kwwaleszczynski-del/pv-shade-fingerprint) · [WARP: wake-aware turbine verification](https://github.com/kwwaleszczynski-del/wind-wake-aware-verification)

#### Solar PV

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-shade-fingerprint"><img src="https://kwwaleszczynski-del.github.io/img/pv-shade-fingerprint.webp" alt="PV shading from AC power alone"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-shade-fingerprint">PV shading from AC power alone</a></b><br><sub>A building's silhouette recovered with mask IoU 0.93 and 0.8 deg RMSE on simulated systems, then run on two years of a real PVDAQ roof.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-tracker-shading-3d"><img src="https://kwwaleszczynski-del.github.io/img/pv-tracker-shading-3d.webp" alt="Single-axis trackers in 3D"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-tracker-shading-3d">Single-axis trackers in 3D</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-tracker-shading-3d/">live page</a><br><sub>Backtracking gives +4.3 % DC yield over true tracking on flat ground (1255 vs 1204 kWh/kWp).</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-anomaly-autoencoder"><img src="https://kwwaleszczynski-del.github.io/img/pv-anomaly-autoencoder.webp" alt="PV fault detection: autoencoder vs baselines"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-anomaly-autoencoder">PV fault detection: autoencoder vs baselines</a></b><br><sub>F1 0.77 against 0.37-0.48 for the baselines; on real data it caught an inverter outage reported 10 days late by the inverter itself.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pv-thermal-check"><img src="https://kwwaleszczynski-del.github.io/img/pv-thermal-check.webp" alt="PV thermal check: modules, inverter, transformer"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pv-thermal-check">PV thermal check: modules, inverter, transformer</a></b> · <a href="https://kwwaleszczynski-del.github.io/pv-thermal-check/">live page</a><br><sub>The back-of-module sensor saw only about half of the real heating: thermal losses are 10.5 % a year, not 6.7 %; temperature-corrected PR cuts the seasonal spread from 13.1 to 4.8 pp.</sub></td>
</tr>
</table>

#### Wind

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-wake-aware-verification"><img src="https://kwwaleszczynski-del.github.io/img/wind-wake-aware-verification.webp" alt="WARP: wake-aware turbine verification"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-wake-aware-verification">WARP: wake-aware turbine verification</a></b><br><sub>Validated on 288 injected faults: a 4 deg yaw misalignment is found in 100 % of cases (median 6 days), standard references find 6-10 %.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-power-curve-kelmarsh"><img src="https://kwwaleszczynski-del.github.io/img/wind-power-curve-kelmarsh.webp" alt="Wind power curves (IEC 61400-12-1)"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-power-curve-kelmarsh">Wind power curves (IEC 61400-12-1)</a></b><br><sub>Caught a silent change of the SCADA wind speed definition that made the turbines look up to 14 % better than they were.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/wind-wake-shadow"><img src="https://kwwaleszczynski-del.github.io/img/wind-wake-shadow.webp" alt="Wakes and shadow flicker"></a><br><b><a href="https://github.com/kwwaleszczynski-del/wind-wake-shadow">Wakes and shadow flicker</a></b> · <a href="https://kwwaleszczynski-del.github.io/wind-wake-shadow/">live page</a><br><sub>Measured wake loss 9.2 %: Gaussian model 9.7 %, Jensen 11.4 %, TurbOPark 12.1 %.</sub></td>
<td width="50%"></td>
</tr>
</table>

#### Storage & markets

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-power-market-live"><img src="https://kwwaleszczynski-del.github.io/img/pl-power-market-live.webp" alt="Polish power market, live"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-power-market-live">Polish power market, live</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-power-market-live/">live page</a><br><sub>No server and no database: GitHub Actions rebuilds a static page from cached monthly Parquet files.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-capture-price"><img src="https://kwwaleszczynski-del.github.io/img/pl-capture-price.webp" alt="How solar eats its own price in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-capture-price">How solar eats its own price in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-capture-price/">live page</a><br><sub>In 2025 PV captured 64 % of the average price and wind 94 %; every 10 pp of PV share costs PV about 0.20 of value factor.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-arbitrage-pl"><img src="https://kwwaleszczynski-del.github.io/img/bess-arbitrage-pl.webp" alt="Battery arbitrage on Polish prices"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-arbitrage-pl">Battery arbitrage on Polish prices</a></b><br><sub>859-day backtest: a 2-hour battery earned 308 k PLN per MW in 2025, and negative prices reached 354 hours that year.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-bess-saturation"><img src="https://kwwaleszczynski-del.github.io/img/pl-bess-saturation.webp" alt="When batteries flatten their own spreads"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-bess-saturation">When batteries flatten their own spreads</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-bess-saturation/">live page</a><br><sub>At 2025 prices a 2-hour battery earns 308 k PLN/MW alone, 203 k at 2 GW of fleet and 72 k at 10 GW; the marginal value of the fleet turns negative near 10 GW.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/cable-pooling-sizer"><img src="https://kwwaleszczynski-del.github.io/img/cable-pooling-sizer.webp" alt="Cable pooling: PV, wind and storage behind one connection"></a><br><b><a href="https://github.com/kwwaleszczynski-del/cable-pooling-sizer">Cable pooling: PV, wind and storage behind one connection</a></b> · <a href="https://kwwaleszczynski-del.github.io/cable-pooling-sizer/">live page</a><br><sub>Best oversizing is 1.75-2.25x the connection without a battery and 2.75-3x with one, curtailing 9-20 % of the energy.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/nem-battery-behaviour"><img src="https://kwwaleszczynski-del.github.io/img/nem-battery-behaviour.webp" alt="How real batteries trade"></a><br><b><a href="https://github.com/kwwaleszczynski-del/nem-battery-behaviour">How real batteries trade</a></b><br><sub>The six largest batteries earn 11-51 % of their perfect-foresight optimum; the gap is split into capacity offered, volume and timing.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-soc-soh-degradation"><img src="https://kwwaleszczynski-del.github.io/img/bess-soc-soh-degradation.webp" alt="Battery state of charge and ageing"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-soc-soh-degradation">Battery state of charge and ageing</a></b><br><sub>SoC from 5-minute market data tracks the operator's SoC within 2.7-3.8 percentage points (RMSE).</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/bess-capacity-augmentation"><img src="https://kwwaleszczynski-del.github.io/img/bess-capacity-augmentation.webp" alt="Battery ageing vs capacity market obligation"></a><br><b><a href="https://github.com/kwwaleszczynski-del/bess-capacity-augmentation">Battery ageing vs capacity market obligation</a></b> · <a href="https://kwwaleszczynski-del.github.io/bess-capacity-augmentation/">live page</a><br><sub>Built to nominal energy, a battery misses its obligation in year one; +20 % headroom lasts 7-10 years, and full arbitrage leaves 62-68 % SoH after 17 years.</sub></td>
</tr>
</table>

#### Power system & resource

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-res-reliability-markov"><img src="https://kwwaleszczynski-del.github.io/img/pl-res-reliability-markov.webp" alt="Capacity credit of wind and PV in Poland"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-res-reliability-markov">Capacity credit of wind and PV in Poland</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-res-reliability-markov/">live page</a><br><sub>Reproduces the IEEE RTS-79 reference LOLE exactly; wind ELCC about 26.5 % and PV about 10 %, compared with capacity market derating factors.</sub></td>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/pl-flexibility-ramps"><img src="https://kwwaleszczynski-del.github.io/img/pl-flexibility-ramps.webp" alt="Ramps and flexibility needs of the Polish grid"></a><br><b><a href="https://github.com/kwwaleszczynski-del/pl-flexibility-ramps">Ramps and flexibility needs of the Polish grid</a></b> · <a href="https://kwwaleszczynski-del.github.io/pl-flexibility-ramps/">live page</a><br><sub>The evening ramp grew from 1.5 to 4.3 GW between 2021 and 2025; the P99 hourly ramp is 3.2 GW, against 4.6 GW PSE expects for 2030.</sub></td>
</tr>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/era5-check-pl"><img src="https://kwwaleszczynski-del.github.io/img/era5-check-pl.webp" alt="How good is ERA5 in Poland?"></a><br><b><a href="https://github.com/kwwaleszczynski-del/era5-check-pl">How good is ERA5 in Poland?</a></b> · <a href="https://kwwaleszczynski-del.github.io/era5-check-pl/">live page</a><br><sub>ERA5 overstates 10 m wind by 8 % (median), about 15 % in wind energy; the matrix MCP method cuts the energy error from 41 % to 5 %.</sub></td>
<td width="50%"></td>
</tr>
</table>

#### Monitoring

<table>
<tr>
<td width="50%" valign="top"><a href="https://github.com/kwwaleszczynski-del/grafana-fleet-as-code"><img src="https://kwwaleszczynski-del.github.io/img/grafana-fleet-as-code.webp" alt="Fleet monitoring as code"></a><br><b><a href="https://github.com/kwwaleszczynski-del/grafana-fleet-as-code">Fleet monitoring as code</a></b><br><sub>Alerts fire on real faults, including a PV inverter that stopped producing ten days before it reported an error code.</sub></td>
<td width="50%"></td>
</tr>
</table>

**Stack:** Python · pandas · SciPy / HiGHS MILP · pvlib · PyWake · PyTorch · Plotly · Grafana · InfluxDB 2 / Flux · GitHub Actions · pytest  
**Open data:** PSE (Polish TSO) open API · AEMO NEM · NREL PVDAQ · Kelmarsh wind farm SCADA (Cubico, CC BY 4.0) · PVGIS · Open-Meteo / ERA5 · Met Office sunshine records · Zenodo LFP cell ageing data · IMGW-PIB synoptic stations · CERRA (Copernicus) · IEEE RTS-79
