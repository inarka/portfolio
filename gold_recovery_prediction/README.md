# Прогнозирование коэффициента восстановления золота

## Описание проекта
Компания «Цифра» занимается разработкой решений для повышения эффективности промышленных предприятий. Одной из ключевых задач является оптимизация процессов добычи и очистки золотосодержащей руды. Для этого необходимо разработать модель машинного обучения, способную предсказывать коэффициент восстановления золота из руды, что позволит оптимизировать производство и избегать запуска убыточных предприятий.

## Использованные технологии и библиотеки

**Язык программирования:** Python

**Библиотеки:** pandas, numpy, matplotlib, seaborn, sklearn, os.

## Описание данных
В нашем распоряжении 3 файла с сырыми данными:
- gold_industry_train.csv — обучающая выборка;
- gold_industry_test.csv — тестовая выборка;
- gold_industry_full.csv — исходные данные.

В процессе реализации проекта также была проведена проверка данных на корректность. 

## Методология

1. Подготовка данных
- Изучение данных: Загрузка и первичный анализ предоставленных датасетов.
- Проверка расчета эффективности обогащения: Исследование правильности расчета эффективности обогащения на обучающей выборке и вычисление MAE между расчетными значениями и данными в датасете для анализа точности данных.
- Анализ признаков, недоступных в тестовой выборке.
- Предобработка данных: Очистка данных от аномалий, обработка пропущенных значений и приведение данных к формату, пригодному для анализа и моделирования.
2. Анализ данных
- Исследование концентрации металлов: Анализ изменения концентрации основных металлов (Au, Ag, Pb) на различных этапах очистки.
- Сравнение распределений размеров гранул сырья: Анализ и сравнение распределений размеров гранул сырья в обучающей и тестовой выборках для оценки возможного влияния на качество модели.
- Анализ суммарной концентрации металлов: Исследование суммарной концентрации металлов на разных стадиях процесса для оценки эффективности процесса очистки.
3. Построение модели
- Разработка функции для вычисления sMAPE: Создание специализированной функции для оценки качества моделей, учитывающей специфику задачи.
- Обучение и оценка моделей: Тренировка различных моделей машинного обучения с использованием кросс-валидации для нахождения оптимальной модели.
- Выбор лучшей модели и тестирование: Определение модели с лучшими показателями качества и ее тестирование на тестовой выборке для итоговой оценки эффективности.
4. Анализ результатов
- Оценка полученных результатов, анализ эффективности лучшей модели на тестовых данных.

## Выводы
В ходе выполнения проекта была успешно реализована модель машинного обучения для предсказания коэффициента восстановления золота из руды. Это позволит компании «Цифра» эффективно управлять производственными процессами, оптимизировать расходы и повышать общую эффективность работы промышленных предприятий. 



