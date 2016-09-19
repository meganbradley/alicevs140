---
title: "COleSafeArray::DestroyData"
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
ms.assetid: 6b7b330a-74a4-4746-8295-89f44f704d46
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::DestroyData
Destroys all the data in a safe array.  
  
## Syntax  
  
```  
  
void DestroyData( );  
```  
  
## Remarks  
 If objects are stored in the array, each object is released. On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::Destroy](../vs140/COleSafeArray--Destroy.md)   
 [COleSafeArray::DestroyDescriptor](../vs140/COleSafeArray--DestroyDescriptor.md)