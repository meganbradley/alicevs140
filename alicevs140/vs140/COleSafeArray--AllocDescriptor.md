---
title: "COleSafeArray::AllocDescriptor"
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
ms.assetid: e7583700-efec-45b3-bddf-2c9fa46291cf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::AllocDescriptor
Allocates memory for the descriptor of a safe array.  
  
## Syntax  
  
```  
  
      void AllocDescriptor(  
   DWORD dwDims   
);  
```  
  
#### Parameters  
 `dwDims`  
 Number of dimensions in the safe array.  
  
## Remarks  
 On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::AllocData](../vs140/COleSafeArray--AllocData.md)   
 [SafeArrayAllocDescriptor](assetId:///8fe5c802-cdc0-4e7a-9410-ba65f9a5140e)