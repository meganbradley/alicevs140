---
title: "COleDocument::OnEditLinks"
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
ms.assetid: 07911b28-066f-4d79-b830-dbe33c54928e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnEditLinks
Displays the OLE Edit/Links dialog box.  
  
## Syntax  
  
```  
  
afx_msg void OnEditLinks( );  
```  
  
## Remarks  
 `OnEditLinks` creates and launches a `COleLinksDialog` Links dialog box that allows the user to change the linked objects.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::OnUpdateEditLinksMenu](../vs140/COleDocument--OnUpdateEditLinksMenu.md)   
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)