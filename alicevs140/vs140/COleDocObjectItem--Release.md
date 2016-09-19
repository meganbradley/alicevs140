---
title: "COleDocObjectItem::Release"
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
ms.assetid: af5c81d4-7e52-463c-b164-faf10052b277
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::Release
Releases the connection to an OLE linked item and closes it if it was open. Does not destroy the client item.  
  
## Syntax  
  
```  
  
      virtual void Release(  
   OLECLOSE dwCloseOption = OLECLOSE_NOSAVE  
);  
```  
  
#### Parameters  
 `dwCloseOption`  
 Flag specifying under what circumstances the OLE item is saved when it returns to the loaded state. For a list of possible values, see [COleClientItem::Close](../vs140/COleClientItem--Close.md).  
  
## Remarks  
 Does not destroy the client item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)