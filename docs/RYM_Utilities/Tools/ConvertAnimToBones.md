# Костяная нога (Blender addon)

Аддон для #Blender 3.5+, работоспособность сохранена вплоть до версии 4.3. 

<mark style="color:hsl(0, 0%, 100%);background-color:hsl(192, 49%, 45%);border-radius: 6px;padding: 3px;">Скачать</mark> можно на [гитхабе](https://github.com/Branskugel/ObjectAnimToBones/releases/download/v.1.0.6/AnimConvertToBones_v1.0.6.zip)

Предназначен для запекания объектной анимации, в том числе rigid body симуляций, на скелетную. В процессе объекты будут автоматически привязаны к новым скелетам.


![[BlenderAddon_ConvertAnimToBones.png]]{style="border-radius: 5px"}

##### Join Objects
Объединит сетки объектов в один объект

##### Combine armatures
То же самое, но для скелетов

##### Baking frame step
Запекать каждый n-й кадр анимации

**Copy** параметры отвечают за то, какие трансформации объекта будут перенесены на кости.

Перед запеканием рекомендуется встать на наиболее нейтральный кадр, чтобы запекание прошло корректно и референсная (ref или же rest) поза была визуально адекватной и удобное для последующей работы.

#AddOns 