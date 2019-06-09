Климова Наталья

### Unicode

Unicode –это универсальный стандарт кодирования символов, объединивший практически все основные письменные языки. До появления универсальной кодировки, перенос файлов из одной операционной системы в другую представлял определенную трудность, так как разные системы могли использовать разные наборы кодировок. Часто возникали ситуации, когда при открытии документа, вместо текста отображались непонятные символы. Появление Юникода позволило справиться с этой проблемой. 

Сам стандарт состоит из двух частей: универсальный набор символов и семейство кодировок.  Универсальный набор символов (англ. UCS) представляет из себя таблицу соответствия символов их кодовому значению.  Сами символы делятся на группы по их принадлежности либо к какому-либо языку, либо к математическим символам, знакам пунктуации, специальным знакам. Сейчас таких групп 17 по 216 (65536) символа в каждом. 

Символы в стандарте Unicode могут быть представлены в виде: «U+xxxx», «U+xxxxx», «U+xxxxxx», где xxxxxx –это шестнадцатеричные символы. Символы имеющие надстрочные или подстрочные элементы являются составными и кодируются группой из нескольких кодов. Кроме того, Юникод поддерживает не только письменность слева на право, но и справа на лево, а также комбинированные тексты сочетающие и то и другое. 

Семейство кодировок (англ. UTF) отвечает за машинное представление кодов, то есть за количество бит которым закодирован символ. Семейство кодировок сейчас представлены несколькими формами-это «UTF-8», «UTF-16» и «UTF-32», а также несколько других получивших меньшее распространение.

UTF-8 – это формат кодирует символы последовательностью из двоичных блоков от1 до 6 байт. Если последовательность состоит только из 8 бит, то такая кодировка совпадает с ACSII. В других случаях первый байт содержит количество бит символа, закодированного в двоичной системе счисления.

###### Таблица1. Кодировка UTF-8

| Кол-во    байт | Первый    байт | Формат   кода                                    | Описание                                                     |
| :------------- | -------------- | ------------------------------------------------ | ------------------------------------------------------------ |
| 1              | -              | 0ааааааа                                         | Где «a» — это   код символа в кодировке ASCII                |
| 2              | 11             | 110xxxxx10xxxxxx                                 | Где   0 - бит   завершение кода размера,  10 – биты продолжения   кода, х- значащие биты |
| 3              | 111            | 1110xxxx10xxxxxх10xxxxxx                         |                                                              |
| 4              | 1111           | 11110xxx10xxxxxx10xxxxxx10xxxxxx                 |                                                              |
| 5              | 11111          | 111110xx10xxxxxx10xxxxxx10xxxxxx10xxxxxx         |                                                              |
| 6              | 111111         | 1111110x10xxxxxx10xxxxxx10xxxxxx10xxxxxx10xxxxxx |                                                              |

 

 

UTF-16 – формат кодировки символов двухбайтовыми словами. Для большинства языков мира 16 бит достаточно для кодирования всех используемых символов, если 16 бит оказывается недостаточно, то используются «суррогатные» кодировки, когда один символ кодируется 4 байтами. 

Если сравнить кодировки UTF-8 и UTF-16, то можно сделать следующие выводы:

1. Символы, закодированные с помощью UTF-8, занимают меньший объём и быстрее обрабатываются, только если использованы символы из таблицы ACSII.

2. Обе кодировки используют переменную длину кода.

3. Обе кодировки используют все пространство символов и конвертация между ними осуществляется без потери качества.

 

 

 

 

 

### Unicode

Unicode is a universal character encoding standard that combines almost all major written languages. Before the advent of universal encoding, transferring files from one operating system to another presented a certain difficulty, since different systems could use different sets of encodings. Often there were situations when, when opening a document, incomprehensible characters were displayed instead of text. The appearance of Unicode allowed to cope with this problem.

The standard itself consists of two parts: a universal set of characters and a family of encodings. A universal character set (English UCS) is a table of correspondence of characters to their code value. The characters themselves are divided into groups according to their affiliation, either to a particular language, or to mathematical symbols, punctuation, and special characters. Now there are 17 such groups by 216 (65536) characters in each.

Characters in the Unicode standard can be represented as: “U + xxxx”, “U + xxxxx”, “U + xxxxxx”, where xxxxxx are hexadecimal characters. Characters with superscripts or descenders are composite and are encoded by a group of several codes. In addition, Unicode supports not only writing from left to right, but also right to left, as well as combined texts combining both.

The family of encodings (English UTF) is responsible for the machine representation of codes, that is, for the number of bits in which the character is encoded. The family of encodings is now represented in several forms - it is "UTF-8", "UTF-16" and "UTF-32", as well as several others that are less common.

UTF-8 - this format encodes characters in a sequence of binary blocks from 1 to 6 bytes. If the sequence consists of only 8 bits, then this encoding is the same as ACSII. In other cases, the first byte contains the number of bits of the character encoded in the binary number system.

###### Table 1. UTF-8 Encoding

| Amount   byte | First    byte | Code format                                      | Description                                                  |
| ------------- | ------------- | ------------------------------------------------ | ------------------------------------------------------------ |
| 1             | -             | 0ааааааа                                         | Where "a" is an ASCII character code                         |
| 2             | 11            | 110xxxxx10xxxxxx                                 | Where   0 is the bit size code completion, 10 are code continuation bits,   x-significant bits |
| 3             | 111           | 1110xxxx10xxxxxх10xxxxxx                         |                                                              |
| 4             | 1111          | 11110xxx10xxxxxx10xxxxxx10xxxxxx                 |                                                              |
| 5             | 11111         | 111110xx10xxxxxx10xxxxxx10xxxxxx10xxxxxx         |                                                              |
| 6             | 111111        | 1111110x10xxxxxx10xxxxxx10xxxxxx10xxxxxx10xxxxxx |                                                              |

 

UTF-16 is a character encoding format using double-byte words. For most languages of the world, 16 bits is enough to encode all the characters used, if 16 bits are not enough, then surrogate encodings are used, when one character is encoded with 4 bytes.

If we compare the encodings UTF-8 and UTF-16, we can draw the following conclusions:

1. Characters encoded with UTF-8 take up less space and are processed faster only if the characters from the ACSII table are used.

2. Both encodings use variable code length.

3. Both encodings use the entire character space and conversion between them is carried out without loss of quality.