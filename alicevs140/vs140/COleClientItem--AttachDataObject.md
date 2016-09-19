---
title: "COleClientItem::AttachDataObject"
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
ms.assetid: 23256df7-0cbc-4dca-a352-66d8c057df97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::AttachDataObject
Call this function to initialize a [COleDataObject](../vs140/COleDataObject-Class.md) for accessing the data in the OLE item.  
  
## Syntax  
  
```  
  
      void AttachDataObject(  
   COleDataObject& rDataObject   
) const;  
```  
  
#### Parameters  
 *rDataObject*  
 Reference to a `COleDataObject` object that will be initialized to allow access to the data in the OLE item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)