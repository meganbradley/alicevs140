---
title: "COleServerDoc::ActivateDocObject"
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
ms.assetid: c8eb7edd-807c-4cc0-935b-6a7837bd7f25
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::ActivateDocObject
Activates the associated DocObject document.  
  
## Syntax  
  
```  
  
void ActivateDocObject( );  
  
```  
  
## Remarks  
 By default, `COleServerDoc` does not support Active documents (also referred to as DocObjects). To enable this support, see [GetDocObjectServer](../vs140/COleServerDoc--GetDocObjectServer.md) and class [CDocObjectServer](../vs140/CDocObjectServer-Class.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::IsDocObject](../vs140/COleServerDoc--IsDocObject.md)