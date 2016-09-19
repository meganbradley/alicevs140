---
title: "CComSafeArray::GetLowerBound"
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
ms.assetid: 84c04dce-a8ff-4b64-99ce-4543fb3a3362
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::GetLowerBound
Returns the lower bound for a given dimension of the array.  
  
## Syntax  
  
```  
  
      LONG GetLowerBound(  
   UINT uDim = 0   
) const;  
```  
  
#### Parameters  
 `uDim`  
 The array dimension for which to get the lower bound. If omitted, the default is 0.  
  
## Return Value  
 Returns the lower bound.  
  
## Remarks  
 If the lower bound is 0, this indicates a C-like array whose first element is element number 0. In the event of an error, for example, an invalid dimension argument, this method calls `AtlThrow` with an HRESULT describing the error.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::GetCount](../vs140/CComSafeArray--GetCount.md)   
 [CComSafeArray::GetUpperBound](../vs140/CComSafeArray--GetUpperBound.md)   
 [CComSafeArray::GetDimensions](../vs140/CComSafeArray--GetDimensions.md)