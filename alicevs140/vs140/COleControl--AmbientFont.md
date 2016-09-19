---
title: "COleControl::AmbientFont"
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
ms.assetid: e8d9fa41-a153-454b-913a-44c8696c79a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientFont
Returns the value of the ambient Font property.  
  
## Syntax  
  
```  
  
LPFONTDISP AmbientFont( );  
```  
  
## Return Value  
 A pointer to the container's ambient Font dispatch interface. The default value is **NULL**. If the return is not equal to **NULL**, you are responsible for releasing the font by calling its [IUnknown::Release](http://msdn.microsoft.com/library/windows/desktop/ms682317) member function.  
  
## Remarks  
 The ambient Font property is defined by the container and available to all controls.Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetFont](../vs140/COleControl--GetFont.md)   
 [COleControl::SetFont](../vs140/COleControl--SetFont.md)