---
title: "CArray::Append"
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
ms.assetid: 6d596113-a5d2-4c29-9bd1-571a028ce162
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::Append
Call this member function to add the contents of one array to the end of another.  
  
## Syntax  
  
```  
  
      INT_PTR Append(  
   const CArray& src   
);  
```  
  
#### Parameters  
 *src*  
 Source of the elements to be appended to an array.  
  
## Return Value  
 The index of the first appended element.  
  
## Remarks  
 The arrays must be of the same type.  
  
 If necessary, **Append** may allocate extra memory to accommodate the elements appended to the array.  
  
## Example  
 [!CODE [NVC_MFCCollections#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#23)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::Copy](../vs140/CArray--Copy.md)