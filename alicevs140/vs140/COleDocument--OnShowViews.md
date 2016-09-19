---
title: "COleDocument::OnShowViews"
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
ms.assetid: 500f1e6d-c14b-4536-bcb4-a87b8e9eaf0b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnShowViews
The framework calls this function after the document's visibility state changes.  
  
## Syntax  
  
```  
  
      virtual void OnShowViews(  
   BOOL bVisible   
);  
```  
  
#### Parameters  
 `bVisible`  
 Indicates whether the document has become visible or invisible.  
  
## Remarks  
 The default version of this function does nothing. Override it if your application must perform any special processing when the document's visibility changes.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)