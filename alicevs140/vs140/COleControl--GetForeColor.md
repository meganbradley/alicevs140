---
title: "COleControl::GetForeColor"
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
ms.assetid: 260dff7c-0c03-48a0-86e8-b820ba8b954e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetForeColor
Implements the Get function of the stock ForeColor property.  
  
## Syntax  
  
```  
  
OLE_COLOR GetForeColor( );  
```  
  
## Return Value  
 The return value specifies the current foreground color as a **OLE_COLOR** value, if successful. This value can be translated to a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) value with a call to `TranslateColor`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientForeColor](../vs140/COleControl--AmbientForeColor.md)   
 [COleControl::TranslateColor](../vs140/COleControl--TranslateColor.md)   
 [COleControl::GetBackColor](../vs140/COleControl--GetBackColor.md)   
 [COleControl::SetForeColor](../vs140/COleControl--SetForeColor.md)