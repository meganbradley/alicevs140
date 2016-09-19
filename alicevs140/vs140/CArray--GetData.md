---
title: "CArray::GetData"
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
ms.assetid: 2bc7347a-943a-470f-81bd-6cb400572353
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::GetData
Use this member function to gain direct access to the elements in an array.  
  
## Syntax  
  
```  
  
      const   
      TYPE  
      * GetData( ) const;  
TYPE* GetData( );  
```  
  
#### Parameters  
 *TYPE*  
 Template parameter specifying the type of the array elements.  
  
## Return Value  
 A pointer to an array element.  
  
## Remarks  
 If no elements are available, `GetData` returns a null value.  
  
 While direct access to the elements of an array can help you work more quickly, use caution when calling `GetData`; any errors you make directly affect the elements of your array.  
  
## Example  
 [!CODE [NVC_MFCCollections#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#28)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetAt](../vs140/CArray--GetAt.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::ElementAt](../vs140/CArray--ElementAt.md)