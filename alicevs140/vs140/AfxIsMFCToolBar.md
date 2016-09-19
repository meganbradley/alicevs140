---
title: "AfxIsMFCToolBar"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ecd0671-7dc1-4730-8b8b-552d63a61572
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxIsMFCToolBar
Determines whether the given window is a toolbar object.  
  
## Syntax  
  
```  
BOOL AFXAPI AfxIsMFCToolBar(  
   CWnd* pWnd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 A pointer to an object that is derived from `CWnd`.  
  
## Return Value  
 `TRUE` if the provided window is a toolbar object; otherwise `FALSE`.  
  
## Remarks  
 This method returns `TRUE` if `pWnd` derives from `CMFCToolBar`. This method is useful when you have to validate that a function or method parameter is a `CMFCToolBar` object.  
  
## Requirements  
 **Header:** afxpriv.h  
  
## See Also  
 [Macros, Global Functions, and Global Variables](../vs140/Macros--Global-Functions--and-Global-Variables.md)   
 [CWnd Class](../vs140/CWnd-Class.md)   
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)