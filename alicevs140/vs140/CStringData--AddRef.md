---
title: "CStringData::AddRef"
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
ms.assetid: 7b77940a-866a-4977-a374-ceb48c2afae6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::AddRef
Increments the reference count of the string object.  
  
## Syntax  
  
```  
  
void AddRef( ) throw( );  
  
```  
  
## Remarks  
 Increments the reference count of the string object.  
  
> [!NOTE]
>  Do not call this method on a string with a negative reference count, since a negative count indicates that the string buffer is locked.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)