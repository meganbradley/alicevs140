---
title: "CSimpleStringT::IsEmpty"
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
ms.assetid: 2792c6a4-fb52-4941-b9f8-3993d3979973
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::IsEmpty
Tests a `CSimpleStringT` object for the empty condition.  
  
## Syntax  
  
```  
  
bool IsEmpty( ) const throw( );  
  
```  
  
## Return Value  
 Returns **true** if the `CSimpleStringT` object has 0 length; otherwise **false**.  
  
## Remarks  
 Call this method to determine if the object contains an empty string.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::IsEmpty`.  
  
 [!CODE [NVC_ATLMFC_Utilities#84](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#84)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetLength](../vs140/CSimpleStringT--GetLength.md)