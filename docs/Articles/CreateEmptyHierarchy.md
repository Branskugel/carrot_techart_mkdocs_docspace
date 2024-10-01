# Организация сцены иерархией пустышек

#RYM_Utilities

Активация [[Helpers#Create Empty|инструмента Create Empty]] с зажатыми клавишами ++ctrl+alt+shift++ запускает функцию организации выделенных объектов в иерархию пустышек. Пользователь будет встречен окном подтверждения.

![[CreateEmptyHierarchy_Prompt.png]]{style="border-radius: 5px"}

**Cancel** - отменит операцию, **OK** приведёт к открытию следующего окна.

![[CreateEmptyHierarchy_NamePrompt.png]]{style="border-radius: 5px"}
 
 Здесь можно ввести произвольное название-заголовок для будущей иерархии. Если не ввести ничего, то операция будет отменена. После нажатия OK, выделенные объекты будут распределены по новым пустышкам, каждая из которых будет создана в центре мировых координат.

??? success "Пример иерархии"

    === "До"
    
        ![[Helpers_Before_EmptyHierarchy.png]]{style="border-radius: 5px"}
    
    === "После"
    
        ![[Helpers_After_EmptyHierarchy.png]]{style="border-radius: 5px"}
       