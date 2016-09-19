---
title: "COleSafeArray::ResizeOneDim"
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
ms.assetid: 4c17b08a-c6b1-4ad4-af3a-937b84d116db
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::ResizeOneDim
Changes the number of elements in a one-dimensional `COleSafeArray` object.  
  
## Syntax  
  
```  
  
      void ResizeOneDim(  
   DWORD dwElements   
);  
```  
  
#### Parameters  
 `dwElements`  
 Number of elements in the one-dimensional safe array.  
  
## Remarks  
 On error, the function throws a [COleException](../vs140/COleException-Class.md).  
  
## Example  
 See the example for [COleSafeArray::CreateOneDim](../vs140/COleSafeArray--CreateOneDim.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::Redim](../vs140/COleSafeArray--Redim.md)   
 [COleSafeArray::GetOneDimSize](../vs140/COleSafeArray--GetOneDimSize.md)   
 [COleSafeArray::CreateOneDim](../vs140/COleSafeArray--CreateOneDim.md)