---
title: "CDC::GetKerningPairs"
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
ms.assetid: 11262555-8d96-4000-b689-9d8b165eedf3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetKerningPairs
Retrieves the character kerning pairs for the font that is currently selected in the specified device context.  
  
## Syntax  
  
```  
  
      int GetKerningPairs(  
   int nPairs,  
   LPKERNINGPAIR lpkrnpair   
) const;  
```  
  
#### Parameters  
 `nPairs`  
 Specifies the number of [KERNINGPAIR](http://msdn.microsoft.com/library/windows/desktop/dd145024) structures pointed to by `lpkrnpair`. The function will not copy more kerning pairs than specified by `nPairs`.  
  
 `lpkrnpair`  
 Points to an array of **KERNINGPAIR** structures that receive the kerning pairs when the function returns. This array must contain at least as many structures as specified by `nPairs`. If this parameter is **NULL**, the function returns the total number of kerning pairs for the font.  
  
## Return Value  
 Specifies the number of kerning pairs retrieved or the total number of kerning pairs in the font, if the function is successful. Zero is returned if the function fails or there are no kerning pairs for the font.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetKerningPairs](http://msdn.microsoft.com/library/windows/desktop/dd144895)   
 [KERNINGPAIR](http://msdn.microsoft.com/library/windows/desktop/dd145024)