---
title: "CComSafeArrayBound::SetLowerBound"
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
ms.assetid: 98198291-c12d-4745-95cb-e74d9275f922
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::SetLowerBound
Call this method to set the lower bound.  
  
## Syntax  
  
```  
  
      LONG SetLowerBound(  
   LONG lLowerBound   
) throw( );  
```  
  
#### Parameters  
 `lLowerBound`  
 The lower bound.  
  
## Return Value  
 Returns the new lower bound of the `CComSafeArrayBound` object.  
  
## Remarks  
 If the array is to be accessed from a Visual C++ program, it is recommended that the lower bound be defined as 0. It may be preferable to use a different lower bound value if the array is to be used with other languages, such as Visual Basic.  
  
 The upper bound depends on the number of elements and the lower bound value. For example, if the lower bound is 0 and the number of elements is 10, the upper bound will automatically be set to 9.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)   
 [CComSafeArrayBound::GetUpperBound](../vs140/CComSafeArrayBound--GetUpperBound.md)   
 [CComSafeArrayBound::GetLowerBound](../vs140/CComSafeArrayBound--GetLowerBound.md)   
 [CComSafeArrayBound::SetCount](../vs140/CComSafeArrayBound--SetCount.md)