---
title: "_com_error::Error"
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
ms.topic: language-reference
ms.assetid: b53a15fd-198e-4276-afcd-13439c4807f7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_error::Error
**Microsoft Specific**  
  
 Retrieves the `HRESULT` passed to the constructor.  
  
## Syntax  
  
```  
  
HRESULT Error( ) const throw( );  
  
```  
  
## Return Value  
 Raw `HRESULT` item passed into the constructor.  
  
## Remarks  
 Retrieves the encapsulated `HRESULT` item in a `_com_error` object.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error Class](../vs140/_com_error-Class.md)