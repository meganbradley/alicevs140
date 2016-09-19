---
title: "CCmdTarget::OnFinalRelease"
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
ms.assetid: 5fda8ada-5bd4-4c31-8c4f-c91016081744
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::OnFinalRelease
Called by the framework when the last OLE reference to or from the object is released.  
  
## Syntax  
  
```  
  
virtual void OnFinalRelease( );  
```  
  
## Remarks  
 Override this function to provide special handling for this situation. The default implementation deletes the object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem Class](../vs140/COleServerItem-Class.md)