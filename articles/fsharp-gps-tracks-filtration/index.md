---
title: Фильтрация треков GPS на F#
id: fsharp-gps-tracks-filtration
excerpt: Фрагменты лекции, прочитанной в Московском клубе программистов 21 февраля 2019 года.
---

Несколько лет я изучаю функциональное программирование. Первый интерес к теме возник давно, но в конце восьмидеятых и начале девяностых типичная функциональная программа выполнялась слишком медленно на доступных тогда компьютерах.

В начале двухтысячных ситуация изменилась. В мир пришла Java, запускаемая на *виртуальной машине* с обязательной *сборкой мусора*. С 2003-го я перешёл на C#, форк Java от компании Microsoft. В 2-й версии языка появились *анонимные делегаты*&nbsp;&mdash; предтечи настоящих *лямбда-функций*.

В 2005-м я написал несколько программ на Ruby и был очарован красотой *замыканий*. В 2008-м вышла версия C# 3.5 с подъязыком запросов *LINQ*, *выводом типов* и *деревьями выражений*.

Стало трудно игнорировать функциональные элементы в массовых языках программирования. Сегодня вывод типов и лямбда-функции есть даже в C++.

С другой стороны, истинно функциональное программирование встречается всё ещё нечасто. Языки общего назначения остаются императивными и не требуют функционального подхода.

Для популяризации функциональных языков необходимы учебные материалы, понятные классическим программистам. К сожалению, подобных материалов не очень много. В качестве примеров мы видим вычисление факториалов или чисел Фибоначчи, которые вы вряд ли встречаете в реальной практике.

Я попробую продемонстрировать приёмы функциональной разработки на задаче фильтрации треков. Она действительно практическая&nbsp;&mdash; с одной стороны, а с другой&nbsp;&mdash; достаточно сложная. Эта задача способна пропродемонстрировать мощность функциональных средств.

Я работаю в стеке .NET, поэтому моим функциоанльным языком является F#. Предположу, что вы знаете C#, или знакомы с его ближайшими родственниками C++ или Java.

В этом цикле я буду рассказывать о тех проблемах, которые предстоит решить в рамках фильтрации треков. Постарайтесь продумать императивную реализацию, прежде чем посмотреть на реализацию F#. Возможно, вы будете приятно удивлены краткостью функциональных решений.

Мы не будет далеко уходить от стандартов промышленного программирования. Для каждой функции мы напишем необходимые *модульные тесты*, а в конце цикла встроим наше решение в реальный проект.

[Часть I: Удаление нулевых и отрицательных интервалов времени](1)

[Часть II: Устранение дрейфа нулевой скорости и всплесков скорости](2)

Часть III: Фильтр Калмана

ЧАсть IV: интеграция с C#, Azure и Xamarin