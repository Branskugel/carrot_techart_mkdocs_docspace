# Вспомогашки

#RYM_Utilities

Панель с набором функций, часто применимых к объектам на сцене для их подготовки к передаче инженерам или решения рутинных задач и проблем. Каждая функция пробегает по компонентам выделенных акторов вне зависимости от их типа и меняет настройки, если таковые имеются.


![[WidgetPanel_GridPanel.png]]{style="border-radius: 5px"}


### Create Empty 
Быстрое создание иерархии объектов через привязку к пустышкам (Empty Actors)

![[WidgetPanel_GridPanel_CreateEmpty.png]]{style="border-radius: 5px"}


??? info "Дополнительные возможности"

	Если сначала кликнуть в виджете (сфокусировать анриал на нём), а потом по кнопке, то можно использовать клавиши модификаторы:
	
	 ++ctrl++  создать родительскую пустышку в центре между объектами
	 
	 ++shift++  в мировых координатах (приоритет ниже чем у ctrl)
	 
	 \+ ++alt++  без учёта текущей иерархии
	
	 ++ctrl+alt+shift++  [[CreateEmptyHierarchy|создать шаблонную иерархию]] с частичным учётом текущей иерархии

### No Collisions
Отключение коллизий.

![[WidgetPanel_GridPanel_NoCollisions.png]]{style="border-radius: 5px"}


### Static - Movable
Переключение свойства Mobility на соответствующую настройку. Удобно в ситуациях, когда нужно привязать много акторов с настройкой отличной от будущего родителя.

![[WidgetPanel_GridPanel_StaticMovable.png]]{style="border-radius: 5px"}

>[!info]- Дополнительные возможности
>Если сначала кликнуть в виджете (сфокусировать анриал на нём) а потом по кнопке, то можно использовать клавишу модификатор:
>
>++shift++ - назначит на Stationary, при клике на кнопку MOVABLE
### Set Light Channels
Переключает световые каналы на состояние, установленное под иконкой.

![[WidgetPanel_GridPanel_SetLightChannels.png]]{style="border-radius: 5px"}

### Shadows Off - Shadows On
Переключение свойств отбрасывания теней.

![[WidgetPanel_GridPanel_ShadowsToggler.png]]{style="border-radius: 5px"}

### Custom Stencil
Отключение и включение рендеринга маски стенсила, а также настройка на конкретное значение, установленное на слайдере.

![[WidgetPanel_GridPanel_CustomStencil.png]]{style="border-radius: 5px"}

### LODs Disabler

Отключает ЛОДы выбранных акторов, а при клике с зажатым Ctrl отключает (и удаляет если проставлены галочки) ЛОДы исходных ассетов используемых этими акторами.

![[WidgetPanel_GridPanel_LODsDisabler.png]]{style="border-radius: 5px"}


Имеет парную [[Scripted_Actions#Disable LODS For Selected Assets|функцию]]для работы напрямую с ассетами в контент-браузере.


### Hidden in Game

![[Helpers_HiddenInGame.png]]

Новый набор кнопок для управления свойством Hidden in Game. Пришёл в версии плагина `1.27.1`

Галочка отвечает за состояние, которое нужно применить к выделенным объектам. Так же используется для поиска объектов, которые нужно выделить. То есть, если установлено значение **Hidden In Game** ✅ то, по нажатию кнопки <mark style="color:hsl(0, 0%, 100%);background-color: #2b7dbc;border-radius: 6px;padding: 3px;">ВЫДЕЛИТЬ</mark> движок сообщит о количестве объектов с совпадающим значением свойства и предложит их выделить.

![[Helpers_FoundHidden.png]]