# Лабораторные и практические работы по ЭБЦС

## Лабораторные и практические работы по Элементной базе цифровых систем (ЭБЦС), 6 семестр СПбГЭТУ "ЛЭТИ", 2022

# Структура репозитория

## Директория `Guideline`

В директории `Guideline` находятся методические указания к лабораторным, практическим работам и курсовой работе,
инструкции по работе с Quartus II и LMS Moodle,
а также скриншоты программной информации об используемых версиях "Quartus II" и "КОМПАС-3D" с приложением "КОМПАС-Электрик"
(для чертежа по ГОСТу в практической работе 2).

## Директории `Laboratory_work_n`

В директориях `Laboratory_work_n` находятся файлы, относящиеся к лабораторным работам по ЭБЦС:
проекты в Quartus II, расчёты, скриншоты, схемы, отчёты и иные материалы.
Всего 8 лабораторных работ.

В проект для Quartus II не загружаются следующие директории с файлами (смотреть файл `.gitignore`):

+ `db/` -- отвечает за локальную репрезентацию проекта (директория создаётся при открытии проекта);
+ `incremental_db/` -- отвечает за информацию о модификации проекта, используемую при быстрой рекомпиляции (создаётся при компиляции);
+ `output_files/` -- результат компиляции функциональной схемы (проекта), который в том числе содержит файлы .pof и .sof для загрузки на плату Cyclone II (создаётся при компиляции функциональной схемы);
+ `simulation/` -- результат функциональной или временной симуляции (создаётся при временной или функциональной симуляции);
+ `greybox_tmp/` -- сгенерированный выходной IP-файл (неизвестно, когда создаётся);
+ `.qsys_edit/` -- личные пользовательские настройки (скорее всего создаётся при задании каких-либо настроек).

Так как данные директории с файлами либо локальны, либо могут быть получены при повторной компиляции/симуляции исходных файлов,
они не загружаются в репозиторий.

Информация про значения этих директорий взята отсюда:

+ https://electronix.ru/forum/index.php?app=forums&module=forums&controller=topic&id=134438
+ https://electronics.stackexchange.com/questions/540153/what-does-database-do-in-quartus
+ https://marsohod.org/forum/5-altera-quartus-ii/924-ispolzovanie-quartus
+ https://www.intel.com/content/dam/www/programmable/us/en/pdfs/literature/hb/qts/qts_qii5v1.pdf

## Директории `Practice_work_n`

В директориях `Practice_work_n` находятся файлы, относящиеся к практическим работам по ЭБЦС.
Всего 2 практические работы.

В практической работе 1 функциональная схема по ГОСТу была построена от руки.

В практической работе 2 функциональная схема была построена в Quartus II,
принципиальная схема и список элементов по ГОСТу были построены в **КОМПАС-3D** версии **18.1.35** с приложением **КОМПАС-Электрик**.
Для открытия проекта в **КОМПАС-Электрик** нужно открыть **КОМПАС-3D** и перейти в *Приложения* --> *КОМПАС-Электрик* --> *Менеджер проектов*
(при условии, что вы подключили **КОМПАС-Электрик** к **КОМПАС-3D**).
В *Менеджере проектов* нужно открыть файл с расширением `*.kpj` (если вы уже имеете этот файл), либо создать новый.

Если вы используете файл `*.kpj` из директории `Practice_work_2\Stuff`, то желательно использовать **КОМПАС-3D** и **КОМПАС-Электрик** 18 версию и выше, так как иначе не откроется.
В директории `Practice_work_2\Stuff` лежат уже преобразованные в стандартные для **КОМПАС-3D** `*.cdw` чертёж и перечень элементов.

# Как добавить разрыв цепи (и название контакта)?

## Определяем место (в данном случае -- справа сверху)

![Инструкция, как вставить название контакта 1](./Laboratory_work_5/Other/how_to_add_contact_name/how_to_add_contact_name_1.png)

## Выделяем проводку и кликаем правой кнопокой мыши, чтобы открыть настройки, и выбираем `Properties`

![Инструкция, как вставить название контакта 2](./Laboratory_work_5/Other/how_to_add_contact_name/how_to_add_contact_name_2.png)

## Называем контакт, затем нажимаем `ОК` и закрываем

![Инструкция, как вставить название контакта 3](./Laboratory_work_5/Other/how_to_add_contact_name/how_to_add_contact_name_3.png)

## Готово

![Инструкция, как вставить название контакта 4](./Laboratory_work_5/Other/how_to_add_contact_name/how_to_add_contact_name_4.png)

# Что делать, если файл не компилируется и выдаёт такую ошибку?

![Инструкция, как изменить главный в проекте файл 1](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_01.png)

Ошибка при компиляции `Full Compilation was NOT successful...`.
Обратите внимание, что согласно ошибке пункт `Top-level Entity name` не определён.
Это значит, скорее всего, что такого файла нет, поэтому нужно сделать так, чтобы он стал **главным** в этом проекте.

Во-первых, определим, какой файл нам нужен.

![Инструкция, как изменить главный в проекте файл 2](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_02.png)

Во-вторых, заходим во вкладку **Hierarchy** и выбираем сущность проекта, как показано на картинке.

![Инструкция, как изменить главный в проекте файл 3](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_03.png)

В-третьих, нажимаем на него правой кнопокой и выбираем пункт **Settings...**.

![Инструкция, как изменить главный в проекте файл 4](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_04.png)

В-четвёртых, прописываем в поле **Top-level entity** имя нашего файла без расширения (обычно это `*.bdf` файл) и...

![Инструкция, как изменить главный в проекте файл 5](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_05.png)

...нажимаем **OK**.

![Инструкция, как изменить главный в проекте файл 6](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_06.png)

Пока что изменения не отразились. Далее просто компилируем проект...

![Инструкция, как изменить главный в проекте файл 7](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_07.png)

...и компиляция проходит успешно (если у вас нет иных ошибок и проблем)!

![Инструкция, как изменить главный в проекте файл 8](./Laboratory_work_6/Other/change_main_file_instr/lab_6_change_main_file_08.png)

# Как создать bsf-файл (файл, чтобы вставить какую-то схему в другую)?

![Инструкция, как создать bsf-файл 1](./Course_work/Other/cw_create_bsf_instr/cw_create_bsf_01.png)

![Инструкция, как создать bsf-файл 2](./Course_work/Other/cw_create_bsf_instr/cw_create_bsf_02.png)

![Инструкция, как создать bsf-файл 3](./Course_work/Other/cw_create_bsf_instr/cw_create_bsf_03.png)

![Инструкция, как создать bsf-файл 4](./Course_work/Other/cw_create_bsf_instr/cw_create_bsf_04.png)

![Инструкция, как создать bsf-файл 5](./Course_work/Other/cw_create_bsf_instr/cw_create_bsf_05.png)

# Последовательность изменения настроек в проекте, необходимая для загрузки на плату

В методических указаниях в директории `Guideline` есть указание, как это сделать, однако это сделано не в самом удобном виде.
Здесь я приведу скриншоты, иллюстрирующие, как изменить настройки для корректной загрузки.

Во-первых, нужно зайти из главного меню *либо* во вкладку **Device**, а затем в **Device and pin options...**,
*либо* во вкладку **Settings**, затем во вкладку **Device...**, и потом в **Device and pin options**.

1 -- либо **Device** --> **Device and pin options**

![Инструкция, как изменить настройки для загрузки на плату 1](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_01.png)

![Инструкция, как изменить настройки для загрузки на плату 2](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_02.png)

2 -- либо **Settings** --> **Device...** --> **Device and pin options**

![Инструкция, как изменить настройки для загрузки на плату 3](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_03.png)

![Инструкция, как изменить настройки для загрузки на плату 4](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_04.png)

![Инструкция, как изменить настройки для загрузки на плату 5](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_05.png)

В разделе `Configuraion` в секции `Use configuration device:` ставим `EPCS1`.

![Инструкция, как изменить настройки для загрузки на плату 6](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_06.png)

![Инструкция, как изменить настройки для загрузки на плату 7](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_07.png)

![Инструкция, как изменить настройки для загрузки на плату 8](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_08.png)

В разделе `Unused Pins` в секции `Reserve all unused pins:` ставим `As input tri-stated`.

![Инструкция, как изменить настройки для загрузки на плату 9](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_09.png)

![Инструкция, как изменить настройки для загрузки на плату 10](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_10.png)

![Инструкция, как изменить настройки для загрузки на плату 11](./Laboratory_work_6/Other/change_settings_for_loading_instr/lab_6_change_settings_for_loading_11.png)

Нажимаем `ОК` и выходим. Готово.

# Краткие сведения о плате

![Инструкция, как изменить настройки для загрузки на плату 1](./Laboratory_work_5/Other/plate_usage/lab_5_plate_usage_1.jpg)

![Инструкция, как изменить настройки для загрузки на плату 2](./Laboratory_work_5/Other/plate_usage/lab_5_plate_usage_2.jpg)

![Инструкция, как изменить настройки для загрузки на плату 3](./Laboratory_work_5/Other/plate_usage/lab_5_plate_usage_3.jpg)

# Лицензия

Этот проект находится под лицензией MIT. Дополнительная информация в файле `license.txt`.