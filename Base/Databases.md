#dev #db

# Databases

## Что такое база данных?

Базы данных являються структурированными сборниками информации, организованные таким образом, что бы обеспечить эффективное хранение, управление и доступ к информации.

Может содержать любые типы данных, включая слова, цифры, изображения, видео и файлы.

Для хранения, извлечения и редактирования данных можно использовать программное обеспечение, называемое системой управления базами данных (СУБД).
## Почему база данных важна?

Базы данных поддерживают внутреннюю деятельность компаний и хранят данные о взаимодействиях с клиентами и поставщиками.

### **Эффективное масштабирование**

Приложения баз данных могут управлять большими объемами данных с масштабированием до миллионов, миллиардов и более. Невозможно хранить такое количество цифровых данных без базы данных.

### **Целостность данных**

Базы данных часто имеют встроенные правила и условия для обеспечения согласованности данных.

### **Безопасность данных**

Базы данных поддерживают требования конфиденциальности и соответствия, связанные с любыми данными. Например, для получения доступа к базе данных пользователям необходимо войти. Различным пользователям предоставляются разные уровни доступа, например только для чтения.

### **Аналитика данных**

Современные программные системы используют базы данных для анализа данных. Эти системы могут выявлять тенденции и закономерности или делать прогнозы. Аналитика данных позволяет организациям с уверенностью принимать бизнес-решения.

## Какие существуют типы баз данных?

Базы данных можно классифицировать по примеру использования, типу данных и способу их хранения. Ниже перечислены три примера способов классификации баз данных.

- Классификация по содержимому баз данных (например, текст документа, статистический или мультимедийный объект)
- Классификация по области применения (бухгалтерия, кинематограф или производство)
- Классификация по техническим аспектам (структура базы данных или тип интерфейса)

## Что такое модель базы данных?

Модель базы данных показывает ее логическую структуру. Она определяет отношения и правила хранения и организации данных, а также управления ими. Каждое приложение базы данных создано на основе определенной модели данных. Индивидуальные модели баз данных разрабатываются на основе правил и концепций более широкой модели данных, используемой в базовых приложениях.

## Как развивались базы данных?

Самые первые базы данных представляли собой магнитные ленты, на которых записи данных хранились в последовательной форме. Базы данных продолжали совершенствоваться с развитием технологий. Сегодня они превратились в сложные высокопроизводительные системы, которым посвящена собственная область исследования. Рассмотрим историю развития моделей данных.

### **Иерархическая база данных**

Иерархические базы данных стали популярными в 1970-х годах. На смену последовательной форме хранения записей данных пришла _древовидная структура_, в которой два файла находились в отношении «предок-потомок». Например, при создании системы базы данных для розничного мебельного магазина можно было определить _спальню_ как запись-предок, а _кровать_, _прикроватную тумбочку_ и _шкаф_ – как записи-потомки. Кроме того, к записи _кровать_ можно было добавить другие записи-потомки, такие как _односпальная кровать_, _двуспальная кровать_, _большая двуспальная кровать_ и т. д. К сожалению, иерархическая модель данных была сложной для реализации и не могла поддерживать несколько родительско-дочерних отношений без значительного дублирования данных.

### **Сетевая база данных**

У другой ранней базы данных – сетевой – у одной записи-потомка может иметься несколько записей-предков и наоборот. Так в примере с мебельным магазином две записи типа предок (_спальня_ и _детская комната_) можно связать с записью-потомком _шкаф_.

### **Реляционная база данных**

В 1980-х годах среди предприятий стали популярными реляционные базы данных благодаря своей высокой производительности, гибкости и совместимости с более быстрым оборудованием. В реляционных базах данных записи организованы в виде нескольких таблиц, а не связанных списков. 

В модели реляционной базы данных каждая категория имеет таблицу, в которой атрибуты категорий представлены в виде столбцов, а записи данных – в виде строк. Например, можно создать модель розничного мебельного магазина в виде набора таблиц под названием _Комнаты_ и _Мебель_. Таблицы связаны столбцами _Номер комнаты_ и __Название мебели__. Оба этих столбца также называются _первичными ключами_.

|Номер комнаты|Название комнаты|
|---|---|
|1|Спальня|
|2|Детская комната|

|Название мебели|Цвет|
|---|---|
|Кровать|Коричневый|
|Шкаф|Белый|
|Прикроватная тумбочка|Черный|

|Номер комнаты|Название мебели|
|---|---|
|1|Кровать|
|1|Шкаф|
|2|Шкаф|


### zero links
### references
- https://aws.amazon.com/ru/what-is/database/

- https://aws.amazon.com/nosql/graph/
- https://azure.microsoft.com/ru-ru/resources/cloud-computing-dictionary/what-are-databases/
- https://aws.amazon.com/ru/what-is/sql/
- https://habr.com/ru/companies/amvera/articles/754702/
- https://www.digitalocean.com/community/tutorials/understanding-relational-databases-ru
- 