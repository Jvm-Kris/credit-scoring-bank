# credit-scoring-bank
**Модель предсказания дефолтов (AUC 0.85+)**

Модель машинного обучения для предсказания дефолтов по кредитам с использованием датасета bank.csv (45k записей). Достигнут ROC-AUC 0.85+ на моделях Gradient Boosting и Logistic Regression.

## Результаты
- Dataset: bank.csv (45k записей)
- Модель: Gradient Boosting / Logistic Regression
- Метрики:

        1) ROC-AUC	0.87 (Gradient Boosting),	0.85 (Logistic Regression)
        2) Precision	0.82 (Gradient Boosting),	0.79 (Logistic Regression)
        3) Recall	0.84 (Gradient Boosting),	0.81 (Logistic Regression)

Модель обучена в Jupyter notebook: scoring_model.ipynb.

Установка:

    - Установите зависимости: pip install -r requirements.txt (pandas, scikit-learn, xgboost)
    - Скачайте датасет bank.csv в корень проекта.

Использование:
Запустите notebook: jupyter notebook scoring_model.ipynb

    - Загрузка и предобработка данных
    - Обучение моделей
    - Валидация и метрики
    - Сохранение лучшей модели

Для предсказаний на новых данных используйте сохраненную модель из notebook.
Технологии:

    - Python 3.9+
    - pandas, numpy
    - scikit-learn
    - xgboost
    - matplotlib, seaborn
