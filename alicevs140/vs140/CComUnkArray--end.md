---
title: "CComUnkArray::end"
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
ms.assetid: 6aef126a-581e-4d93-9187-1d4127c53b8c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComUnkArray::end
Returns a pointer to one past the last **IUnknown** pointer in the collection.  
  
## Syntax  
  
```  
  
IUnknown** end( );  
```  
  
## Return Value  
 A pointer to an **IUnknown** interface pointer.  
  
## Remarks  
 The `CComUnkArray` methods **begin** and **end** can be used to loop through all connection points, for example, when an event is fired.  
  
 [!CODE [NVC_ATL_COM#44](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#44)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComUnkArray Class](../vs140/CComUnkArray-Class.md)   
 [CComUnkArray::begin](../vs140/CComUnkArray--begin.md)   
 [CComDynamicUnkArray::end](../vs140/CComDynamicUnkArray--end.md)