# MLMedicine
Применение машинного обучения для решения медицинских задач
# Проекты по анализу медицинских данных
Данный репозиторий содержит 4 самостоятельных проекта, в которых демонстрируются различные подходы и инструменты машинного обучения для анализа медицинских данных. В частности, рассмотрены задачи классификации медицинских изображений, сегментации кожных образований и прогнозирования заболевания диабетом на основе клинических показателей.

---

## Содержание

1. [Описание проектов](#описание-проектов)
2. [Требования к окружению](#требования-к-окружению)
3. [Структура репозитория](#структура-репозитория)
4. [Используемые инструменты](#используемые-инструменты)
5. [Как запустить](#как-запустить)
6. [Контакты](#контакты)

---

## Описание проектов

### 1. [Классификация медицинских изображений](Pneumonia)
- **Задача:** Обнаружение пневмонии по рентгеновским снимкам грудной клетки.
- **Данные:** [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia).
- **Краткое описание:**
    - Выполнена загрузка и предобработка рентгеновских снимков (очистка, приведение к единым размерам, нормализация).
    - Использованы сверточные нейронные сети (CNN) для обучения модели классификации.
    - Проведена оценка качества с использованием метрик точности, полноты и F1-меры.

### 2. [Сегментация медицинских изображений](Segmentation)
- **Задача:** Сегментация кожных образований на дерматоскопических изображениях.
- **Данные:** [ISIC 2018 Challenge - Task 1: Lesion Segmentation](https://www.kaggle.com/datasets/tschandl/isic2018-challenge-task1-data-segmentation).
- **Краткое описание:**
    - Предварительная обработка изображений: аугментация, приведение к нужным размерам, нормализация.
    - Реализована архитектура U-Net (или аналогичные сегментационные сети) для точного определения границ кожных образований.
    - Результаты оценивались при помощи метрик IoU (Intersection over Union), Dice coefficient и др.

### 3. [Прогнозирование заболеваний диабета](Predict_Diabetes)
- **Задача:** Классификация наличия или отсутствия диабета на основе клинических данных.
- **Данные:** [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database/data).
- **Краткое описание:**
    - Проведена первичная очистка данных, замена некорректных значений, а также заполнение пропусков.
    - Применены методы балансировки классов (SMOTE) и нормализации признаков (StandardScaler).
    - Обучение и оценка классификаторов (RandomForest, Logistic Regression и др.) с анализом метрик (Accuracy, Precision, Recall, ROC-AUC).
    - Использованы SHAP-значения и анализ важности признаков для интерпретации работы модели.

---

## Требования к окружению

- Python 3.7+
- Jupyter Notebook или JupyterLab (при желании)
- Библиотеки:
    - NumPy
    - Pandas
    - Matplotlib / Seaborn
    - scikit-learn
    - TensorFlow / PyTorch (в зависимости от реализации нейронных сетей)
    - imbalanced-learn (для SMOTE)
    - SHAP (для интерпретации моделей)

---

## Используемые инструменты

- **scikit-learn** — машинное обучение и классические алгоритмы классификации, регрессии, кластеризации.
- **TensorFlow/PyTorch** — фреймворки для глубокого обучения (использовались в задачах классификации и сегментации изображений).
- **NumPy, Pandas** — базовые библиотеки для научных вычислений и работы с данными.
- **Matplotlib, Seaborn** — инструменты визуализации данных.
- **imbalanced-learn** — методы балансировки данных (SMOTE, ADASYN и т. д.).
- **SHAP** — инструмент для интерпретации моделей и оценки вклада признаков.

---

## Как запустить

1. **Клонировать репозиторий**:
   ```bash
   git clone https://github.com/Soundflog/MLMedicine.git
   ```
2. Установить необходимые библиотеки (например, через pip или conda):
    ```bash
   pip install -r requirements.txt
   ```
При отсутствии файла requirements.txt установите библиотеки вручную по списку выше.

3. Открыть соответствующий проект (например, classification, segmentation или diabetes_prediction) и запустить Jupyter Notebook:
    ```bash
   jupyter notebook
   ```
4. Запустить ноутбук с шагами обработки данных, обучения и оценки модели.

