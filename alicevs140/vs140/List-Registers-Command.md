---
title: "List Registers Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 19a9d789-f6c9-46b3-b1f6-4934fc33e055
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List Registers Command
Displays the value of the selected registers and lets you modify the list of registers to show.  
  
## Syntax  
  
```  
Debug.ListRegisters [/Display [{register|registerGroup}...]] [/List]  
[/Watch [{register|registerGroup}...]]  
[/Unwatch [{register|registerGroup}...]]  
```  
  
## Switches  
 /Display [{`register`&#124;`registerGroup`}...]  
 Displays the values of the specified `register` or `registerGroup`. If no `register` or `registerGroup` is specified, the default list of registers is displayed. If no switch is specified, the behavior is the same. For example:  
  
 `Debug.ListRegisters /Display eax`  
  
 is equivalent to  
  
 `Debug.ListRegisters eax`  
  
 /List  
 Displays all register groups in the list.  
  
 /Watch [{`register`&#124;`registerGroup`}...]  
 Adds one or more `register` or `registerGroup` values to the list.  
  
 /Unwatch [{`register`&#124;`registerGroup`}...]  
 Removes one or more `register` or `registerGroup` values from the list.  
  
## Remarks  
 The alias `r` can be used in place of `Debug.ListRegisters`.  
  
## Example  
 This example uses the `Debug.ListRegisters` alias `r` to display the values of the register group `Flags`.  
  
```  
r /Display Flags  
```  
  
## See Also  
 [Visual Studio Commands with Arguments](../vs140/Visual-Studio-Commands.md)   
 [Debugging Basics: Registers Window](../vs140/Debugging-Basics--Registers-Window.md)   
 [How to: Use the Registers Window](../vs140/How-to--Use-the-Registers-Window.md)