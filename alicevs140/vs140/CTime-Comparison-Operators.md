---
title: "CTime Comparison Operators"
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
ms.assetid: cbd8b0ff-4c44-4bdd-bcd3-f56d2586be77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime Comparison Operators
Comparison operators.  
  
## Syntax  
  
```  
  
      bool operator ==(  
   CTime time   
) const throw( );  
bool operator !=(  
   CTime time   
) const throw( );  
bool operator <(  
   CTime time   
) const throw( );  
bool operator >(  
   CTime time   
) const throw( );  
bool operator <=(  
   CTime time   
) const throw( );  
bool operator >=(  
   CTime time   
) const throw( );  
```  
  
#### Parameters  
 `time`  
 The `CTime` object to be compared.  
  
## Return Value  
 These operators compare two absolute times and return **true** if the condition is true; otherwise **false**.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#161](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#161)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)