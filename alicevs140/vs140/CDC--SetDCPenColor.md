---
title: "CDC::SetDCPenColor"
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
ms.assetid: dfe9ea6b-ce7c-4b68-9260-f01f176b256d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetDCPenColor
Sets the current device context (DC) pen color to the specified color value.  
  
## Syntax  
  
```  
  
      COLORREF SetDCPenColor(  
   COLORREF crColor  
);  
```  
  
#### Parameters  
 `crColor`  
 Specifies the new pen color.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This member function utilizes the Win32 function [SetDCPenColor](http://msdn.microsoft.com/library/windows/desktop/dd162970), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetDCPenColor](../vs140/CDC--GetDCPenColor.md)