---
title: "CComSafeArray::GetUpperBound"
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
ms.assetid: 4d8bc153-ce3b-473b-b6f6-4730fb1beb23
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::GetUpperBound
Returns the upper bound for any dimension of the array.  
  
## Syntax  
  
```  
  
      LONG GetUpperBound(  
   UINT uDim = 0   
) const;  
```  
  
#### Parameters  
 `uDim`  
 The array dimension for which to get the upper bound. If omitted, the default is 0.  
  
## Return Value  
 Returns the upper bound. This value is inclusive, the maximum valid index for this dimension.  
  
## Remarks  
 In the event of an error, for example, an invalid dimension argument, this method calls `AtlThrow` with an HRESULT describing the error.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::GetLowerBound](../vs140/CComSafeArray--GetLowerBound.md)   
 [CComSafeArray::GetCount](../vs140/CComSafeArray--GetCount.md)