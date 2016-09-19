---
title: "CMap::SetAt"
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
ms.assetid: 84b3eb6e-3530-46a5-adf0-6217c5cad09f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::SetAt
The primary means to insert an element in a map.  
  
## Syntax  
  
```  
  
      void SetAt(  
   ARG_KEY key,  
   ARG_VALUE newValue   
);  
```  
  
#### Parameters  
 `ARG_KEY`  
 Template parameter specifying the type of the `key` parameter.  
  
 `key`  
 Specifies the key of the new element.  
  
 `ARG_VALUE`  
 Template parameter specifying the type of the `newValue` parameter.  
  
 `newValue`  
 Specifies the value of the new element.  
  
## Remarks  
 First, the key is looked up. If the key is found, then the corresponding value is changed; otherwise a new key-value pair is created.  
  
## Example  
 [!CODE [NVC_MFCCollections#62](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#62)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::Lookup](../vs140/CMap--Lookup.md)   
 [CMap::operator](../vs140/CMap--operator.md)