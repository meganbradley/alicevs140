---
title: "IAtlStringMgr::GetNilString"
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
ms.assetid: 6278a62e-2183-4711-a5fb-82a4c0553bcd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAtlStringMgr::GetNilString
Returns a pointer to a string data structure for an empty string.  
  
## Syntax  
  
```  
  
CStringData* GetNilString( ) throw( );  
  
```  
  
## Return Value  
 A pointer to the `CStringData` object used to represent an empty string.  
  
## Remarks  
 Call this function to return a representation of an empty string.  
  
> [!NOTE]
>  When implementing a custom string manager, this function must never fail. You can ensure this by embedding an instance of **CNilStringData** in the string manager class, and return a pointer to that instance.  
  
> [!NOTE]
>  For usage examples, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [IAtlStringMgr Class](../vs140/IAtlStringMgr-Class.md)