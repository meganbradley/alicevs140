---
title: "DECLARE_WND_CLASS"
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
ms.assetid: 55247a72-fb9e-4bde-87f3-747c08076971
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_WND_CLASS
Allows you to specify the name of a new window class. Place this macro in an ATL ActiveX control's control class.  
  
## Syntax  
  
```  
  
      DECLARE_WND_CLASS(   
   WndClassName    
)  
```  
  
#### Parameters  
 `WndClassName`  
 [in] The name of the new window class. If **NULL**, ATL will generate a window class name.  
  
## Remarks  
 This macro allows you to specify the name of a new window class whose information will be managed by [CWndClassInfo](../vs140/CWndClassInfo-Class.md). `DECLARE_WND_CLASS` defines the new window class by implementing the following static function:  
  
 [!CODE [NVC_ATL_Windowing#127](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#127)]  
  
 `DECLARE_WND_CLASS` specifies the following styles for the new window:  
  
-   CS_HREDRAW  
  
-   CS_VREDRAW  
  
-   CS_DBLCLKS  
  
 `DECLARE_WND_CLASS` also specifies the default window's background color. Use the [DECLARE_WND_CLASS_EX](../vs140/DECLARE_WND_CLASS_EX.md) macro to provide your own styles and background color.  
  
 [CWindowImpl](../vs140/CWindowImpl-Class.md) uses the `DECLARE_WND_CLASS` macro to create a window based on a new window class. To override this behavior, use the [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md) macro, or provide your own implementation of the [GetWndClassInfo](../vs140/CWindowImpl--GetWndClassInfo.md) function.  
  
 For more information about using windows in ATL, see the article [ATL Window Classes](../vs140/ATL-Window-Classes.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Window Class Macros](../vs140/Window-Class-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)