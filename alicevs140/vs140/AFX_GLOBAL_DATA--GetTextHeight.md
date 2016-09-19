---
title: "AFX_GLOBAL_DATA::GetTextHeight"
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
ms.topic: article
ms.assetid: 54488f47-2fa0-4d03-885c-f5fe8e00b31d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::GetTextHeight
Retrieves the height of text characters in the current font.  
  
## Syntax  
  
```  
int GetTextHeight(  
   BOOL bHorz = TRUE  
);  
```  
  
#### Parameters  
 [in] `bHorz`  
 `TRUE` to retrieve the height of characters when text runs horizontally; `FALSE` to retrieve the height of characters when text runs vertically. The default value is `TRUE`.  
  
## Return Value  
 The height of the current font, which is measured from its ascender to its descender.  
  
## Requirements  
 **Header:**  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)