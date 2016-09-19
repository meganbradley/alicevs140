---
title: "COleSafeArray::Redim"
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
ms.assetid: 347f3df4-ba85-4269-bffb-165f6f40803b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Redim
Changes the least significant (rightmost) bound of a safe array.  
  
## Syntax  
  
```  
  
      void Redim(  
   SAFEARRAYBOUND* psaboundNew   
);  
```  
  
#### Parameters  
 *psaboundNew*  
 Pointer to a new safe array bound structure containing the new array bound. Only the least significant dimension of an array may be changed.  
  
## Remarks  
 On error, the function throws a [COleException](../vs140/COleException-Class.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::Create](../vs140/COleSafeArray--Create.md)   
 [COleSafeArray::GetDim](../vs140/COleSafeArray--GetDim.md)   
 [COleSafeArray::ResizeOneDim](../vs140/COleSafeArray--ResizeOneDim.md)