# booking
Предсказание рейтинга отеля на booking.com

## Постановка задачи бизнесом
Необходимо обнаружить нечестные отели, которые накручивают себе рейтинг. В качестве решения предлагается обучить модель машинного обучения на данных об отзывах о гостиницах. Если предсказания модели сильно отличаются от наблюдаемого результата, то, возможно, отель ведёт себя нечестно, и его стоит проверить.
Эффективность модели оценивается по величине средней абсолютной процентной ошибки (MAPE). Бэйслайн - результат RandomForestRegressor на сырых данных (MAPE = 14.15449)

## Декомпозиция задачи
1. Изучение данных 
2. Подготовка данных:
  1) Очистка данных (удаление или замена явных выбросов и пропусков)
  2) Генерация признаков (извлечение признаков из предоставленных данных и внешних источников, кодировка, нормализация)
  3) Отбор признаков (удаление нечисловых признаков, тест на мультиколлинеарность)
3. Выбор и обучение модели (тот же ансамбль деревьев)
4. Оценка эффективности 

## Итог
Новое значение MAPE составило 13.56128 (до нормализации). Видно улучшению относительно бэйслайна, причем только за счет EDA и Feature Engineering (без изменения самой ML-модели)
