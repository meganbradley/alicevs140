---
title: "COleClientItem::OnShowItem"
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
ms.assetid: 4c6fb989-9b52-437b-b404-90bb583f90cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnShowItem
Called by the framework to display the OLE item, making it totally visible during editing.  
  
## Syntax  
  
```  
  
virtual void OnShowItem( );  
```  
  
## Remarks  
 It is used when your container application supports links to embedded items (that is, if you have derived your document class from [COleLinkingDoc](../vs140/COleLinkingDoc-Class.md)). This function is called during in-place activation or when the OLE item is a link source and the user wants to edit it. The default implementation activates the first view on the container document. Override this function to scroll the document so that the OLE item is visible.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleLinkingDoc Class](../vs140/COleLinkingDoc-Class.md)