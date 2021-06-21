# Software-Testing

## Junior QA requirements

### Основы, определения, виды тестирования
Качество ПО - это совокупность характеристик ПО, относящихся к его способности удовлетворять установленные и предполагаемые потребности.  
Обеспечение качества (QA) - комплекс мероприятий направленный на обеспечение качества разрабатываемого продукта, на всех стадиях разработки.   
Тестирование ПО (Software Testing) – процесс анализа программного средства и сопутствующей документации с целью выявления дефектов и повышения качества продукта.  
Quality Control направлено на поиск дефектов в готовом продукте для того, чтобы убедиться, что продукт соответствует требованиям и готов к передаче пользователю (заказчику).  
Quality Assurance направлено больше на процессы, их усовершенствование (оптимизацию) для минимизации количества багов (дефектов) в самом начале разработки продукта. Это довольно эффективно, так как анализируются все аспекты в самом начале, а не когда продукт готов и выясняется, что работать с ним не совсем удобно или можно реализовать функциональность по-другому.  

#### Объекты тестирования
* Программы при их непосредственном запуске и исполнении (software).
* Код программ без запуска и исполнения (code).
* Прототип программного продукта (product prototype). 
* Проектная документация (project documentation):
  * Требования к продукту (product requirements).
  * Функциональные  спецификации к продукту (functional specifications).
  * Документы по архитектуре (product architecture) и дизайну (product design).
  * План проекта (project plan).
  * Тестовые сценарии (test cases).
* Сопроводительная документация:
  * Интерактивная помощь (on-line help).
  * Руководства  по  установке  (Installation guide)  и  использованию (user manual).

#### Этапы тестирования (жизненный цикл тестирования)
* Анализ требований. Изучаем спецификации требований, функциональные требования к системе. Отвечаем на вопросы: что нам предстоит тестировать, как много будет работы, какие есть сложности, всё ли необходимое у нас есть. Получаем данные, по которым составляем план тестирования.
* Планирование испытаний. Определяем объемы испытаний и ресурсы, пишем расписание того, когда будем выполнять намеченные действия.
* Проектирование тестов. Определяем: цель тестирования, специфику входных данных (классы эквивалентности...), модули и подмодули приложения, архитектуру проверок (группы чек-листов), архитектуру тестов (детализация от крупного к деталям). Пишем тесты.
* Запуск тестов. Проверяем тесты в действии, анализируем тестовые результаты.
* Редактирование тестов. Пересматриваем и корректируем тесты, держим тесты в актуальном состоянии, дополняем новыми тестами.
* Системное тестирование. Проверяем всю систему (все модули нашего продукта как единую систему), получаем сведения о качестве ПО. 
* Приемочные испытания (альфа и бета тестирование).
* Эксплуатация и сопровождение. Тестирование багов, найденных в релизном продукте, регрессионное тестирование билда после внесенных исправлений (regression testing).

#### Виды тестирования
##### По методу тестирования
Мы работаем с кодом системы?
* НЕТ = метод «черного» ящика (black-box)
* Частично = метод «серого» ящика (grey-box)
* ДА = метод «белого» ящика (white-box)

##### По уровню (вширь)
* Компонентное/модульное (component/unit testing). Каждая сложная программная система состоит из отдельных частей – модулей, выполняющих ту или иную функцию в составе системы. Для того, чтобы удостовериться в корректной работе системы в целом, необходимо вначале протестировать каждый модуль системы по отдельности. 
* Интеграционное (integration testing). Результатом тестирования и верификации отдельных модулей, составляющих программную систему, является заключение о том, что эти модули являются внутренне непротиворечивыми и соответствуют требованиям. Однако отдельные модули редко функционируют сами по себе, поэтому следующая задача после тестирования отдельных модулей – тестирование корректности взаимодействия нескольких модулей, объединенных в единое целое. Такое тестирование называют интеграционным. Его цель – удостовериться в корректности совместной работы компонент системы.
* Системное (system testing). На этом этапе проводится не только функциональное тестирование, но и оценка характеристик качества системы – ее устойчивости, надежности, безопасности и производительности. На этом этапе выявляются многие проблемы внешних интерфейсов системы, связанные с неверным взаимодействием с другими системами, аппаратным обеспечением, неверным распределением памяти, отсутствием корректного освобождения ресурсов и т.п.

##### По уровню (вглубь)
* Приемочное (smoke test, acceptance testing) - проверка самой важной функциональности программного продукта.
* Тест критического пути (critical path test) – проверка функциональности, используемой типичными пользователями в повседневной деятельности.
* Расширенный тест (extended test) – проверка всей заявленной функциональности.

##### По цели
* Функциональное
  * Функциональное тестирование (functional testing)
  * Тестирование новой функциональности (new feature testing)
  * Тестирование безопасности (security testing)
 
* Нефункциональное
  * Производительности (performance testing) - определить, как быстро работает система или её часть под определённой нагрузкой:
    * нагрузочное (performance & load testing) - автоматизированное тестирование, которое имитирует одновременную работу множества пользователей над приложением;
    * стрессовое ( stress testing) позволяет проверить насколько приложение (система в целом) работоспособны в условиях стресса, и также оценить способность системы к регенерации (возвращение к нормальному состоянию после прекращения стресса);
    * тестирование стабильности / надежности (stability / reliability testing)  проверка работоспособности приложения при длительном (многочасовом) тестировании со средним уровнем нагрузки;
    * тестирование объемами (volume testing) оценить производительность при увеличении объемов данных в базах данных приложения.
  * Установочное (installation testing) направлено на проверку успешной инсталляции и настройки, а также обновления и удаления ПО.
  * Удобства пользования (usability testing) - тестирование, показывающее степень удобства использования, обучаемости, понятности и привлекательности для пользователя разрабатываемого ПО в контексте определенных условий.
  * Тестирование на отказ и восстановление (failover & recovery testing) проверяет продукт с точки зрения способности противостоять и успешно восстанавливаться после сбоев, возникших в связи с ошибками ПО, отказами оборудования или проблемами связи (например, отказ сети). 
  * Конфигурационное (configuration testing) - специальный вид тестирования, направленный на проверку работы программного обеспечения при различных конфигурациях системы (заявленных платформах, поддерживаемых драйверах, при различных конфигурациях компьютеров ...).
  * Интернационализации (internationalization testing) проверяет  готовность  приложения  к  работе  с разными языковвыми интерфейсами.
  * Локализационное (localization testing) проверяет, насколько корректно продукт адаптирован к работе на другом языке.
  * Тестирование документации (document testing) – тестирование, с которого начинается почти любой проект. Призвано  обнаружить  ошибки  в  документации на ранних стадиях.
  * Тестирование совместимости (compatibility testing) - тестирование, для проверки корректной работы продукта в определенном окружении.

* Связанное с изменениями
  * Дымовое тестирование (smoke testing) - короткий цикл тестов, чтобы убедиться, что после сборки кода (нового или исправленного) приложение стартует и выполняет основные функции.
  * Регрессионное тестирование (regression testing) - вид тестирования для подтверждения факта, что существующая ранее функциональность работает как и прежде после сделанных в приложении или окружающей среде исправлений или дополнений (починка дефекта, слияние кода, миграция на другую операционную систему, базу данных, веб сервер или сервер приложения).
  * Тестирование сборки (build verification testing) - тестирование выпущенной версии (сборки) по критериям качества для начала тестирования.
  * Проверка согласованности/исправности (sanity testing) - это узконаправленное тестирование, чтобы доказать, что конкретная функция работает согласно заявленным требованиям.

#### Верификация и валидация
Верификация (Verification) — это статическая практика проверки документов, дизайна, архитектуры, кода, т.д.  Отвечает на вопрос “Делаем ли мы продукт правильно?”.  
Валидация (validation) – это процесс оценки конечного продукта, необходимо проверить, соответствует ли программное обеспечение ожиданиям и требованиям клиента. Это динамический механизм проверки и тестирования фактического продукта. Отвечает на вопрос “Делаем ли мы правильный продукт?”.

#### Принципы тестирования
1. Тестирование показывает наличие дефектов. Тестирование может показать наличие дефектов в программе, но не доказать их отсутствие. Тем не менее, важно составлять тест-кейсы, которые будут находить как можно больше багов. Таким образом, при должном тестовом покрытии, тестирование позволяет снизить вероятность наличия дефектов в программном обеспечении. В то же время, даже если дефекты не были найдены в процессе тестирования, нельзя утверждать, что их нет.  
2. Исчерпывающее тестирование невозможно. Невозможно провести исчерпывающее тестирование, которое бы покрывало все комбинации пользовательского ввода и состояний системы, за исключениям совсем уж примитивных случаев. Вместо этого необходимо использовать анализ рисков и расстановку приоритетов, что позволит более эффективно распределять усилия по обеспечению качества ПО.  
3. Раннее тестирование. Тестирование должно начинаться как можно раньше в жизненном цикле разработки программного обеспечения, и его усилия  должны быть сконцентрированы на определенных целях.  
4. Скопление дефектов. Разные модули системы могут содержать разное количество дефектов – то есть, плотность скопления дефектов в разных элементах программы может отличаться. Усилия по тестированию должны распределяться пропорционально фактической плотности дефектов. В основном, большую часть критических дефектов находят в ограниченном количестве модулей. Это проявление принципа Парето: 80% проблем содержатся в 20% модулей.  
5. Парадокс пестицида. Прогоняя одни и те же тесты вновь и вновь, Вы столкнетесь с тем, что они находят все меньше новых ошибок. Поскольку система эволюционирует, многие из ранее найденных дефектов исправляют и старые тест-кейсы больше не срабатывают. Чтобы преодолеть этот парадокс, необходимо периодически вносить изменения в используемые наборы тестов, рецензировать и корректировать их с тем, чтобы они отвечали новому состоянию системы и позволяли находить как можно большее количество дефектов.  
6. Тестирование зависит от контекста. Выбор методологии, техники и типа тестирования будет напрямую зависеть от природы самой программы. Например, программное обеспечение для медицинских нужд требует гораздо более строгой и тщательной проверки, чем, скажем, компьютерная игра. Из тех же соображений, сайт с большой посещаемостью должен пройти через серьезное тестирование производительности, чтобы показать возможность работы в условиях высокой нагрузки.  
7. Заблуждение об отсутствии ошибок. Тот факт, что тестирование не обнаружило дефектов, еще не значит, что программа готова к релизу. Нахождение и исправление дефектов будут не важны, если система окажется неудобной в использовании, и не будет удовлетворять ожиданиям и потребностям пользователя.


To be updated


