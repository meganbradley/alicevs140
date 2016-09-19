---
title: "CAxWindow2T::Create"
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
ms.assetid: f101e366-755f-42ca-ad8d-b520b48e4d86
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAxWindow2T::Create
Creates a host window.  
  
## Syntax  
  
```  
  
      HWND Create(  
   HWND hWndParent,   
   _U_RECT rect = NULL,   
   LPCTSTR szWindowName = NULL,   
   DWORD dwStyle = 0,   
   DWORD dwExStyle = 0,  
   _U_MENUorID MenuOrID = 0U,   
   LPVOID lpCreateParam = NULL  
);  
```  
  
## Remarks  
 `CAxWindow2T::Create` calls [CWindow::Create](../vs140/CWindow--Create.md) with the `LPCTSTR` `lpstrWndClass` parameter set to the window class that provides control hosting (**AtlAxWinLic80**).  
  
 See `CWindow::Create` for a description of the parameters and return value.  
  
 **Note** If 0 is used as the value for the `MenuOrID` parameter, it must be specified as 0U (the default value) to avoid a compiler error.  
  
## Example  
 See [Hosting ActiveX Controls Using ATL AXHost](../vs140/Hosting-ActiveX-Controls-Using-ATL-AXHost.md) for a sample that uses `CAxWindow2T::Create`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CAxWindow2T Class](../vs140/CAxWindow2T-Class.md)