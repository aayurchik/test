# COAST Steering on PushT

Репозиторий содержит реализацию и результаты экспериментов по применению activation steering к предобученной state-based Diffusion Policy в среде PushT.

В работе сравниваются два метода:

- **Difference-in-Means (DiM)** — вмешательство на основе разности средних активаций успешных и неуспешных эпизодов.
- **COAST-style steering** — вмешательство на основе контрастивных концепторов, построенных по ковариационным матрицам активаций.

## Структура проекта

```text
.
├── COAST_PushT.ipynb
├── Report_COAST_PushT.pdf
├── README.md
│
├── config/
│   └── metadata.json
│
├── baseline/
│   ├── results_baseline.pkl
│   └── baseline_test_*.pkl
│
└── steering/
    ├── steering_train_act_*.pkl
    ├── results_mean_steering.pkl
    └── results_coast.pkl

```

## Описание файлов

- **`COAST_PushT.ipynb`** — основной ноутбук с реализацией экспериментов.
- **`Report_COAST_PushT.pdf`** — отчёт с методологией и результатами.
- **`config/metadata.json`** — параметры модели и эксперимента.
- **`baseline/results_baseline.pkl`** — агрегированные результаты базовой модели.
- **`baseline/baseline_test_*.pkl`** — данные отдельных тестовых эпизодов базовой модели.
- **`steering/steering_train_act_*.pkl`** — активации обучающих эпизодов для построения операторов steering.
- **`steering/results_mean_steering.pkl`** — результаты метода Difference-in-Means.
- **`steering/results_coast.pkl`** — результаты метода COAST.
