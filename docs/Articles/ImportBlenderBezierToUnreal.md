# Ипорт кривых Bezier из Blender в Unreal

### Инструкция


- Импортируем файл с расширением .csv, который [[ExportBlenderBezierToUnrealCSV|экспортировали]] с помощью аддона.
- Выбираем **BezierDataTable** в качестве шаблона импорта данных.

![[ImportBlenderBezierToUnreal_structs.png]]{style="border-radius: 5px"}

- Нажимаем Apply to All, на случай если импортируем несколько кривых за раз. Остальные параметры можно оставить по умолчанию
- Выбираем любой из трёх доступных блюпринтов и добавляем на сцену по одному экземпляру выбранного на кривую.
![[ImportBlenderBezierToUnreal_BPs.png]]{style="border-radius: 5px"}

### BP_ImportableSpline

Это "чистокровный" блюпринт, обновление данных из таблицы в нём производится вручную нажатием кнопки <mark style="color:hsl(0, 0%, 100%);background-color:hsl(192, 10%, 25%);border:1px;border-color:black;border-radius: 6px;padding: 3px;">Load Data Table</mark>, но это можно изменить на своё усмотрение.

### BP_ImportableSpline_cpp

Это блюпринт <span style=color:#ae00ff>c++</span> класса, в остальном ничем не отличается.

### BP_ImportableSpline_Custom_cpp

Это так же блюпринт <span style=color:#ae00ff>c++</span> класса, но использует кастомный класс SplineComponent и обновляется автоматически. Во избежание перезаписи пользовательских изменений, поле ассета Bezier Data Table рекомендуется очистить по окончанию работы или сразу после загрузки данных.




#cpp