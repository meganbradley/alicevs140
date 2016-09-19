---
title: "CComSafeArrayBound::CComSafeArrayBound"
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
ms.assetid: 4c5335ab-2b12-4258-9e9a-7585866eaa90
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::CComSafeArrayBound
The constructor.  
  
## Syntax  
  
```  
  
      CComSafeArrayBound(  
   ULONG ulCount = 0,  
   LONG lLowerBound = 0   
) throw( );  
```  
  
#### Parameters  
 `ulCount`  
 The number of elements in the array.  
  
 `lLowerBound`  
 The lower bound from which the array is numbered.  
  
## Remarks  
 If the array is to be accessed from a Visual C++ program, it is recommended that the lower bound be defined as 0. It may be preferable to use a different lower bound value if the array is to be used with other languages, such as Visual Basic.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)