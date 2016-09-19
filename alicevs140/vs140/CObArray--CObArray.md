---
title: "CObArray::CObArray"
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
ms.assetid: 3e1ee3a7-e7b3-41ee-bb91-2699e3522a63
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::CObArray
Constructs an empty `CObject` pointer array.  
  
## Syntax  
  
```  
  
CObArray( );  
```  
  
## Remarks  
 The array grows one element at a time.  
  
 The following table shows other constructors that are similar to `CObArray::CObArray`.  
  
|Class|Constructor|  
|-----------|-----------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**CByteArray( );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**CDWordArray( );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**CPtrArray( );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**CStringArray( );**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**CUIntArray( );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**CWordArray( );**|  
  
## Example  
 [!CODE [NVC_MFCCollections#78](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#78)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::CObList](../vs140/CObList--CObList.md)