---
title: "AFX_GLOBAL_DATA::RegisterWindowClass"
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
ms.topic: article
ms.assetid: 9d225f6b-2c3c-4bb8-8c0c-4cf568a643ba
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AFX_GLOBAL_DATA::RegisterWindowClass
Registers the specified MFC window class.  
  
## Syntax  
  
```  
CString RegisterWindowClass(  
   LPCTSTR lpszClassNamePrefix  
);  
```  
  
#### Parameters  
 [in] `lpszClassNamePrefix`  
 The name of the window class to register.  
  
## Return Value  
 The qualified name of the registered class if this method succeeds; otherwise, a [resource exception](../vs140/AfxThrowResourceException.md).  
  
## Remarks  
 The return value is a colon-delimited list of the `lpszClassNamePrefix` parameter string, and the hexadecimal text representations of the handles of the current application instance; the application cursor, which is the arrow cursor whose identifier is IDC_ARROW; and the background brush. For more information about registering MFC window classes, see [AfxRegisterClass](../vs140/AfxRegisterClass.md).  
  
## Requirements  
 **Header:** afxglobals.h  
  
## See Also  
 [AFX_GLOBAL_DATA Structure](../vs140/AFX_GLOBAL_DATA-Structure.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [AfxRegisterClass](../vs140/AfxRegisterClass.md)   
 [AfxThrowResourceException](../vs140/AfxThrowResourceException.md)