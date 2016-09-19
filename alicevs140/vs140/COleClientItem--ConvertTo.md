---
title: "COleClientItem::ConvertTo"
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
ms.assetid: 65d6dbd7-c8b4-4ea7-8d3d-402b3af1da55
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::ConvertTo
Call this member function to convert the item to the type specified by `clsidNew`.  
  
## Syntax  
  
```  
  
      virtual BOOL ConvertTo(  
   REFCLSID clsidNew   
);  
```  
  
#### Parameters  
 `clsidNew`  
 The class ID of the target type.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This is called automatically by [COleConvertDialog](../vs140/COleConvertDialog-Class.md). It is not necessary to call it directly.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::ActivateAs](../vs140/COleClientItem--ActivateAs.md)   
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)