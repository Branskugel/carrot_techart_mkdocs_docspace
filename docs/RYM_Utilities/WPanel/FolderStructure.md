# Создание структуры папок

#RYM_Utilities

Данная функция создаёт структуру папок, так же работает с уже существующими папками - заходит внутрь. Нажатие Enter когда курсор в поле для ввода адреса тоже активирует инструмент. Ожидаемый путь относителен папки Content.

!!! example "Формат пути"

	`НАЗВАНИЕ_ПАПКИ/НАЗВАНИЕ_ПОДПАПКИ`


![[WPanel_FolderStructure.png]]{style="border-radius: 5px"}

!!! important "Важно"

	Если просто нажать по кнопке создать, то указанные папки будут созданы прямо в папке Content, но если ввести какой-то путь или название родительской папки, то инструмент попробует его найти и создать папки там. Если таковой путь или папка не будут найдены, то они будут созданы.



!!! example "Пример"

	
	![[WidgetPanel_FolderStructure_Example.png]]{style="border-radius: 5px"}
	`Результат`