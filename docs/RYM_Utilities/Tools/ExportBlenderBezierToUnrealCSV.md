# Экспортер кривых Bezier из Blender в Unreal

Аддон для #Blender Работоспособность проверялась на версии 4.3. 

<mark style="color:hsl(0, 0%, 100%);background-color:hsl(192, 49%, 45%);border-radius: 6px;padding: 3px;">Скачать</mark> можно на [гитхабе](https://github.com/Branskugel/BlenderBezierToUnrealCSV/releases/download/v.0.1/Blender_4.3_Export_BezierCSV_For_UE.zip)

Предназначен для сохранения кривых Bezier из блендера в формате CSV, для последующего импорта в Unreal инструментами плагина RYM_Utilities, такими как:
- BP_ImportableSpline
- BP_ImportableSpline_cpp
- BP_ImportableSpline_Custom_cpp

Подойдёт любой из трёх на выбор, однако у них есть небольшие отличительные черты.

Сам же аддон добавляет в меню экспорта блендера пункты

![[ExportBlenderBezierToUnrealCSV.png]]
{style="border-radius: 5px"} `поддерживается не только UE4, но и UE5`

Поддерживает:
1. Индвидуальный экспорт объектов кривых Bezier, даже если они состоят из нескольких не соединённых кривых
2. Батч-экспорт нескольких объектов кривых Bezier с тем же преимуществом что и в (1)
3. Произвольное наименование файлов по пользовательскому шаблону


??? success "Настройка именования файлов"

    === "Пользовательское"
    
        ![[ExportBlenderBezierToUnrealCSV_template_name.png]]{style="border-radius: 5px"}
    
    === "Объектное"
    
        ![[ExportBlenderBezierToUnrealCSV_obj_name.png]]{style="border-radius: 5px"}       


#AddOns
