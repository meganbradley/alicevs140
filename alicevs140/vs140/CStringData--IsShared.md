---
title: "CStringData::IsShared"
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
ms.assetid: b49b4741-cd54-4bab-aec0-fa1b9165d657
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::IsShared
Determines if the character buffer is shared.  
  
## Syntax  
  
```  
  
bool IsShared( ) const throw( );  
  
```  
  
## Return Value  
 Returns **true** if the buffer is shared; otherwise **false**.  
  
## Remarks  
 Call this function to determine if the character buffer of a string data object is currently shared among multiple string objects.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)