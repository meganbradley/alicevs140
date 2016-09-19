---
title: "DECLARE_WND_CLASS_EX"
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
ms.assetid: 0672c144-f2aa-4f6a-ae16-566e3a1f5411
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_WND_CLASS_EX
Allows you to specify the name of an existing window class on which a new window class will be based. Place this macro in an ATL ActiveX control's control class.  
  
## Syntax  
  
```  
  
      DECLARE_WND_CLASS_EX(   
   WndClassName,   
   style,   
   bkgnd    
)  
```  
  
#### Parameters  
 `WndClassName`  
 [in] The name of the new window class. If **NULL**, ATL will generate a window class name.  
  
 `style`  
 [in] The style of the window.  
  
 *bkgnd*  
 [in] The background color of the window.  
  
## Remarks  
 This macro allows you to specify the class parameters of a new window class, whose information will be managed by [CWndClassInfo](../vs140/CWndClassInfo-Class.md). `DECLARE_WND_CLASS_EX` defines the new window class by implementing the following static function:  
  
 [!CODE [NVC_ATL_Windowing#127](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#127)]  
  
 If you want to use the default styles and background color, use the [DECLARE_WND_CLASS](../vs140/DECLARE_WND_CLASS.md) macro. For more information about using windows in ATL, see the article [ATL Window Classes](../vs140/ATL-Window-Classes.md).  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Window Class Macros](../vs140/Window-Class-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_WND_SUPERCLASS](../vs140/DECLARE_WND_SUPERCLASS.md)