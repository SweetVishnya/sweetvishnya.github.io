---
title: Алексей Вишняков
---

<p style="text-align: right"><a href="/">English</a></p>

<div style="float: left; margin-right: 1em">
<img src="https://gravatar.com/avatar/991fda15b33321f67ba8e3647980ea62?s=200">
</div>

Привет!

Я закончил бакалавриат факультета [ВМК МГУ](https://cs.msu.ru/) на кафедре системного программирования в 2018 г. Получил магистерскую степень по направлению «компиляторные технологии» факультета [ВМК МГУ](https://cs.msu.ru/) в 2020 г. Я получил степень кандидата физико-математических наук в [Институте системного программирования им. В.П. Иванникова РАН](https://www.ispras.ru/) в 2022 г.

Я работаю старшим инженером DevSecOps в [Яндекс Облако](https://cloud.yandex.ru/).

Область научных интересов: компьютерная безопасность, жизненный цикл безопасной разработки (SDL), символьное выполнение, фаззинг, автоматическое обнаружение ошибок, возвратно-ориентированное программирование (ROP), динамический анализ, бинарный анализ, компиляторы и разработка инструментов для всего выше.

# Контакты

 * pmvishnya&nbsp;\<at\>&nbsp;gmail&nbsp;.&nbsp;com
 * GitHub: [SweetVishnya](https://github.com/SweetVishnya)
 * [ResearchGate](https://www.researchgate.net/profile/Alexey_Vishnyakov)
 * [Google Scholar](https://scholar.google.ru/citations?user=2FcTnyQAAAAJ)
 * [LinkedIn](https://www.linkedin.com/in/sweetvishnya/)
 * [Twitter](https://twitter.com/VishnyaSweet)
 * [Mastodon](https://infosec.exchange/@VishnyaSweet)
 * ResearcherID: [AAN-3944-2021](https://www.webofscience.com/wos/author/record/AAN-3944-2021)
 * Scopus Author ID: [57259933600](https://www.scopus.com/authid/detail.uri?authorId=57259933600)
 * ORCID: [0000-0003-1819-220X](https://orcid.org/0000-0003-1819-220X)
 * РИНЦ AuthorID: [1114229](https://www.elibrary.ru/author_items.asp?authorid=1114229)

# Публикации и доклады

[BibTeX](papers.bib)

## Numeric Truncation Security Predicate \[[видео](https://www.youtube.com/watch?v=oMpSgMFFiXc&t=18608s)\] \[[статья](https://arxiv.org/abs/2312.06425)\] \[[слайды](/mirror/mezhuev-ispopen2023.pdf)\]

Mezhuev T., Kobrin I., <u>Vishnyakov A.</u>, Kuts D. Numeric Truncation Security Predicate. 2023 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2023.

### Аннотация

Numeric truncation is a widely spread error in software written in languages with static data typing, such as C/C++ or Java. It occurs when the significant bits of the value with a bigger type size are truncated during value conversion to the smaller type. Utilizing one of the most powerful methods for path exploration and automated bug detection called dynamic symbolic execution (DSE), we propose the symbolic security predicate for numeric truncation error detection, developed on top of DSE tool Sydr. Firstly, we execute the program on the data, which does not lead to any errors. During program execution we update symbolic shadow stack and shadow registers to track symbolic sizes of the symbolic variables to avoid false positives. Then, if we meet the instruction, which truncates the symbolic variable, we build the security predicate, try to solve it with the SMT-solver and in case of success save new input file to reproduce the error. We tested our approach on Juliet Dynamic test suite for CWE-197 and achieved 100% accuracy. We approved the workability of our approach by detecting 12 new errors of numeric truncation in 5 different real-world open source projects within OSS-Sydr-Fuzz project. All of the errors were reported, most of the reports were equipped with appropriate fixes, successfully confirmed and applied by project maintainers.

## Фаззинг для SDL: выбрать, накрыть, раскопать \[[видео](https://youtu.be/ASZMRp8AoTQ?si=HW0q_TxtbMWCkuoH&t=1067)\] \[[слайды](https://offzone.moscow/upload/iblock/8ff/zkmuunr799jcdo41jf87h1lvx4y1f3o1.pdf)\]

Вартан Падарян, Владислав Степанов, <u>Алексей Вишняков</u>. Фаззинг для SDL: выбрать, накрыть, раскопать. OFFZONE 2023.

### Аннотация

Фаззинг-тестирование — одна из базовых технологий, применяемых при разработке безопасного ПО. Осмысленное и продуктивное применение фаззинга требует его глубокой интеграции в процессы разработки ПО и установления связей с другими технологиями: анализом поверхности атаки, функциональным тестированием, санитайзерами, автоматизированным разбором выявленных сбоев.

В докладе рассказывается как о самом движке фаззера, так и о вопросе выбора фаззинг‑целей. Динамический анализ помеченных данных, скрещенный с интроспекцией виртуальной машины, позволяет находить интерфейсы сложного ПО, через которые нарушитель в первую очередь будет атаковать ваше ПО, и в условиях ограниченных ресурсов расставлять приоритеты по порядку фаззинга. А гибридный фаззинг с динамическим символьным выполнением поможет быстро достичь хорошего покрытия кода и выявить ошибки, даже если они сразу не приводят к видимым сбоям в работе ПО

## CASR: ваш спасательный жилет в море крешей \[[видео](https://youtu.be/EgEeICZQD9M?si=hiFEwPmDqnh0cEq6)\] \[[слайды](https://offzone.moscow/upload/iblock/6cc/pujglwwoc8teeol03jwsuirfplm8e4dc.pdf)\]

Андрей Федотов, <u>Алексей Вишняков</u>. CASR: ваш спасательный жилет в море крешей. OFFZONE 2023.

### Аннотация

CASR — это фреймворк с открытым исходным кодом для анализа аварийных завершений, который создан для решения вызовов, возникающих после фаззинга при исследовании безопасности и разработке программного обеспечения. Он позволяет генерировать отчеты об аварийных завершениях, проводить их дедупликацию и кластеризацию, а также оценку критичности. Более того, CASR интегрирован с современными фаззерами, такими как AFL++, LibAFL и libFuzzer.

CASR поддерживает несколько архитектур (x86, ARM, RISC‑V), языков программирования (C/C++/Go/Rust/Python/Java) и включает в себя LibCASR для разработки пользовательских инструментов анализа. Также пользователю предлагается использовать casr‑dojo для экспорта аварийных завершений в систему управления уязвимостями DefectDojo. CASR является ценным инструментом для исследователей безопасности и разработчиков, которые сталкиваются с фаззингом и управлением уязвимостями.

Набор инструментов CASR реализует следующий пайплайн анализа аварийных завершений после фаззинга: создание отчетов об аварийных завершениях со всей необходимой информацией для ручного анализа, дедупликацию и кластеризацию аварийных завершений, создание отчетов UBSAN и выгрузку новых отчетов в систему управления уязвимостями DefectDojo

## Sydr-Fuzz: Continuous Hybrid Fuzzing and Dynamic Analysis for Security Development Lifecycle \[[статья](https://arxiv.org/abs/2211.11595)\] \[[видео](https://youtu.be/qw_tzzgX04E?t=16813)\] \[[слайды](/vishnyakov-isprasopen2022.pdf)\]

<u>Vishnyakov A.</u>, Kuts D., Logunova V., Parygina D., Kobrin E., Savidov G., Fedotov A. Sydr-Fuzz: Continuous Hybrid Fuzzing and Dynamic Analysis for Security Development Lifecycle. 2022 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2022, pp. 111-123. DOI: [10.1109/ISPRAS57371.2022.10076861](https://www.doi.org/10.1109/ISPRAS57371.2022.10076861)

### Аннотация

Nowadays automated dynamic analysis frameworks for continuous testing are in high demand to ensure software safety and satisfy the security development lifecycle (SDL) requirements. The security bug hunting efficiency of cutting-edge hybrid fuzzing techniques outperforms widely utilized coverage-guided fuzzing. We propose an enhanced dynamic analysis pipeline to leverage productivity of automated bug detection based on hybrid fuzzing. We implement the proposed pipeline in the continuous fuzzing toolset Sydr-Fuzz which is powered by hybrid fuzzing orchestrator, integrating our DSE tool Sydr with libFuzzer and AFL++. Sydr-Fuzz also incorporates security predicate checkers, crash triaging tool Casr, and utilities for corpus minimization and coverage gathering. The benchmarking of our hybrid fuzzer against alternative state-of-the-art solutions demonstrates its superiority over coverage-guided fuzzers while remaining on the same level with advanced hybrid fuzzers. Furthermore, we approve the relevance of our approach by discovering 85 new real-world software flaws within the OSS-Sydr-Fuzz project. Finally, we open Casr source code to the community to facilitate examination of the existing crashes.

## Исследование свойств алгоритма слайсинга предиката пути \[[статья](https://ispranproceedings.elpub.ru/jour/article/view/1528/1361)\]

<u>Вишняков А.В.</u> Исследование свойств алгоритма слайсинга предиката пути. Труды Института системного программирования РАН, том 34, вып. 3, 2022, стр. 7-12. DOI: [10.15514/ISPRAS-2022-34(3)-1](https://doi.org/10.15514/ISPRAS-2022-34(3)-1)

### Аннотация

Безопасный цикл разработки ПО (SDL) применяется для повышения надежности и защищенности программного обеспечения. В жизненный цикл программы добавляются этапы для проверки свойств ее безопасности. Среди прочего повсеместно применяется фаззинг-тестирование, которое позволяет обнаруживать аварийные завершения и зависания анализируемого кода. Гибридный подход, совмещающий в себе фаззинг и динамическую символьную интерпретацию, показал еще большую эффективность, чем классический фаззинг. Более того, символьная интерпретация позволяет добавлять дополнительные проверки, называемые предикатами безопасности, которые ищут ошибки работы с памятью и неопределенное поведение. Данная статья исследует свойства и характеристики алгоритма слайсинга предиката пути, который позволяет устранять избыточные ограничения из предиката пути без потери точности. В статье доказывается, что алгоритм конечен и не теряет решений. Более того, производится оценка асимптотической сложности алгоритма.

## Strong Optimistic Solving for Dynamic Symbolic Execution \[[статья](https://arxiv.org/abs/2209.03710)\] \[[видео](https://youtu.be/L7ZRV2Voee4?t=14710)\] \[[слайды](https://sydr-fuzz.github.io/papers/parygina-ivmem2022.pdf)\]

Parygina D., <u>Vishnyakov A.</u>, Fedotov A. Strong Optimistic Solving for Dynamic Symbolic Execution. 2022 Ivannikov Memorial Workshop (IVMEM), IEEE, 2022, pp. 43-53. DOI: [10.1109/IVMEM57067.2022.9983965](https://www.doi.org/10.1109/IVMEM57067.2022.9983965)

### Аннотация

Dynamic symbolic execution (DSE) is an effective method for automated program testing and bug detection. It is increasing the code coverage by the complex branches exploration during hybrid fuzzing. DSE tools invert the branches along some execution path and help fuzzer examine previously unavailable program parts. DSE often faces over- and underconstraint problems. The first one leads to significant analysis complication while the second one causes inaccurate symbolic execution.

We propose strong optimistic solving method that eliminates irrelevant path predicate constraints for target branch inversion. We eliminate such symbolic constraints that the target branch is not control dependent on. Moreover, we separately handle symbolic branches that have nested control transfer instructions that pass control beyond the parent branch scope, e.g. return, goto, break, etc. We implement the proposed method in our dynamic symbolic execution tool Sydr.

We evaluate the strong optimistic strategy, the optimistic strategy that contains only the last constraint negation, and their combination. The results show that the strategies combination helps increase either the code coverage or the average number of correctly inverted branches per one minute. It is optimal to apply both strategies together in contrast with other configurations.

## Поиск ошибок в бинарном коде методами динамической символьной интерпретации \[[статья](https://ispranproceedings.elpub.ru/jour/article/view/1512/1346)\] \[[слайды](/vishnyakov-mitsobi2022.pdf)\]

<u>Вишняков А.В.</u>, Кобрин И.А., Федотов А.Н. Поиск ошибок в бинарном коде методами динамической символьной интерпретации. Труды Института системного программирования РАН, том 34, вып. 2, 2022, стр. 25-42. DOI: [10.15514/ISPRAS-2022-34(2)-3](https://doi.org/10.15514/ISPRAS-2022-34(2)-3)

### Аннотация

Современное программное обеспечение стремительно развивается, принося новые ошибки, и все больше компаний следуют безопасному циклу разработки ПО. Одними из самых популярных средств для поддержки безопасного цикла разработки являются фаззинг и символьная интерпретация программ, позволяющие автоматически тестировать программу и искать в ней ошибки. Гибридный фаззинг — наиболее эффективный подход, который заключается в применении комбинации этих двух техник, при котором две техники работают совместно. Другим способом искать программные ошибки является символьная интерпретация с использованием предикатов безопасности — условий на входные данные, при выполнении которых будет проявлена ошибка. В этой работе мы предлагаем метод автоматизированного поиска ошибок с помощью динамической символьной интерпретации, совмещающий гибридный фаззинг с проверкой предикатов безопасности. Гибридный фаззинг требуется для получения большого количества различных входных данных, а ошибки работы с памятью и неопределенного поведения в программах ищут предикаты безопасности, которые позволяют находить ошибки деления на нуль, выхода за границы массива, целочисленного переполнения и другие. Результаты работы предикатов безопасности верифицируются с помощью санитайзеров, чтобы отбросить ложно положительные срабатывания. В результате практического применения предложенного метода к программам с открытым исходным кодом было найдено 11 различных новых ошибок в 5 разных проектах.

## Гибридный фаззинг фреймворка машинного обучения TensorFlow \[[слайды](/kobrin-mitsobi2022.pdf)\]

Кобрин И.А., <u>Вишняков А.В.</u>, Федотов А.Н. Гибридный фаззинг фреймворка машинного обучения TensorFlow. МиТСОБИ 2022.

## Symbolic Security Predicates: Hunt Program Weaknesses \[[статья](https://arxiv.org/abs/2111.05770)\] \[[видео](https://youtu.be/CI-Zioq5G84?t=6583)\] \[[слайды](/vishnyakov-isprasopen2021.pdf)\] \[[github](https://github.com/ispras/juliet-dynamic)\]

<u>Vishnyakov A.</u>, Logunova V., Kobrin E., Kuts D., Parygina D., Fedotov A. Symbolic Security Predicates: Hunt Program Weaknesses. 2021 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2021, pp. 76-85. DOI: [10.1109/ISPRAS53967.2021.00016](https://www.doi.org/10.1109/ISPRAS53967.2021.00016)

### Аннотация

Dynamic symbolic execution (DSE) is a powerful method for path exploration during hybrid fuzzing and automatic bug detection. We propose security predicates to effectively detect undefined behavior and memory access violation errors. Initially, we symbolically execute program on paths that don't trigger any errors (hybrid fuzzing may explore these paths). Then we construct a symbolic security predicate to verify some error condition. Thus, we may change the program data flow to entail null pointer dereference, division by zero, out-of-bounds access, or integer overflow weaknesses. Unlike static analysis, dynamic symbolic execution does not only report errors but also generates new input data to reproduce them. Furthermore, we introduce function semantics modeling for common C/C++ standard library functions. We aim to model the control flow inside a function with a single symbolic formula. This assists bug detection, speeds up path exploration, and overcomes overconstraints in path predicate. We implement the proposed techniques in our dynamic symbolic execution tool Sydr. Thus, we utilize powerful methods from Sydr such as path predicate slicing that eliminates irrelevant constraints.

We present Juliet Dynamic to measure dynamic bug detection tools accuracy. The testing system also verifies that generated inputs trigger sanitizers. We evaluate Sydr accuracy for 11 CWEs from Juliet test suite. Sydr shows 95.59% overall accuracy. We make Sydr evaluation artifacts publicly available to facilitate results reproducibility.

## MAJORCA: Multi-Architecture JOP and ROP Chain Assembler \[[статья](https://arxiv.org/abs/2111.05781)\] \[[видео](https://youtu.be/CI-Zioq5G84?t=11670)\] \[[слайды](/mirror/majorca_presentation.pdf)\] \[[github](https://github.com/ispras/rop-benchmark)\]

Nurmukhametov, A., <u>Vishnyakov, A.</u>, Logunova V., Kurmangaleev Sh. MAJORCA: Multi-Architecture JOP and ROP Chain Assembler. 2021 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2021, pp. 37-46. DOI: [10.1109/ISPRAS53967.2021.00011](https://www.doi.org/10.1109/ISPRAS53967.2021.00011)

### Аннотация

Nowadays, exploits often rely on a code-reuse approach. Short pieces of code called gadgets are chained together to execute some payload. Code-reuse attacks can exploit vulnerabilities in the presence of operating system protection that prohibits data memory execution. The ROP chain construction task is the code generation for the virtual machine defined by an exploited executable. It is crucial to understand how powerful ROP attacks can be. Such knowledge can be used to improve software security. We implement MAJORCA that generates ROP and JOP payloads in an architecture agnostic manner and thoroughly consider restricted symbols such as null bytes that terminate data copying via strcpy. The paper covers the whole code-reuse payloads construction pipeline: cataloging gadgets, chaining them in DAG, scheduling, linearizing to the ready-to-run payload. MAJORCA automatically generates both ROP and JOP payloads for x86 and MIPS. MAJORCA constructs payloads respecting restricted symbols both in gadget addresses and data. We evaluate MAJORCA performance and accuracy with rop-benchmark and compare it with open-source compilers. We show that MAJORCA outperforms open-source tools. We propose a ROP chaining metric and use it to estimate the probabilities of successful ROP chaining for different operating systems with MAJORCA as well as other ROP compilers to show that ROP chaining is still feasible. This metric can estimate the efficiency of OS defences.

## Обзор методов автоматизированной генерации эксплойтов повторного использования кода \[[статья](https://arxiv.org/abs/2011.07862)\] \[[github](https://github.com/ispras/rop-benchmark)\] \[[русская&nbsp;статья](https://ispras.ru/preprints/docs/prep_32_2019.pdf)\]

<u>Vishnyakov, A.V.</u> and Nurmukhametov, A.R., 2021. Survey of Methods for Automated Code-Reuse Exploit Generation. Programming and Computer Software 47(4), pp. 271-297. DOI: [10.1134/S0361768821040071](https://doi.org/10.1134/S0361768821040071)

### Аннотация

В работе приводится обзор существующих методов и инструментов автоматизированной генерации эксплойтов повторного использования кода. Такие эксплойты используют код, уже содержащийся в уязвимом приложении. Подход повторного использования кода позволяет эксплуатировать уязвимости программного обеспечения при наличии защитного механизма операционной системы, который запрещает исполнение кода страниц памяти, помеченных в качестве данных. В статье приводится описание различных методов повторного использования кода: атаки возврата в библиотеку, возвратно-ориентированного программирования, переходо-ориентированного программирования и других. Дается определение базовых понятий таких, как гаджет, фрейм гаджета, каталог гаджетов. Кроме того, показывается, что гаджет по своей сути является инструкцией, а их набор задает некоторую виртуальную машину. Задача создания эксплойта сводится к задаче генерации кода для такой виртуальной машины. Набор команд виртуальной машины задается исполняемым кодом конкретной программы. В работе приводится обзор методов поиска гаджетов и определения их семантики (формирования каталога гаджетов). Они позволяют получить набор команд виртуальной машины. Если набор гаджетов в каталоге полон по Тьюрингу, то гаджеты из каталога можно использовать в качестве набора команд целевой архитектуры компилятора. Однако в каталоге гаджетов для конкретного приложения могут отсутствовать некоторые инструкции, поэтому в литературе было предложено несколько способов для замены отсутствующих инструкций несколькими гаджетами. Связывание гаджетов в цепочки может происходить как поиском гаджетов по шаблонам, задаваемым регулярными выражениями, так и с учетом семантики гаджета. Более того, существуют подходы конструирования ROP цепочек с использованием генетических алгоритмов, а также методы с использованием SMT-решателей. В статье проводится сравнение инструментов с открытым исходным кодом. Мы предлагаем тестовую систему rop-benchmark, с помощью которой была проведена экспериментальная проверка работоспособности генерируемых инструментами цепочек на специально сформированном наборе тестов.

## Sydr: Cutting Edge Dynamic Symbolic Execution \[[статья](https://arxiv.org/abs/2011.09269)\] \[[видео](https://www.ispras.ru/conf/2020/video/compiler-technology-11-december.mp4#t=6021)\] \[[слайды](/vishnyakov-isprasopen2020.pdf)\] \[[github](https://github.com/ispras/sydr-benchmark)\] \[[демо](https://youtu.be/yznSawgD9D0)\]

<u>Vishnyakov A.</u>, Fedotov A., Kuts D., Novikov A., Parygina D., Kobrin E., Logunova V., Belecky P., Kurmangaleev Sh. Sydr: Cutting Edge Dynamic Symbolic Execution. 2020 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2020, pp. 46-54. DOI: [10.1109/ISPRAS51486.2020.00014](https://doi.org/10.1109/ISPRAS51486.2020.00014)

### Аннотация

The security development lifecycle (SDL) is becoming an industry standard. Dynamic symbolic execution (DSE) has enormous amount of applications in computer security (fuzzing, vulnerability discovery, reverse-engineering, etc.). We propose several performance and accuracy improvements for dynamic symbolic execution. Skipping non-symbolic instructions allows to build a path predicate 1.2--3.5 times faster. Symbolic engine simplifies formulas during symbolic execution. Path predicate slicing eliminates irrelevant conjuncts from solver queries. We handle each jump table (switch statement) as multiple branches and describe the method for symbolic execution of multi-threaded programs. The proposed solutions were implemented in Sydr tool. Sydr performs inversion of branches in path predicate. Sydr combines DynamoRIO dynamic binary instrumentation tool with Triton symbolic engine. We evaluated Sydr features on 64-bit Linux executables.

## Метод анализа атак повторного использования кода \[[препринт](/vishnyakov19-draft.pdf)\] \[[статья](https://link.springer.com/article/10.1134/S0361768819080061)\] \[[слайды](/vishnyakov-isprasopen2018.pdf)\] \[[русская&nbsp;статья](https://www.ispras.ru/proceedings/docs/2018/30/5/isp_30_2018_5_31.pdf)\] \[[видео](https://vimeo.com/298786113)\]

<u>Vishnyakov, A.V.</u>, Nurmukhametov, A.R., Kurmangaleev, S.F., and Gaisaryan S.S., 2019. A Method for Analyzing Code-Reuse Attacks. Programming and Computer Software 45(8), pp. 473-484. DOI: [10.1134/S0361768819080061](https://doi.org/10.1134/S0361768819080061)

### Аннотация

Обеспечение безопасности программного обеспечения является на сегодняшний день одной из первостепенных задач. Сбои в работе программного обеспечения могут привести к серьезным последствиям, а злонамеренная эксплуатация уязвимостей может причинить колоссальный ущерб. Крупные корпорации уделяют особое внимание анализу инцидентов информационной безопасности. Атаки повторного использования кода, основанные на возвратно-ориентированном программировании (ROP), приобретают всю большую популярность с каждым годом и могут быть применены даже в условиях работы защитных механизмов современных операционных систем. В отличие от обычного шелл-кода, где инструкции размещаются последовательно в памяти, ROP-цепочка состоит из множества маленьких блоков инструкций (гаджетов) и использует стек для связывания этих блоков, что затрудняет анализ ROP-эксплойтов. Целью данной работы является упрощение обратной инженерии ROP-эксплойтов. В этой статье предлагается метод анализа атак повторного использования кода, который позволяет восстановить семантику ROP-цепочки: разбить цепочку на гаджеты, определить семантику отдельных гаджетов и восстановить прототипы вызванных в ходе выполнения цепочки функций и системных вызовов и значения их аргументов. Семантика гаджета определяется его принадлежностью параметризованным типам. Каждый тип задается постусловием (булевым предикатом), которое должно быть всегда истинно после выполнения гаджета. Метод был реализован в виде программного инструмента и апробирован на реальных ROP-эксплойтах, найденных в интернете.

## Мелкогранулярная  рандомизация адресного  пространства  программы  при запуске \[[статья](https://link.springer.com/article/10.1134%2FS0361768818050080)\] \[[слайды](https://www.ispras.ru/conf/2017/pdf/Nurmukhametov.pdf)\] \[[русская&nbsp;статья](https://www.ispras.ru/proceedings/docs/2017/29/6/isp_29_2017_6_163.pdf)\] \[[русские&nbsp;слайды](/mirror/fine_grained_aslr.ru.pdf)\]

Nurmukhametov, A.R., Zhabotinskiy, E.A., Kurmangaleev, S.F., Gaissaryan, S.S., and <u>Vishnyakov, A.V.</u>, 2018. Fine-Grained Address Space Layout Randomization on Program Load. Programming and Computer Software, 44(5), pp. 363-370. DOI: [10.1134/S0361768818050080](https://doi.org/10.1134/S0361768818050080)

### Аннотация

Уязвимости программного обеспечения являются серьезной угрозой безопасности. Важной задачей является развитие методов противодействия их эксплуатации. Она приобретает особую актуальность с развитием ROP-атак. Имеющиеся средства защиты обладают некоторыми недостатками, которые могут быть использованы атакующими. В данной работе предлагается метод защиты от атак такого типа, который называется мелкогранулярной рандомизацией адресного пространства программы при запуске. Приводятся результаты по разработке и реализации данного метода на базе операционной системы CentOS 7. Рандомизацию на уровне перестановки функций осуществляет динамический загрузчик с помощью дополнительной информации, сохраненной с этапа статического связывания. Описываются детали реализации и приводятся результаты тестирования производительности, изменения времени запуска и размера файла. Отдельное внимание уделяется оценке эффективности противодействия эксплуатации с помощью ROP атак. Строятся две численных метрики: процент выживших гаджетов и оценка работоспособности примеров ROP цепочек. Приводимая в статье реализация применима в масштабах всей операционной системы и не имеет проблем совместимости с точки зрения работоспособности программ. По результатам проведенных работ была продемонстрирована работоспособность данного подхода на реальных примерах, обнаружены преимущества и недостатки и намечены пути дальнейшего развития.

## Классификация ROP гаджетов \[[статья](https://www.ispras.ru/proceedings/docs/2016/28/6/isp_28_2016_6_27.pdf)\] \[[слайды](/gadgets.pdf)\]

<u>Вишняков А.В.</u> Классификация ROP гаджетов. Труды Института системного программирования РАН. 2016;28(6):27-36. DOI: [10.15514/ISPRAS-2016-28(6)-2](https://doi.org/10.15514/ISPRAS-2016-28(6)-2)

### Аннотация

В данной работе предложен метод классификации ROP гаджетов, который позволяет аналитику сделать вывод о применимости техники ROP для эксплуатации уязвимостей в том или ином случае. Метод, реализованный в виде программного инструмента, применим к бинарным файлам программ. Работа инструмента продемонстрирована на 32-х и 64-х битных приложениях из дистрибутива Ubuntu 14.04, а возможность применения ROP на основе результатов классификации подтверждена на нескольких примерах.

## Оценка критичности программных дефектов в условиях работы современных защитных механизмов \[[статья](https://www.ispras.ru/proceedings/docs/2016/28/5/isp_28_2016_5_73.pdf)\]

Федотов А.Н., Падарян В.А., Каушан В.В., Курмангалеев Ш.Ф., <u>Вишняков А.В.</u>, Нурмухаметов А.Р. Оценка критичности программных дефектов в условиях работы современных защитных механизмов. Труды Института системного программирования РАН. 2016;28(5):73-92. DOI: [10.15514/ISPRAS-2016-28(5)-4](https://doi.org/10.15514/ISPRAS-2016-28(5)-4)

### Аннотация

В данной работе предложен уточненный метод автоматизированной оценки степени опасности найденных программных дефектов. На этапе тестирования промышленного программного обеспечения выявляется значительное число дефектов, приводящих к аварийному завершению. Из-за ограниченности ресурсов исправление дефектов растягивается во времени и требует расстановки приоритетов. Основным критерием для назначения высокого приоритета становится возможность использования ошибки в злонамеренных целях. На практике эта задача решается путем автоматизированного построения входных данных, подтверждающего наличие опасной уязвимости. Но в известных публикациях по данной теме не учитывают современные защитные механизмы, препятствующие действиям атакующего, что снижает качество вырабатываемых оценок. В данной статье рассматриваются современные защитные механизмы и дается оценка их распространенности и эффективности. Метод применим к бинарным файлам и не требует какой-либо отладочной информации. В основе метода лежит символьная интерпретация трасс выполнения, полученных при помощи полносистемного эмулятора. Даже в условиях одновременного функционирования DEP, ASLR и защиты стека («канарейка») метод способен демонстрировать возможность использования ошибок, сочетающих условия «write-what-where» и переполнение буфера на стеке. Возможности реализованного метода были продемонстрированы на модельных примерах и реальных программах.

# Тезисы

 * Кандидатская диссертация 2022 &mdash; Поиск ошибок в бинарном коде методами динамической символьной интерпретации \[[диссертация](/vishnyakov-phd-thesis2022.pdf)\] \[[автореферат](/vishnyakov-phd-synopsis2022.pdf)\] \[[слайды](/vishnyakov-phd-thesis2022-presentation.pdf)\]

 * Магистерская диссертация 2020 &mdash; Разработка и реализация метода генерации цепочек возвратно-ориентированного программирования \[[тезисы](/vishnyakov-master-thesis2020.pdf)\] \[[слайды](/vishnyakov-master-thesis2020-presentation.pdf)\]

 * Курсовая работа 2019 &mdash; Верификация семантики линейной последовательности машинных инструкций \[[тезисы](/vishnyakov-coursework2019.pdf)\] \[[слайды](/vishnyakov-coursework2019-presentation.pdf)\]

 * Выпускная квалификационная работа 2018 &mdash; Разработка и реализация метода анализа атак повторного использования кода \[[тезисы](/vishnyakov-diploma2018.pdf)\] \[[слайды](/vishnyakov-diploma2018-presentation.pdf)\]

 * Курсовая работа 2017 &mdash; Управляемое построение предиката пути при символьной интерпретации трасс бинарного кода \[[тезисы](/vishnyakov-coursework2017.pdf)\] \[[слайды](/vishnyakov-coursework2017-presentation.pdf)\]
