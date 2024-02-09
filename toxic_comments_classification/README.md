# Прогнозирование коэффициента восстановления золота

## Описание проекта
Интернет-магазин "Викишоп" запускает новый сервис, позволяющий пользователям редактировать и дополнять описания товаров. Для поддержания здоровой атмосферы в сообществе магазину необходим инструмент, способный выявлять токсичные комментарии и отправлять их на модерацию. Цель проекта — разработать модель машинного обучения, которая сможет классифицировать комментарии на позитивные и негативные.

## Использованные технологии и библиотеки

**Язык программирования:** Python 3.7+

**Библиотеки:** pandas, re, spacy, nltk, tqdm, sklearn, lightgbm 

## Описание данных
В нашем распоряжении 3 файла с сырыми данными:
- gold_industry_train.csv — обучающая выборка;
- gold_industry_test.csv — тестовая выборка;
- gold_industry_full.csv — исходные данные.

В процессе реализации проекта была проведена проверка данных на корректность. 

## Методология

1. Загрука и знакомство с данными
- Изучение данных: Ознакомление с предоставленным датасетом, содержащим тексты комментариев и маркеры их токсичности.
2. Предобработка данных
- Очистка текста: Удаление из текстов лишних символов.
- Нормализация: Приведение всех слов текста к нижнему регистру для унификации данных.
- Удаление стоп-слов: Исключение из текстов слов, не несущих значимой информации для анализа.
- Лемматизация: Приведение слов к их словарной форме (леммам).
3. Обучение моделей и выбор наилучшей
- Подготовка выборок: Разделение датасета на обучающую и тестовую выборки для оценки эффективности моделей.
- Векторизация текстов: Применение TF-IDF векторизации для преобразования текстов в числовой формат.
- Обучение моделей и подбор гиперпараметров: Обучение нескольких моделей (Логистическая регрессия, Случайный лес, LightGBM) с использованием кросс-валидации для поиска оптимальных гиперпараметров.
- Выбор наилучшей модели: Определение модели Логистической регрессии как наиболее эффективной для задачи классификации токсичных комментариев.
5. Тестирование модели
- Проверка модели на адекватность: Сравнение результатов отобранной модели с результатами базовой дамми модели для подтверждения адекватности нашей обученной модели.
- Оценка на тестовой выборке: Проверка выбранной модели Логистической регрессии на тестовой выборке для финальной оценки её эффективности.

## Выводы
Модель для классификации токсичных комментариев была успешно разработана и обучена, демонстрируя высокую точность в определении негативного контента. Это позволяет автоматизировать процесс модерации комментариев в новом сервисе интернет-магазина "Викишоп", способствуя созданию здоровой и уважительной атмосферы общения в сообществе.


