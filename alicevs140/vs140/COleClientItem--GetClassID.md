---
title: "COleClientItem::GetClassID"
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
ms.assetid: 7995f51e-0623-4585-8263-d2acc04c2e08
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetClassID
Returns the class ID of the item into the memory pointed to by `pClassID`.  
  
## Syntax  
  
```  
  
      void GetClassID(  
   CLSID* pClassID   
) const;  
```  
  
#### Parameters  
 `pClassID`  
 Pointer to an identifier of type [CLSID](http://msdn.microsoft.com/library/windows/desktop/ms691424) to retrieve the class ID. For information on **CLSID**, see the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 The class ID is a 128-bit number that uniquely identifies the application that edits the item.  
  
 For more information, see [IPersist::GetClassID](http://msdn.microsoft.com/library/windows/desktop/ms688664) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)