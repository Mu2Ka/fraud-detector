# Обнаружение мошеннических транзакций

Проект по классификации сильно несбалансированных данных для выявления мошеннических операций по банковским картам. Ноутбук объединяет supervised learning, anomaly detection, feature engineering, настройку гиперпараметров и подбор рабочего порога решения.

## Подход

- анализ дубликатов, пропусков и дисбаланса классов;
- исследование суммы транзакций и частоты мошенничества по часам и дням;
- сравнение One-Class SVM, Isolation Forest и XGBoost;
- оценка по ROC-AUC, PR-AUC, precision и recall;
- генерация временных признаков, логарифма суммы и anomaly scores;
- оптимизация XGBoost по PR-AUC с помощью Optuna;
- выбор порога решения с ограничением на минимальный recall;
- анализ false positives и false negatives во времени.

## Инструменты

Python, pandas, NumPy, scikit-learn, XGBoost, Optuna, matplotlib, seaborn, Jupyter.

## Датасет

Скачайте [Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) и поместите файл `creditcard.csv` в корень проекта.


## Локальный запуск

```bash
pip install -r requirements.txt
jupyter notebook fraud_detector.ipynb
```
