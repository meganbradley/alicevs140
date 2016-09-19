---
title: "COleControl::GetFont"
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
ms.assetid: c7cba46c-ae1a-4941-abd4-8ae24bda1e98
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetFont
Implements the Get function of the stock Font property.  
  
## Syntax  
  
```  
  
LPFONTDISP GetFont( );  
```  
  
## Return Value  
 A pointer to the font dispatch interface of the control's stock Font property.  
  
## Remarks  
 Note that the caller must release the object when finished. Within the implementation of the control, use `InternalGetFont` to access the control's stock Font object. For more information on using fonts in your control, see the article [ActiveX Controls: Using Fonts in an ActiveX Control](../vs140/MFC-ActiveX-Controls--Using-Fonts.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetFont](../vs140/COleControl--SetFont.md)   
 [COleControl::AmbientFont](../vs140/COleControl--AmbientFont.md)   
 [COleControl::InternalGetFont](../vs140/COleControl--InternalGetFont.md)