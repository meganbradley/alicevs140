---
title: "CTimeSpan::operator +=, -="
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
ms.assetid: ece7c677-ea62-4585-9a7c-e08a69e098db
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::operator +=, -=
Adds and subtracts a `CTimeSpan` object to and from this `CTimeSpan`.  
  
## Syntax  
  
```  
  
      CTimeSpan& operator +=(  
   CTimeSpan span   
) throw( );  
CTimeSpan& operator -=(  
   CTimeSpan span   
) throw( );  
```  
  
#### Parameters  
 `span`  
 The value to add to the `CTimeSpan` object.  
  
## Return Value  
 The updated `CTimeSpan` object.  
  
## Remarks  
 These operators allow you to add and subtract a `CTimeSpan` object to and from this `CTimeSpan`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#168](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#168)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)