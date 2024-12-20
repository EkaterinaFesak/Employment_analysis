# Employment_analysis
В данном репозитории содержится проект по анализу вакансий с карьерного портала HH.ru У проекта есть **отчет в [Табло](https://public.tableau.com/views/_17321292207670/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

**Цель**: Выявить различия в предлагаемых вакансиях для Аналитиков данных и Системных аналитиков.

**Задачи** заключаются в подтверждении или опровержении следующих гипотез:

 - "Среди вакансий аналитиков данных превалирует грейд Junior+, а среди системных аналитиков - Senior"

 - Чаще всего аналитикам данных и системным аналитикам предлагают гибкий или полностью удаленный график

 - Для аналитиков данных hard-skills важнее soft-skills, а для системных аналитиков - наоборот

 - Наиболее желаемым кандидатом на позицию аналитика данных является обладатель сильных hard-скиллов с развитыми навыками коммуникации уровня Junior+

 - Наиболее желаемым кандидатом на позицию системного аналитика является обладатель сильных soft-скиллов и hard-скиллов уровня Senior

**План работы:**

1. Предобработка данных.

2. Исследовательский анализ данных.

3. Выявление грейда требуемых специалистов по названию вакансии или по колонке с требуемым опытом.

4. Определение доли грейдов Junior, Junior+, Middle, Senior среди вакансий Аналитик данных и Системный аналитик.

5. Определение типичного места работы для Аналитика данных и Системного аналитика по следующим параметрам: ТОП-работодателей, зарплата, тип занятости, график работы. Отдельный анализ для грейдов Junior, Junior+, Middle, Senior.

6. Определение, того, какие навыки спрашивают чаще - твердые или мягкие. К какому грейду и к какой специальности требований больше.

7. Определение наиболее желаемых кандидатов на вакансии Аналитик данных и Системный аналитик по следующим параметрам: самые важные hard-skils, самые важные soft-skils. отдельный анализ для грейдов Junior, Junior+, Middle, Senior.

8. Формулирование выводов и рекомендаций.

**Описание данных:**
2 датасета: первый `da` об аналитиках данных, второй - `sа` о системных аналитиках
 
 - `id` - Уникальный идентификатор вакансии.
 
 - `name` - Название вакансии.
 
 - `published_at` - Дата публикации.
 
 - `alternate_url` - Ссылка на вакансию.
 
 - `type` - Статус вакансии на момент получения данных от api и передачи их в базу.
 
 - `employer` - Работодатель.
 
 - `department` - Работодатель, отдел.
 
 - `area` - Регион места работы.
 
 - `experience` - Требуемый опыт работы.
 
 - `key_skills` - Ключевые навыки, в том числе найденные при анализе полного текста вакансии. Поле генерируется после получения информации от api.
 
- `schedule` - График работы.
 
- `employment` - Тип занятости.

- `description` - Описание вакансии.

- `description_lemmatized` - Лемматизированное описание вакансии.

- `salary_from` - Нижняя граница предлагаемой заработной платы.

- `salary_to` - Верхняя граница предлагаемой заработной платы.

- `salary_bin` - Категория зарплаты.

- `key_skills_from_key_skills_field` - Ключевые навыки из поля вакансии key_skills.

- `hard_skills_from_description` - “Твердые” навыки, найденные при обработке полей с навыками. Поле генерируется после получения информации от api. 

- `soft_skills_from_description` - “Мягкие” навыки, найденные при обработке полей с навыками. Поле генерируется после получения информации от api.
