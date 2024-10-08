# MC_Pong

#RYM_Utilities

Компонент колебательных трансформаций. 
## Применение {: id="purpose"}

Добавляется к объекту для наделения его возможностью анимирования трансформаций по синусоиде.

>[!example]- Примеры
>
>Позиция, вращение, масштабирование
> 
><iframe src="https://giphy.com/embed/mWaLPeeQLPT3i" width="100" height="100" style="align=left" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
><iframe src="https://giphy.com/embed/3oz8xRQiRlaS1XwnPW" width="133" height="100" style="align=right" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
><iframe src="https://giphy.com/embed/l3vRlt8kty8KKeHni" width="100" height="100" style="" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
>
>Хорошо подходит для парящих объектов или "симуляции" покачивания лодки

## Инструкция {: id="how-to"}

1. Находим через поиск в контент браузере в корне проекта или папке плагина по названию. 
   `Если не находится, то включаем свойство Show Plugin Content`
2. Перетаскиваем в список компонентов актора, к которому хотим добавить и отпускаем
3. Настраиваем под свои нужды.

Ниже описание настроек.


## Параметры {: id="parameters"}


### Default

![[MC_Pong_Setup.png]]{style="border-radius: 5px"}

##### Initialize
Устанавливает мобильность объекта, к которому прикреплён компонент на Movable и выбирает целевой компонент для применения трансформаций. В случае если инструменту не удастся найти у актора компонент с именем заданным в **Component Name**, он выберет корневой (Root Component) компонент актора.

##### Component Name

Имя целевого компонента для применения трансформаций.

#### Advanced

##### Debug

Включить выведение на экран (и в лог) отладочных сообщений о привязке инструмента к компоненту.

### Анимация {: id="animation"}

![[MC_Pong_AnimParams.png]]{style="border-radius: 5px"}

##### Autoplay?

Активация автовключения анимации при старте игры.

##### Speed

Глобальный множитель частоты колебаний.

##### Cut Negative

Исключить отрицательные значения из диапазона амплитуды колебаний.

### Transforms

![[MC_Pong_TransformsParams.png]]{style="border-radius: 5px"}

* Location ✅ - активация колебаний по позиции
* Rotation ✅ - активация колебаний вращения
* Scale ✅ - активация колебаний размера


Следующие параметры все делятся по осям XYZ

##### Location, Rotation

* Frequency - частота колебаний
* Amplitude - амплитуда. множитель диапазона \[-1;1\] или \[0;1\] при включённом свойстве [[#Cut Negative]]
* Phase Offset - сдвиг фазы, для рассинхронизации колебаний между несколькими объектами

##### Scale

Амплитуда масштабирования работает несколько иначе.

* Min - Минимальный множитель размера, до которого проанимируется объект
* Max - Соответственно максимальный множитель