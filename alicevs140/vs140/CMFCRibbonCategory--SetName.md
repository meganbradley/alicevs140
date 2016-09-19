---
title: "CMFCRibbonCategory::SetName"
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
ms.assetid: 13befb64-4919-4d94-9213-58c6fc512b33
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::SetName
Assigns a name and keytip to the ribbon category.  
  
## Syntax  
  
```  
void SetName(  
   LPCTSTR lpszName  
);  
```  
  
#### Parameters  
 [in] `lpszName`  
 The name and keytip of the ribbon category.  
  
## Remarks  
 To set the keytip for the ribbon category, append a newline escape sequence followed by the keytip characters to `lpszName`.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)