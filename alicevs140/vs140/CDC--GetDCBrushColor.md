---
title: "CDC::GetDCBrushColor"
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
ms.assetid: 8ccc197c-611b-4ea0-a1cc-5dc083d00a55
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetDCBrushColor
Retrieves the current brush color.  
  
## Syntax  
  
```  
  
COLORREF GetDCBrushColor( ) const;  
  
```  
  
## Return Value  
 If the function succeeds, the return value is the [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value for the current brush color.  
  
 If the function fails, the return value is **CLR_INVALID**.  
  
## Remarks  
 This member function emulates the functionality of the function [GetDCBrushColor](http://msdn.microsoft.com/library/windows/desktop/dd144872), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetDCBrushColor](../vs140/CDC--SetDCBrushColor.md)