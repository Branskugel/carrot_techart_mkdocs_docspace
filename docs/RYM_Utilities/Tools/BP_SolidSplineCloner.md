# BP_SolidSplineCloner

#longread #RYM_Utilities


<h2 id="Parameters">Параметры</h2>

![[BP_SolidSplineCloner_InstancingParams.png]]{style="border-radius: 5px"}


###### Instancing Type

Тип объекта копируемого инструментом вдоль траектории сплайна

* **Static Mesh** - полноценно работает
* **Blueprint** - полноценно работает, использует Child Actor компоненты
* **Instanced Static Mesh** - не имплементировано
* **Hierarchical Instanced Static Mesh** - не имплементировано

###### Amount

Количество желаемых объектов. Рекомендуется резко это значение не дёргать, особенно если используете тяжёлые (геометрия, логика) объекты для копирования.

###### Fit Curve Length ✅

Переключает инструмент на вычисление количества, необходимого для заполнения длины кривой, с учётом их размеров и сдвигов относительно друг друга. <span style="color:red">Пользоваться осторожно</span>❗

###### Copy Default Settings

Настройки по умолчанию, используемые для новых копий. Подробнее в разделе [[#Параметры копий]]

###### Use Collision for Blueprint Length Calculation ✅

Переключает использование коллизий блюпринт-объектов для подсчёта их длины
Работа этого параметра может быть пересмотрена в будущем.

###### Prevent Creation Of Overlapping Extras ✅

Переключает механизм предотвращения создания пересекающихся избыточных копий. Работа этого параметра может быть пересмотрена в будущем.

###### Visualization

Раздел с настройками визуализации информации о копиях во вьюпорте. Подробнее в разделе [[#Отладка]]


<h3 id="copy-parameters">Параметры копий</h3>

Делятся на два раздела: **параметры по умолчанию** и [[BP_SolidSplineCloner#generated-instances-params|параметры сгенерированных копий]]

<h4 id="default-params">Параметры по умолчанию</h4>

![[BP_SolidSplineCloner_DefaultCopyParams.png]]{style="border-radius: 5px"}

###### Blueprint class

Класс, используемый копиями в случае, если свойство [[#Instancing Type]] установлено на значение **Blueprint**


###### Mesh

**Static Mesh** ассет, используемый копиями в случае, если свойство [[#Instancing Type]] установлено на значение **Static Mesh**


###### bPickObjectFromArray ✅


Переключает источник объекта (Mesh или Blueprint class) на array [[#Mesh Array]] или [[#Blueprints Array]] соответственно - вместо указанных в свойствах выше, объекты будут выбираться из этих списков.

###### PickObjectIndex

Индекс элемента из соответствующего списка объектов.


###### bPickRandomObject ✅

Переключает использование случайного индекса объекта из списка вместо параметра **PickObjectIndex**



###### bOverrideMaterials ✅

Переключает переназначение материалов объекта на те, что заданы в параметре **OverrideMaterials**


###### bUseOverlayMaterial ✅

Переключает переназначение материалов объекта на заданный в параметре **OverlayMaterial**


###### bPickOverlayMaterialFromArray ✅

Переключает переназначение материалов объекта на те, что заданы в параметре [[#Overlay Materials]]


###### PickOverlayMaterialIndex

Индекс **Overlay** материала из списка.


###### bPickRandomOverlayMaterial ✅

Переключает использование случайного индекса **Overlay** материала из списка вместо параметра **PickOverlayMaterialIndex**


###### bRandomizeSlotMaterials ✅

Переключает использование случайного индекса материала для слота из списка [[#PerSlotMaterialsArray]] вместо параметра **PickObjectIndex**


###### PerSlotMaterialsArray

По-слотовый список материалов для переназначения на объекте. Подробнее в разделе [[BP_SolidSplineCloner#working-with-materials|о работе с материалами]]




#TODO дописать



<h4 id="generated-instances-params">
Параметры сгенерированных копий
<a class="headerlink" href="#generated-instances-params" title="Permanent link">¶</a>
</h4>


![[BP_SolidSplineCloner_GeneratedInstances_Params_1.png]]{style="border-radius: 5px"}

#TODO дописать

<h3 id="working-with-materials">О работе с материалами</h3>

#TODO дописать



<h3 id="debugging">Отладка</h3>

#TODO дописать






