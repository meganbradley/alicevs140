---
title: "CDC::SetTextCharacterExtra"
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
ms.assetid: 0bc765bf-f160-4001-9de6-a301193ace8d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetTextCharacterExtra
Sets the amount of intercharacter spacing.  
  
## Syntax  
  
```  
  
      int SetTextCharacterExtra(  
   int nCharExtra   
);  
```  
  
#### Parameters  
 `nCharExtra`  
 Specifies the amount of extra space (in logical units) to be added to each character. If the current mapping mode is not `MM_TEXT`, `nCharExtra` is transformed and rounded to the nearest pixel.  
  
## Return Value  
 The amount of the previous intercharacter spacing.  
  
## Remarks  
 GDI adds this spacing to each character, including break characters, when it writes a line of text to the device context. The default value for the amount of intercharacter spacing is 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetTextCharacterExtra](../vs140/CDC--GetTextCharacterExtra.md)   
 [SetTextCharacterExtra](http://msdn.microsoft.com/library/windows/desktop/dd145092)