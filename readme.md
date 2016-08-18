# Машинные предсказания итогов выборов в Беларуси

Экспериментальный проект по созданию моделей для машинного предсказания результатов выборов в Беларуси. Пока проект ограничивается данными о выборах в нижнюю палату парламента.

В папке doc_original находятся оригинальные сообщения из [архива](http://rec.gov.by/ru/arhiv-vybory) Центральной комиссии Республики Беларусь по выборам о регистрации кандидатов в депутаты Палаты представителей и об итогах выборов в 2000 (2 тура), 2004, 2008, 2012 и 2016 (только кандидаты) годах.

Набор данных train.csv содержит информацию о зарегистрированных кандидатах на выборах 2000, 2004, 2008, 2012, 2016 годов, а также по кампаниям повторных выборов 2005 и 2014 годов и данные о прохождении кандидата в парламент.

## Структура набора

- region: регион, в котором расположен избирательный округ
- fio: ФИО кандидата
- pol: пол кандидата
- born: год рождения кандидата
- info: информация о кандидате, которую опубликовала ЦК по выборам
- deputat: является или нет депутатом Парламента на момент участия в
  избирательной кампании(1 - да, 0 - нет)
- party: партийная принадлежность кандидата
- place: место жительства
- okrug: название и номер избирательного округа
- year: год, в котором проводилась избирательная кампания
- status: избран или не избран депутатом по итогам выборов
- comment: комментарий
- vydvinut: способ выдвижения (только для кампании 2016 года)

Поле status - главное для всей затеи с предсказанием. Его нужно заполнить для кандидатов 2016 года до 12 сентября, когда ЦК по выборам начнет объялять результаты.
