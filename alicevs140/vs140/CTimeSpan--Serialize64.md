---
title: "CTimeSpan::Serialize64"
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
ms.assetid: 3d552544-ebc0-483f-82b7-b992c02655a0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::Serialize64
> [!NOTE]
>  This method is only available in MFC projects.  
  
 Serializes the data associated with the member variable to or from an archive.  
  
## Syntax  
  
```  
CArchive& Serialize64(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 The `CArchive` object that you want to update.  
  
## Return Value  
 The updated `CArchive` object.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Serialization](../vs140/Serialization-in-MFC.md)