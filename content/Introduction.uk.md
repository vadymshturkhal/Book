# 1. Вступ

Постійне переосмислення своєї діяльності, навіть найпростішої, має супроводжувати інженера все його життя. Звичка записувати свої думки словами та відточувати формулювання дуже допомагає у цьому. Текст цей з'явився як мої уривчасті нотатки, написані в різні роки, які я накопичував і критично вичитував десятки разів. Часто, я не погоджувався з собою, перечитуючи уривок після того, як він полежить деякий час. Тому я доводив текст до того, поки сам не погоджувався з написаним після тривалих періодів витримки матеріалу. Своїм завданням я прийняв писати якомога коротше і неодноразово переписував великі фрагменти, знаходячи, що їх можна виразити коротше. Це дозволило брати участь у формуванні книги всім охочим із спільноти Метархія, швидко знаходити помилки та неточності завдяки читачам, а також багатьом просто зручніше сприймати у вигляді книги. Актуальну версію завжди можна знайти на https://github.com/HowProgrammingWorks/Book, вона доповнюватиметься постійно. Прошу надсилати запити на виправлення та доповнення до [issues](https://github.com/HowProgrammingWorks/Book/issues) англійською мовою, нові ідеї у [discussions](https://github.com/HowProgrammingWorks/Book/discussions) будь-якою мовою, а свої доповнення та виправлення оформляти у вигляді pull-request у репозиторій книги.

Програмування – це мистецтво та інженерія розв'язання задач за допомогою обчислювальної техніки. Інженерія, тому що воно покликане отримувати користь із знань, а мистецтво, тому що знаннями програмування на сучасному етапі розвитку, на жаль, не обмежується і змушене вдаватися до інтуїції та слабко осмисленого особистого досвіду. Завдання програміста не у знаходженні математично вірного рішення, а у відшуканні узагальненого механізму рішення, здатного нас приводити до знаходження прийнятного рішення за обмежений час у якомога більшому класі завдань. Іншими словами, у знаходженні абстрактного класу рішень. Не всі парадигми програмування припускають рішення покрокове, але фізична реалізація обчислювальної техніки та природа людського мислення передбачають покроковість. Складність у цьому, що ці дії далеко не завжди зводяться до машинних операцій і залучають зовнішню взаємодію з пристроями введення/виводу і датчиками, а через них, із зовнішнім світом і людиною. Ця обставина створює велику невизначеність, яка не дозволяє математично суворо довести правильність способу вирішення всіх завдань і, тим більше, суворо вивести таке рішення з аксіом, як це характерно для точних наук. Однак, окремі алгоритми можуть бути виведені аналітично, якщо вони зводяться до чистих функцій. Тобто, до функцій, які у будь-який момент для певного набору вхідних даних однозначно дають однаковий результат. Чиста функція не має історії (пам'яті або стану) і не звертається до зовнішніх пристроїв (які можуть мати такий стан), може звертатися тільки до інших чистих функцій. Від математики програмування успадкувало можливість шукати точні рішення аналітично, та й сама обчислювальна машина функціонує строго в рамках формального математичного апарату. Але процес написання програмного коду не завжди може бути зведений до формальних процедур, ми змушені приймати рішення в умовах великої невизначеності та конструювати програми інженерно. Програміст обмежений і часом розробки програми, тому ми зменшуємо невизначеність завдяки введенню конструктивних обмежень, які не є суворо виведеними із завдання і засновані на інтуїції та досвіді конкретного спеціаліста. Простіше кажучи, через відсутність оптимального алгоритму, програміст може вирішувати завдання будь-яким способом, який дає прийнятні результати за розумний час, і який може бути реалізований за такий час, поки завдання ще залишається актуальним. У таких умовах ми повинні брати до уваги не тільки міру наближення рішення до оптимального, а й знання програміста, володіння інструментарієм та інші наявні ресурси. Адже навіть доступ до знань вже готових програмних рішень обмежений авторським правом, правами володіння вихідним кодом та документацією, що відповідають ліцензійними обмеженнями, не тільки на програмні продукти, а й на книги, відео, статті, навчальні матеріали тощо. Все це суттєво ускладнює та уповільнює розвиток галузі, але згодом доступність знань незворотно зростає, вони просочуються у вільне ходіння в мережі через популяризаторів, ентузіастів та рух вільного програмного забезпечення.

## 1.1. Підходи до вивчення програмування

## 1.2. Приклади на мовах JavaScript, Python та C

## 1.3. Моделювання: абстракції та повторне використання

В основі будь-якого програмування лежить моделювання, тобто створення моделі розв'язання задачі або моделі об'єктів і процесів у пам'яті машини. Мови програмування надають синтаксиси для конструювання обмежень під час створення моделей. Будь-яка конструкція та структура, покликана розширити функціональність та введена в модель, призводить до додаткових обмежень. Підвищення рівня абстракції, навпаки, може знімати частину обмежень і зменшувати складність моделі і коду програми, що виражає цю модель. Ми постійно балансуємо між розширенням функцій і згортанням їх у більш узагальнену модель. Цей процес може та повинен бути багаторазово ітеративним.

Дивно, але людина здатна успішно вирішувати завдання, складність яких перевищує можливості її пам'яті та мислення, за допомогою побудови моделей та абстракцій. Точність цих моделей визначає їх користь для прийняття рішень та вироблення керуючих впливів. Модель завжди не точна і відображає лише малу частину реальності, одну чи кілька її сторін чи аспектів. Однак, в обмежених умовах використання, модель може бути невідмінною від реального об'єкта предметної області. Є фізичні, математичні, імітаційні та інші моделі, але нас цікавитимуть насамперед інформаційні та алгоритмічні моделі.

Абстракція, це спосіб узагальнення, що зводить безліч різних, але схожих між собою випадків до однієї моделі. Нас цікавлять абстракції даних та абстрактні алгоритми. Найпростіші приклади абстракції в алгоритмах, це цикли (ітераційне узагальнення) та функції (процедури та підпрограми). За допомогою циклу ми можемо описати багато ітерацій одним блоком команд, припускаючи його повторюваність кілька разів, з різними значеннями змінних. Функції також повторюються багато разів з різними аргументами. Приклади абстракції даних, це масиви, асоціативні масиви, списки, множини тощо. У застосунках абстракції потрібно поєднувати в рівні – шари абстракцій. Низькорівневі абстракції вбудовані у мову програмування (змінні, функції, масиви, події). Абстракції більш високого рівня містяться у програмних платформах, рантаймах, стандартних бібліотеках, та зовнішніх бібліотеках або їх можна побудувати самостійно із простих абстракцій. Абстракції так називаються тому, що вирішують абстрактні узагальнені завдання загального призначення, не пов'язані з предметною областю.

Побудова шарів абстракцій це чи не найважливіша задача програмування від успішного вирішення якої залежать такі характеристики програмного рішення, як гнучкість налаштування, простота модифікації, здатність до інтеграції з іншими системами та період життя рішення. Всі шари, які не прив'язані до предметної області та конкретних прикладних завдань, ми називатимемо системними. Над системними шарами програміст надбудовує прикладні шари, абстракція яких навпаки знижується, універсальність зменшується та конкретизується застосування, прив'язуючись до конкретних завдань.

Абстракції різних рівнів можуть бути як в одному адресному просторі (одному процесі або одному застосунку), так і в різних. Відокремити їх один від одного і здійснити взаємодію між ними можна за допомогою програмних інтерфейсів, модульності, компонентного підходу і просто зусиллям волі, уникаючи прямих викликів із середини одного програмного компонента в середину іншого, якщо мова програмування або платформа не дбають про запобігання такій можливості. Так слід чинити навіть усередині одного процесу, де можна було б звертатися до будь-яких функцій, компонентів та модулів з будь-яких інших, навіть якщо вони логічно відносяться до різних шарів. Причина цього в необхідності знизити пов'язаність шарів та програмних компонентів, забезпечивши їх взаємозамінність, повторне використання та роблячи можливою їх роздільну розробку. Одночасно потрібно підвищувати зв'язність усередині шарів, компонентів та модулів, що забезпечує зростання продуктивності коду, простоту його читання, розуміння та модифікації. Якщо ж нам вдасться уникати зв'язаності між різними рівнями абстракцій, і за допомогою декомпозиції домогтися того, щоб один модуль завжди міг бути повністю охоплений увагою одного інженера, процес розробки стає масштабованим, керованим і більш передбачуваним. Подібна ідея покладена в основу архітектури мікросервісів, але більш загальний принцип застосовується для будь-яких систем, і не важливо, чи це будуть незалежно запущені мікросервіси або модулі, запущені в одному процесі.

Слід зазначити, що чим краще система розподілена, тим краще вона централізована. Тому, як вирішення завдань у таких системах знаходяться на адекватних рівнях, де вже достатньо інформації для прийняття рішень, обробки та отримання результату, відсутня жорстка зв'язаність моделей різного рівня абстракції. При такому підході немає зайвих ескалацій завдання на верхні рівні, уникаються “перегріви” вузлів прийняття рішень, мінімізована передача даних і підвищена оперативна швидкодія.

## 1.4. Алгоритм, программа, синтаксис, мова

## 1.5. Декомпозиція та поділ відповідальності

## 1.6. Огляд спеціальності інженер-програміст

Навколо програмування, як і навколо будь-якої сфери своєї діяльності, людина встигла побудувати величезну кількість забобонів і омани. Найперше джерело проблеми, це термінологія, адже різні парадигми, мови та екосистеми насаджують свою термінологію, яка не тільки суперечить між собою, але і нелогічна навіть всередині окремої спільноти. Більше того, багато програмістів самоучки і одинаки, видумують самобутню, ні на що не схожу термінологію і концепції, дублюючи один одного. Ошаленілі маркетологи теж деструктивно впливають на ІТ галузь у цілому, на формування світогляду і термінології. Викручуючи очевидні речі, заплутуючи та ускладнюючи концепції, вони забезпечують невичерпну лавину проблем, на якій тільки і підтримується весь софтверний бізнес. Переманюючи користувачі і програмістів на свої технології, гіганти промисловості часто створюють дуже привабливі і правдоподібні концепції, що ведуть в підсумку до несумісності, війни стандартів і до явної залежності від постачальника програмної платформи. Угруповання, що захоплюють увагу людей, десятиліттями паразитують на їх увазі та бюджетах. Ведені гординею та марнославством, деякі розробники й самі розповсюджують сумнівні, а іноді й свідомо тупикові ідеї. Адже робити програмне забезпечення добре – зовсім не вигідно для виробника. Ситуація значно краща у сфері вільного ПЗ та відкритого коду, але децентралізовані ентузіасти надто роз'єднані, щоб ефективно протидіяти потужній пропаганді гігантів галузі.

Як тільки якась технологія або екосистема розвивається достатньо, щоб на ній можна було створювати хороші рішення, вона обов'язково застаріває або виробник припиняє її підтримку або стає занадто складною. На моїй пам'яті вже змінилося понад п'ять таких технологічних екосистем.

## 1.7. Огляд парадигм програмування

Математика розглядає програму, як функцію, яку можна декомпозувати (розділити) на більш прості функції так, щоб програма-функція була їх суперпозицією. Тобто, грубо кажучи, програма є складною формулою, перетворювачем даних, коли на вхід подаються умови завдання, а на виході ми отримуємо рішення. Не всякий програміст знайомий із цією точкою зору, хоч вона й не ідеальна, але корисна для переосмислення своєї діяльності. Більш поширена протилежна точка зору, яку легко одержати з практики програмування. Полягає вона в написанні програм виходячи з уявлення користувача, з малюнків екранів інтерфейсу користувача, і з інструментарію, мови, платформи і бібліотек. В результаті ми отримуємо не програму-функцію, а велику систему станів, в якій відбувається комбінаторний вибух переходів і поведінка якої непередбачувана навіть для автора, не те що для користувача. Але не можна відразу відкидати цей, здавалося б, жахливий підхід. У ньому є конструктивне зерно, і полягає воно в тому, що не всі програми можна за короткий термін реалізувати у функціональній парадигмі, як перетворювачі даних. Тим більше, що людська діяльність вся складається з кроків і зміни станів навколишніх предметів за принципом покрокових маніпуляцій ними, а уявити її у вигляді функцій було б досить неприродним для нашого мислення.

Набір базових ідей, використовуваних інженером для побудови моделей, абстракцій та програмних систем, називається парадигмою. У цьому розділі ми розглянемо деякі з них поверхнево, а далі у книзі буде спеціальний розділ з більш детальним обговоренням кожної парадигми. Існують мови, які підтримують одну парадигму, а є мультипарадигмові мови. Ми звернемо увагу на різні мови та відмінності реалізації парадигм у них.

Для людини природно уявлення про будь-яку дію, як про набір кроків або алгоритм, це імперативний підхід. Ці кроки можуть бути або лінійними або прийняттям рішення про перехід до іншого кроку плану, замість того, щоб виконувати дії послідовно. Прийняття рішення для машини це операція, порівняння, що веде до розгалуження алгоритму, що дає варіанти (зазвичай два). Події можна умовно поділити на внутрішні та зовнішні. У внутрішніх беруть участь лише процесор та пам'ять, дія виконується відразу, без очікування, і має певний результат, який доступний безпосередньо на наступному етапі алгоритму. Зовнішні дії - це звернення до зовнішніх пристроїв введення-виводу (мережа, диски, інші пристрої), і вони вимагають очікування реакції від пристрою, яка прийде за час, зазвичай невідомий заздалегідь. Ми надсилаємо керуючий сигнал периферійним пристроям про те, що їм потрібно щось зробити і передаємо їм потрібні для цього дані. Далі у нас знову є два варіанти, або чекати результату, і це буде називатися блокуючим режимом вводу-виведення або перейти до наступного кроку алгоритму, не чекаючи результату, і це буде неблокуючий ввід-вивід. Такий поділ спричинено значною різницею у тривалості внутрішніх та зовнішніх дій. Більшість зовнішніх дій пов'язані з фізичними операціями над зовнішнім середовищем. Наприклад, передача даних через бездротову або провідну мережу, запис або читання з фізичного носія, взаємодія з датчиком, реле або приводом. Такі операції часто мають не цифрову, а аналогову природу, тому потрібно додаткове перетворення даних, очікування перехідного процесу, очікування потрібного показання датчика або сигналу від пристрою і т.д. Пристрої введення-виводу часто мають свій контролер, в якому виконується окремий потік операцій, а взаємодія між центральним процесором та пристроями введення-виводу також вимагає узгодження, що займає час і може закінчитися невдало.