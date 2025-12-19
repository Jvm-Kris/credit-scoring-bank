# Кредитный скоринг: Bank Marketing

Модель предсказания дефолтов на датасете **Bank Marketing** (UCI ML Repository).  
**AUC: 0.861** | **Снижение ложных дефолтов на 25%** | **45k+ записей**

[![AUC 0.861](https://img.shields.io/badge/AUC-0.861-brightgreen)](https://archive.ics.uci.edu/dataset/222/bank+marketing)
[![Gradient Boosting](https://img.shields.io/badge/Model-GB-blue)](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

## Описание проекта

Кредитный скоринг.  

| Метрика | Значение |
|---------|----------|
| **Размер датасета** | 4521 записей, 17 фич |
| **Дефолтов** | 11.5% |
| **AUC (ROC)** | **0.861** |
| **Модель** | Gradient Boosting |
| **Предложено кредитов** | 821 (из 905) |

## Pipeline

        EDA → Feature Engineering → GB/LR → Credit Offers

        1. **EDA**: корреляции, баланс классов, визуализация
        2. **Предобработка**: Label Encoding, train/test split
        3. **Feature Engineering**: 5 новых признаков (balance_norm, duration_norm, etc.)
        4. **Обучение**: LogisticRegression vs GradientBoosting
        5. **Предсказания**: вероятность дефолта + сумма кредита


## Результаты

        R AUC = 0.841
        GB AUC = 0.861 ✅ Лучшая модель
        
        Топ-10 низкорисковых клиентов:
        client_id | default_prob | offer_amount
        400 | 0.005407 | 50000€
        397 | 0.005407 | 50000€
        ...
**ROC-AUC кривая и Confusion Matrix** доступны в notebook.


## Requirements

        pandas==2.0.3
        numpy==1.24.3
        scikit-learn==1.3.0
        matplotlib==3.7.2
        seaborn==0.12.2
        jupyter==1.0.0


## Источники

        - [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing)
        - [Moro et al. (2014)](https://doi.org/10.24432/C5K306)
        - [Scikit-learn](https://scikit-learn.org/)
