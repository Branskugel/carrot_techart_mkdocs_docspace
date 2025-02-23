# Шаблон проекта TP_KRD

>[!info]- Установленные плагины
>В данный шаблон предустановлены следующие плагины:
>
>* Carrot - v5.0
>* CarrotEditor - v5.0
>* CARROT_Tools - v0.001
>* SideFx_Labs - v20.0
>* RYM_Utilities - v1.26.6

### Установка

1. Скачиваем шаблон с SVN. Ссылка есть в телеграм канале или можно обратиться за ней к коллегам.
2. По завершении скачивания, запускаем .bat файл **install_template**. Нас встретит окно терминала с вопросом, хотим ли мы синхронизировать содержимое папок Source и Destination по указанным путям[^1]. Destination должен быть путём к папке шаблонов в директории установки движка соответствующей версии. ![[TP_KRD_prompt.png]]{style="border-radius: 5px"}
3. Отвечаем Y или Yes, если нас устраивают пути. N или No в противном случае.
4. Если путь Destination был корректен и вы согласились, шаблон должен быть установлен. Об успешности операции так же сигнализирует появление нового файла UE_template_update_log в папке с вашим исходником шаблона.
5. Запускаем движок с ярлыка или из лаунчера и дожидаемся открытия окна Unreal Projects Browser с выбором проектов.
6. Переходим во вкладку **Films / Video & Events** и создаём проект от нашего свежеустановленного шаблона. 

![[TP_KRD_UEProjectBrowser.png]]{style="border-radius: 5px"}

### Как пользоваться

####  Подготовка

![[TP_KRD_Outliner.png]]{style="border-radius: 5px"}



Объекты расположенные на уровне lvl_krd_studio не трогаем и не редактируем, на уровне lvl_RENAME - работаем.

$\quad$Источники света привязанные к пустышке EXAMPLE_StudioLights присутствуют исключительно для примера и чтобы в сцене не было темно при первом открытии проекта.


![[TP_KRD_LevelsLayers.png]]{style="border-radius: 5px"}

Уровень lvl_krd_studio заблокирован для предотвращения нежелательных изменений и загружен внутрь нашего рабочего уровня lvl_RENAME. Соответствующе названы слой для объектов будущей подводки и блюпринт-контроллер.

Все случаи, когда в проекте встречается слово RENAME - это знак, что нужно переименовать эту сущность в соответствии с назначением вашего проекта.

>[!example]- Пример
>Дана задача сделать подводку про хакеров
>
>* папка подводки RENAME ---> Hackers
>* слой RENAME ---> Hackers
>* уровень lvl_RENAME ---> lvl_Hackers
>* контроллер BP_RENAME_CTRL ---> BP_Hackers_CTRL
>* переменная слоя (Layer Name) в контроллере RENAME ---> Hackers
>
>![[TP_KRD_ControllerParams.png]]{style="border-radius: 5px"}
>  

С предупреждением возникающим во время переименования уровня можно просто согласиться.

#### Свет

Освещение настроено таким образом, что технический свет, расположенный на уровне lvl_kdr_studio соответствует тому, который будет на главном уровне куда подгрузят подводку инженеры. Технический свет работает на нулевом канале Light Channels. Ваши источники света <span style="color:red">не должны</span> его использовать, вместо этого используйте каналы 1 и 2. Объекты же могут размещаться на всех трёх каналах.

!!! example "Пример"

    === "Ваши Объекты"
    
        ![[TP_KRD_Object_LightChannels.png]]
    
    === "Ваш свет"
    
        ![[TP_KRD_Lights_LightChannels.png]]

#### Логика

В блюпринте уже реализована логика для скрытия и показа сцены по слою, поэтому вам остаётся только дописать свою логику для запуска и сброса анимации, если таковая необходима и подключить к соответствующим эвентам. При необходимости можете добавить свои дополнительные эвенты.

![[TP_KRD_ControllerEventgraph.png]]{style="border-radius: 5px"}

Название слоя, конечно же, надо будет вписать в переменную то, на которое вы его поменяли.

#### Сдача

Мигрируем уровень своей подводки, предварительно удаляя из него (не ассет!) уровень со студией. Галочки указывающие на папки движка или плагинов можно снять, с лишних папок тоже, если уверены, что у вас нет зависимостей на них.


[^1]: Пути должны быть строго на английском языке, чтобы батник сработал корректно