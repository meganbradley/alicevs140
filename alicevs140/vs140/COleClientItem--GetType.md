---
title: "COleClientItem::GetType"
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
ms.assetid: 3490e459-2f06-4b0f-9595-47184705f48c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetType
Call this function to determine whether the OLE item is embedded or linked, or static.  
  
## Syntax  
  
```  
  
OLE_OBJTYPE GetType( ) const;  
```  
  
## Return Value  
 An unsigned integer with one of the following values:  
  
-   `OT_LINK` The OLE item is a link.  
  
-   `OT_EMBEDDED` The OLE item is embedded.  
  
-   `OT_STATIC` The OLE item is static, that is, it contains only presentation data, not native data, and thus cannot be edited.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetUserType](../vs140/COleClientItem--GetUserType.md)