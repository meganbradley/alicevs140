---
title: "COleSafeArray::Destroy"
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
ms.assetid: 827e52d1-a670-4dbc-bf82-6fd586683522
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Destroy
Destroys an existing array descriptor and all the data in the array.  
  
## Syntax  
  
```  
  
void Destroy( );  
```  
  
## Remarks  
 If objects are stored in the array, each object is released. On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::DestroyData](../vs140/COleSafeArray--DestroyData.md)   
 [COleSafeArray::DestroyDescriptor](../vs140/COleSafeArray--DestroyDescriptor.md)