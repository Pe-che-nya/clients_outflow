Прогноз оттока клиентов в телеком компании

Описание:

Телеком компании необходимо спрогнозировать отток клиентов и при обнаружении потенциальной потери клиента предложить ему дополнительные условия. С помощью методов машинного обучения необходимо решить задачу бинарной классификации. В качестве итоговой метрики использовать ROC-AUC, но также в отчете предоставить accuracy.

Для обучения используются модель случайных деревьев, логистической регресии, а также модель градиентного бустинга, реализованная в библиотеке catboost.

На первом этапе произведена предобработка данных: выявлены и исправлены пропуски, отредактированы типы данных.

На следующем этапе произведен features engineering. Добавлены новые признаки на основание других. Произведена очистка коррелирующих данных. Статистической проверкой гиппотез подтверждены гиппотезы о совпадении выборок, после чего очищены совпадающие данные.

Для обучения с помощью кросвалидации подготовлены Pipeline, в которых производится исправление дисбаланса классов, кодировка категориальных данных и масштабирование колличественных.

После первого этапа обучения для увеличения итоговой метрики произведен тюнинг порога классификации, а также коэффициента обучения для catboost. С помощью features important выявлены менее влияющие на итоговую метрику признаки и удалены из обучающей выборки.

Таким образом выбрана наилучшая модель, реализованная на catboost с итоговой метрикой ROC-AUC 0.852 и accuracy 0.86.

Используемые библиотеки: pandas, copy, matplotlib, numpy, sklearn, catboost.

Статус проекта: завершен
