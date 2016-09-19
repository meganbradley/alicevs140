---
title: "DECLARE_WND_SUPERCLASS"
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
ms.assetid: 650337b6-4973-41e5-8c36-55f90327bdcd
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_WND_SUPERCLASS
Allows you to specify the parameters of a class. Place this macro in an ATL ActiveX control's control class.  
  
## Syntax  
  
```  
  
      DECLARE_WND_SUPERCLASS(   
   WndClassName,   
   OrigWndClassName    
)  
```  
  
#### Parameters  
 `WndClassName`  
 [in] The name of the window class that will superclass `OrigWndClassName`. If **NULL**, ATL will generate a window class name.  
  
 `OrigWndClassName`  
 [in] The name of an existing window class.  
  
## Remarks  
 This macro allows you to specify the name of a window class that will superclass an existing window class. [CWndClassInfo](../vs140/CWndClassInfo-Class.md) manages the information of the superclass.  
  
 `DECLARE_WND_SUPERCLASS` implements the following static function:  
  
 [!CODE [NVC_ATL_Windowing#127](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#127)]  
  
 By default, [CWindowImpl](../vs140/CWindowImpl-Class.md) uses the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro to create a window based on a new window class. By specifying the `DECLARE_WND_SUPERCLASS` macro in a `CWindowImpl`-derived class, the window class will be based on an existing class but will use your window procedure. This technique is called superclassing.  
  
 Besides using the `DECLARE_WND_CLASS` and `DECLARE_WND_SUPERCLASS` macros, you can override the [GetWndClassInfo](../vs140/CWindowImpl--GetWndClassInfo.md) function with your own implementation.  
  
 For more information about using windows in ATL, see the article [ATL Window Classes](../vs140/ATL-Window-Classes.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Window Class Macros](../vs140/Window-Class-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)