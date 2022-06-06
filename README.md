# Распознание жестов
Основная цель проекта создать систему детекции и распознания двигательной активности человека.

В частном случае предлагется распознание жестов рук с помощью прикреплённых на них тензомерических датчиков. При растижении меняется сопротивление датчиков. Отношение сопротивления дефоримрованного датчика к баpовому является измеряемой величиной. По значениям этих отншений обучается ML модель.
---#---

В txt файлах данные с АЦП электронных блоков, к котороым подключаются датчики. К одному электронному блоку подключается максимум два датчика. Соответсвенно для измерения 5 датчиками (по одному на палец) необходимо 3 блока. Информация с каждого отдельного блока пишется в отдельный файл.

Информация в столбцах файла:
  Date - дата
  Time - время
  Data1 - значения с первого датчика
  Data2 - значения со второго датчика
  Gesture - информация о классе жеста. 1 - демострируется жет, который необходиом распознать, 0 - демострируется базовый жет (кулак)
  Биоткань - биоткань, на которую крепятся датчики
  Движение/Жест - название распознаваемого жеста
  Комментарии - комментарий к экперименту
 
 ## Данные в txt файлах
| Index_Middle.txt               |
||:----------------:|:---------------------:||
||Data1             | средний палец (Middle)||
||Data2             | указательный палец    || 
 
В файле Index_Middle.txt
  Data1 - средний палец (Middle)/n
  Data2 - указательный палец (Index)/n

В файле Ring_Little.txt
  Data1 - безымянный палец(Ring)
  Data2 - мизинец (Little)

Thumb.txt
  Data1 - большой палец (Thumb)
