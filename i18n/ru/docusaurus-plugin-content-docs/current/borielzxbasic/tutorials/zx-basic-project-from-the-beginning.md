
# HOWTO: ZX Basic Project from the beginning

This page is dummy. Original is located <a href="https://docs.google.com/document/pub?id=1vUneCCC18oXLglzoRcJdrMDUSh7vaO_tGDjzjOc8IhU">here</a>.

UPDATE: Even though the Tutorial is not complete (and may never be); the end game was released.

You can grab it, and the source code, from http://www.worldofspectrum.org/infoseekid.cgi?id=0027713

## How to Write a Game in Boriel’s ZX Basic

### (Project from the very beginning!)

So, you think you’re a competent Sinclair Basic programmer, but feel that machine code on the humble speccy is still too much for you? Is there something you can do to get basic running faster?

Luckily the answer is yes. There are a few tools out there that will help you write machine code without actually having to write the machine code, and they are called compilers.

A compiler lets you write in what’s called a high level language (BASIC is an example of a high level language), and then translates that code (programmers say it compiles it) into machine code.

You can write in a cut-down, limited version of BASIC on the spectrum, and then get it to compile your code. If you want to do this, I’d recommend using Hisoft’s BASIC compiler. It’s definitely the best one out there for general use.

Вы можете писать на C, если знаете этот язык. Существует кросс-компилятор под названием z88dk, который был использован несколькими людьми для создания некоторых хороших игр.

Третий вариант - компилятор под названием "ZX Basic", написанный Хосе Родригесом (он же "Бориэль"). Он подумывает о смене названия, отчасти потому, что люди путают ZX Basic и Sinclair Basic, а отчасти потому, что он хочет распространить компилятор на другие компьютеры, кроме ZX Spectrum 48K.

Стоит отметить, что вы можете вообще отказаться от компиляторов и писать игры, используя отличные конструкторы аркадных игр Джонатана Колдуэлла, Shoot Em Up Designer (SEUD), Platform games Designer (PGD) и Arcade games Designer (AGD). Их можно рассматривать как игровые движки, которые требуют меньше программирования, подобно тому, как Quill, Graphics Adventure Creator (GAC) и Professional Adventure Writer (PAW) являются игровыми движками для текстовых приключений.

Поскольку это руководство предназначено для пользователей Sinclair Basic, а на дворе 2012 год, поэтому мы должны признать, что существуют средства кросс-компиляции, я попытаюсь полностью задокументировать проект, написанный полностью на ZX Basic. Выбранный проект - это простой клон Pac Man. Это не очень сложная игра для программирования, что должно означать, что за ней легко следить.

Хорошо. Хватит болтать. Давайте начнем с самой простой программы на Sinclair Basic:

``basic
10 PRINT "Hello world"
```

Как бы мы перевели это в ZX Basic, а затем в машинный код?

Ну, код ZX Basic может быть таким:

``basic
10 PRINT "Hello world"
```

Это будет легко, не так ли!? Смотрите - никаких различий! Это правда, что ZX Basic был написан с расчетом на то, чтобы быть достаточно совместимым с Sinclair Basic. Поэтому довольно много программ будут переведены на него лишь с небольшим количеством изменений. Иногда вообще без изменений.

Однако ZX Basic гораздо мощнее. Его также можно использовать как современную версию Basic, при этом многие элементы дизайна намеренно сделаны максимально похожими на FreeBasic (http://en.wikipedia.org/wiki/FreeBASIC, если вы хотите узнать об этом).

Для начала, номера строк необязательны, и фактически не имеют того же значения в ZX Basic, что и в Sinclair Basic. Наша программа может быть написана без:

``basic
PRINT "Hello world"
```

ZX Basic работает сверху вниз вашего базового кода, как и Sinclair Basic, но даже без нумерации строк. Если подумать, номера строк в zx basic служат для упорядочивания кода и для переходов с помощью goto, gosub и так далее. Если вы не переходите к строке кода, зачем ей нужен номер строки - особенно если мы можем использовать лучший редактор для перемещения кода. Если вы читаете это, то велика вероятность, что у вас на компьютере уже есть лучший текстовый редактор (возможно, даже если это просто блокнот).

 На самом деле, ZX Basic использует номера строк в качестве меток. Он не требует, чтобы они располагались по порядку. В ZX Basic было бы совершенно правильно иметь программу, которая читается как:

``basic
20 PRINT "Hello";
10 PRINT "World"
```

Sinclair Basic это не понравится - он попытается изменить порядок. ZX Basic просто плывет по течению - и он все равно будет работать сверху вниз, печатая "Hello World". Порядок номеров строк не имеет значения - и на самом деле, как мы увидим позже, лучше использовать более описательные метки.

Как же нам написать и скомпилировать ZX BASIC? Прежде всего, скачайте ZX Basic с сайта http://www.boriel.com/wiki/en/index.php/ZX_BASIC:Archive.

Вы должны загрузить последнюю версию. Вы также должны обязательно заглянуть на форумы на сайте Хосе boriel.com - это хорошее место, чтобы задать вопросы, когда вы застрянете. (Не если. Вы застрянете! Мы все застряли!)

Вы можете скомпилировать программу на zx basic из командной строки с помощью команды

zxb game.bas [Assumi

Переведено с помощью www.DeepL.com/Translator (бесплатная версия)
