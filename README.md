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

# Лицензия

Этот проект находится под лицензией MIT. Дополнительная информация в файле `license.txt`.