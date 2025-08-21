# parliament_health
Signals on parliamentary openness for health governance (beta). Automated scrapers + datasets for 5 non-WHO indicators: roll-call openness, health committees, open health budget, pharmacovigilance alerts, risk comms protocol. ESP: Visor y ETL ligero para gobernanza sanitaria.

**EN:** Lightweight, reproducible signals of *parliamentary openness for health governance*, complementary to WHO dashboards.  
**ES:** Señales simples y replicables de *apertura parlamentaria para la gobernanza sanitaria*, complementarias a OMS.

## Indicators (not in standard WHO dashboards)
1) **par_rollcall_open** — Roll-call votes open & downloadable (0/1/2)  
2) **health_comm_exists** — Health committee exists & permanent (0/1/2)  
3) **budget_health_open** — Open health budget data w/ license (0/1/2)  
4) **pharmacovigilance_alerts_pub** — Public drug/device safety alerts (0/1/2)  
5) **moh_riskcomms_protocol_pub** — Risk comms protocol published (0/1)

## Quickstart
```bash
python -m venv .venv
source .venv/bin/activate    # Windows: .venv\Scripts\activate
pip install -r requirements.txt

python src/pipeline.py --seed seeds/sources_seed.csv --year 2025 --out data/processed/observations.csv
