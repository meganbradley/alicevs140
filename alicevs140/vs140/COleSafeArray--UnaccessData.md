---
title: "COleSafeArray::UnaccessData"
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
ms.assetid: 4b7593c8-6631-4521-83fd-3a9572b758c5
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::UnaccessData
Decrements the lock count of an array and invalidates the pointer retrieved by `AccessData`.  
  
## Syntax  
  
```  
  
void UnaccessData( );  
```  
  
## Remarks  
 On error, the function throws a [COleException](../vs140/COleException-Class.md).  
  
## Example  
 See the example for [COleSafeArray::AccessData](../vs140/COleSafeArray--AccessData.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::AccessData](../vs140/COleSafeArray--AccessData.md)