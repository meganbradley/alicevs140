---
title: "COleClientItem::CanCreateLinkFromData"
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
ms.assetid: 823e6261-424e-40a2-b1cb-904da2305df7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CanCreateLinkFromData
Checks whether a container application can create a linked object from the given `COleDataObject` object.  
  
## Syntax  
  
```  
  
      static BOOL PASCAL CanCreateLinkFromData(  
   const COleDataObject* pDataObject   
);  
```  
  
#### Parameters  
 `pDataObject`  
 Pointer to the [COleDataObject](../vs140/COleDataObject-Class.md) object from which the OLE item is to be created.  
  
## Return Value  
 Nonzero if the container can create a linked object from the `COleDataObject` object.  
  
## Remarks  
 The `COleDataObject` class is used in data transfers for retrieving data in various formats from the Clipboard, through drag and drop, or from an embedded OLE item.  
  
 Containers can use this function to decide to enable or disable their Edit Paste Special and Edit Paste Link commands.  
  
 For more information, see the article [Data Objects and Data Sources (OLE)](../vs140/Data-Objects-and-Data-Sources--OLE-.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)