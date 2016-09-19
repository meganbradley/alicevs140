---
title: "CDC::SetDCBrushColor"
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
ms.assetid: 677688cd-c6dc-4e70-9056-2f235a561d9f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetDCBrushColor
Sets the current device context (DC) brush color to the specified color value.  
  
## Syntax  
  
```  
  
      COLORREF SetDCBrushColor(  
   COLORREF crColor  
);  
```  
  
#### Parameters  
 `crColor`  
 Specifies the new brush color.  
  
## Return Value  
 If the function succeeds, the return value specifies the previous DC brush color as a `COLORREF` value.  
  
 If the function fails, the return value is `CLR_INVALID`.  
  
## Remarks  
 This method emulates the functionality of the function [SetDCBrushColor](http://msdn.microsoft.com/library/windows/desktop/dd162969), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetDCBrushColor](../vs140/CDC--GetDCBrushColor.md)