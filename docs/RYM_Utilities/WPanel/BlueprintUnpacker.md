# Распаковка блюпринтов

#RYM_Utilities

Инструмент предназначенный для разбивки любого актора по компонентам его составляющим, на акторов состоящих из одного компонента соответствующего типа.

![[WidgetPanel_BlueprintUnpacker.png]]{style="border-radius: 5px"}

Если активирована опция <mark style="color:hsl(0, 0%,100%);background-color:hsl(0, 0%, 25%);border-radius: 6px;padding: 3px;">УДАЛИТЬ ИСХОДНИКИ</mark>, операция удалит со сцены обрабатываемые акторы, в противном случае исходный объект будет скрыт.

??? example "Пример-сравнение"

	=== "Вьюпорт"
	
		=== "Было"
		
			![[BP_Unbaker_PreApply_Model.png]]{style="border-radius: 5px"}
		
		=== "Стало"
		
			![[BP_Unbaker_PostApply_Model.png]]{style="border-radius: 5px"}
			`Цвет иконок лампочек изменился в связи с пересозданием компонентов`
	
	=== "Аутлайнер"
    
    	=== "Было"
		  
			![[BP_Unbaker_PreApply_OutlinerTree.png]]{style="border-radius: 5px"}
		
		=== "Стало"
		
			![[BP_Unbaker_PostApply_OutlinerTree.png]]{style="border-radius: 5px"}
			
			`Галочка "УДАЛИТЬ ИСХОДНИКИ" отключена в данном примере, исходный объект просто скрыт`

