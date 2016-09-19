---
title: "COleControl::GetText"
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
ms.assetid: 585d8d5c-30bb-4361-9621-b8b5de63b3fa
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetText
Implements the Get function of the stock Text or Caption property.  
  
## Syntax  
  
```  
  
BSTR GetText( );  
```  
  
## Return Value  
 The current value of the control text string or a zero-length string if no string is present.  
  
> [!NOTE]
>  For more information on the `BSTR` data type, see [Data Types](../vs140/Data-Types--MFC-.md) in the Macros and Globals section.  
  
## Remarks  
 Note that the caller of this function must call `SysFreeString` on the string returned in order to free the resource. Within the implementation of the control, use `InternalGetText` to access the control's stock Text or Caption property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::InternalGetText](../vs140/COleControl--InternalGetText.md)   
 [COleControl::SetText](../vs140/COleControl--SetText.md)