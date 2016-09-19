---
title: "COleServerItem::OnHide"
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
ms.assetid: c325e9ef-b90a-4769-9743-de6eb1dc0366
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnHide
Called by the framework to hide the OLE item.  
  
## Syntax  
  
```  
  
virtual void OnHide( );  
```  
  
## Remarks  
 The default calls **COleServerDoc::OnShowDocument( FALSE )**. The function also notifies the container that the OLE item has been hidden. Override this function if you want to perform special processing when hiding an OLE item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::OnOpen](../vs140/COleServerItem--OnOpen.md)   
 [COleServerItem::OnShow](../vs140/COleServerItem--OnShow.md)   
 [COleServerDoc::OnShowDocument](../vs140/COleServerDoc--OnShowDocument.md)