---
title: "CWnd::LoadDynamicLayoutResource"
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
ms.assetid: 663cc93d-770c-44a4-92a7-8cf2aa1fc589
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::LoadDynamicLayoutResource
Called by the framework to load dynamic layout information from the resource file.  
  
## Syntax  
  
```  
  
      BOOL LoadDynamicLayoutResource(  
    LPCTSTR lpszResourceName  
);  
```  
  
#### Parameters  
 `lpszResourceName`  
 The name of the resource that contains the desired dynamic layout information for this window.  
  
## Return Value  
 Nonzero if the function is successful. It is 0 if a failure occurs.  
  
## Remarks  
 Do not call this method directly.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)