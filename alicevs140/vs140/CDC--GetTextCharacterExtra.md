---
title: "CDC::GetTextCharacterExtra"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: ce1ef793-a738-4d3b-9ab3-53955885ab6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetTextCharacterExtra
Retrieves the current setting for the amount of intercharacter spacing.  
  
## Syntax  
  
```  
  
int GetTextCharacterExtra( ) const;  
```  
  
## Return Value  
 The amount of the intercharacter spacing.  
  
## Remarks  
 GDI adds this spacing to each character, including break characters, when it writes a line of text to the device context.  
  
 The default value for the amount of intercharacter spacing is 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetTextCharacterExtra](../vs140/CDC--SetTextCharacterExtra.md)   
 [GetTextCharacterExtra](http://msdn.microsoft.com/library/windows/desktop/dd144933)