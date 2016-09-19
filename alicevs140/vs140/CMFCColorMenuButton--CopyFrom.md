---
title: "CMFCColorMenuButton::CopyFrom"
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
ms.assetid: fc1dbe08-af72-4c9c-9001-938cade4052b
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::CopyFrom
Copies one [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)-derived object to another.  
  
## Syntax  
  
```  
virtual void CopyFrom(  
   const CMFCToolBarButton& src   
);  
```  
  
#### Parameters  
 [in] `src`  
 Source button to copy.  
  
## Remarks  
 Override this method to copy objects that are derived from the `CMFCColorMenuButton` object.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)