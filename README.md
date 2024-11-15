# CSV Splitter Scripts

Этот проект содержит несколько скриптов на Python для обработки и разбиения данных из CSV-файлов. Скрипты могут разделять данные на файлы по датам, годам и неделям, а также предоставлять доступ к данным по определенной дате.

## Содержимое проекта

- `splitting_x_y.py`: Разделяет исходный CSV-файл на два файла: `X.csv` с датами и `Y.csv` с данными.
- `splitting_year.py`: Разбивает исходный CSV на несколько файлов по годам. Каждый файл содержит данные за один год и именуется по первой и последней дате, содержащейся в файле.
- `splitting_week.py`: Разделяет исходный CSV на файлы по неделям. Каждый файл содержит данные за одну неделю и именуется по первой и последней дате недели.
- `date_search.py`: Функция, которая принимает на вход дату и возвращает данные для этой даты из CSV или `None`, если данных нет.

## Использование

### 1. Разделение на файлы X.csv и Y.csv
Скрипт `splitting_x_y.py` создает два файла с одинаковым количеством строк. Первый файл содержит даты, а второй - значения.

**Запуск скрипта:**
```bash
python splitting_x_y.py
```
Вы можете ввести путь к исходному файлу или использовать путь по умолчанию (`./dataset.csv`). Файлы сохраняются в папке `splitXY` по умолчанию.

### 2. Разделение на файлы по годам
Скрипт `splitting_year.py` создает файлы для каждого года. Имена файлов формируются на основе первой и последней даты в данных.

**Запуск скрипта:**
```bash
python splitting_year.py
```
Данные сохраняются в папке `splitByYear` по умолчанию.

### 3. Разделение на файлы по неделям
Скрипт `splitting_week.py` создает файлы, содержащие данные за каждую неделю.

**Запуск скрипта:**
```bash
python splitting_week.py
```
Результаты сохраняются в папке `splitByWeek`.

### 4. Получение данных по дате
Функция `get_data_by_date` позволяет получить данные для указанной даты из CSV-файла.

**Пример использования:**
```bash
Введите пути до файлов (например, ./dataset.csv):
Введите дату (например, гггг-мм-дд): 2024-11-13
Значение для 2024-11-13: 70.2042
```


## Примечания

- Скрипты поддерживают CSV-файлы, где данные разделены символом `;`.
- При обработке учитывается формат дат `YYYY-MM-DD`.
