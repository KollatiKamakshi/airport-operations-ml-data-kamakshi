# Flight Delay ML: Kamakshi's part (data quality, comparison, tests, docs)

Part of the Airport Operations Coordination Engine (Infosys Springboard 7.0).
Outputs are estimates for decision support only.

## My files

| File                           | Purpose                                                                                          |
| ------------------------------ | ------------------------------------------------------------------------------------------------ |
| `04_check_dataset.py`          | Schema, leakage, missing-value and delay-rate checks                                             |
| `tests/toy_data.py`            | TEST-ONLY fake data generator                                                                    |
| `tests/`                       | pytest tests (checker, community model, metrics, baselines, explainer, forecast, predict_flight) |
| `ml/community_model.py`        | Community-model comparison harness (documented as not comparable)                                |
| `notebooks/report_plots.ipynb` | EDA and results charts                                                                           |
| `docs/model_card.md`           | Model card (draft; PENDING items marked)                                                         |

## Run (from this folder)

    python -m venv venv
    venv\Scripts\activate
    pip install -r requirements.txt
    pip install matplotlib jupyter ipykernel
    python 04_check_dataset.py data/sample_flights.parquet
    pytest -v

Needs `data/` (sample and full dataset) and `models/` from Google Drive; they are not in Git.
