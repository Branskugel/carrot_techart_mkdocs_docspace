# SplineBaker

#RYM_Utilities

Это <span style=color:#ae00ff>c++</span> инструмент способный "запекать" данные сплайн-компонента в текстуру для дальнейшей "распаковки" этих данных в материале.

![[SplineBaker_PathsAndAssets.png]]{style="border-radius: 5px"}

```Unreal 

'/RYM_Utilities/Materials/Misc/SplineBakery/' | 'BP_RandomInstanceShaderGrid'

```

$\quad$Если вставить этот текст в строку поиска в панели Content Browser, то отобразятся все ассеты имеющие отношение к запеканию сплайна в текстуру и инстанцированию геометрии с учётом шейдерной расстановки.
### Категория Baking - запекание

* **Bake Spline Data to RT** - запечь превью сплайна. Так же выполняет ряд необходимых манипуляций и обязательна к использованию при каждом изменении сплайна перед сохранением запечки в текстуру.
* **Save Limits to MPC** - записывает в указанный ассет MaterialParameterCollection данные "ограничений" сплайна, необходимо для правильной распаковки в материале и обязательно к использованию при каждом изменении сплайна. 
* **Save RT to Texture Asset** - сохраняет превью Render Target в обыкновенную Texture2D по указанному пути.

![[SplineBaker_DetailsPanel.png]]{style="border-radius: 5px"}
### Категория Setup - Настройка запекания

##### Get Spline from Parent Actor
Назначить в поле Spline Actor актора родительского для этого экземпляра Spline Baker и найти у него Spline компонент. В общем-то кнопка говорящая сама за себя. 
##### Spline Actor
Собственно актор, чей spline компонент этот инструмент будет пытаться запечь.
##### Render Target
Своего рода превью, для быстрой оценки результата. С опытом использования придёт и понимание того, как текстура должна выглядеть и как не должна.
##### MPC Spline Limits
Любой ассет MaterialParameterCollection, у которого есть два скалярных параметра: **GridSizeX** и **GridSizeY**. А так же следующие <u>векторные</u> параметры:
  1. Pos_Limits_Min
  2. Pos_Limits_Max
  3. Tangent_limits_Min
  4. Tangent_limits_Max
  5. RightV_limits_Min
  6. RightV_limits_Max
  7. UpV_limits_Min
  8. UpV_limits_Max
  9. CustomRoll_limits_Min
  10. CustomRoll_limits_Max
  11. Scale_limits_Min
  12. Scale_limits_Max 
###### Texture Resolution
Разрешение текстуры. Для **X** берём просто степень двойки, для **Y** - 6, так как это равняется кол-во параметров ограничителей (выше) поделить на два.
  
  > [!warning] 
  > Большие значения **X** лучше работают при снятой в материале галочке Interframe Interpolation, возможно из-за ошибок в реализации. В противном случае появятся видимые задержки и проскальзывания.
  
* **Use "timed"  baking** - запекать данные сплайна используя time для их получения, вместо distance. Вряд ли пригодится, но может.
* **Texture Path** - путь и название будущего ассета текстуры. Если такого пути не существует, он будет создан. Слэш в начале не нужен. Путь относителен папки Content.
  
Подкатегория Debug носит чисто технический характер и возможно будет скрыта в будущем.

