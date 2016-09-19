---
title: "CAtlArray::RemoveAll"
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
ms.assetid: c6de79c9-5748-4ccd-a0c8-e4bd8b48025b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlArray::RemoveAll
Call this method to remove all elements from the array object.  
  
## Syntax  
  
```  
  
void RemoveAll( ) throw( );  
  
```  
  
## Remarks  
 Removes all of the elements from the array object.  
  
 This method calls [CAtlArray::SetCount](../vs140/CAtlArray--SetCount.md) to resize the array and subsequently frees any allocated memory.  
  
## Example  
 See the example for [CAtlArray::IsEmpty](../vs140/CAtlArray--IsEmpty.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlArray Class](../vs140/CAtlArray-Class.md)   
 [CAtlArray::RemoveAt](../vs140/CAtlArray--RemoveAt.md)   
 [CAtlArray::FreeExtra](../vs140/CAtlArray--FreeExtra.md)