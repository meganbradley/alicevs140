---
title: "COleSafeArray::Copy"
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
ms.assetid: 9367acf0-c2d1-43b0-96ac-d5c489c34c55
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Copy
Creates a copy of an existing safe array.  
  
## Syntax  
  
```  
  
      void Copy(  
   LPSAFEARRAY* ppsa   
);  
```  
  
#### Parameters  
 *ppsa*  
 Pointer to a location in which to return the new array descriptor.  
  
## Remarks  
 On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [SafeArrayCopy](assetId:///8f84d4f6-1852-4ad8-b174-f3fa37e5bbd6)