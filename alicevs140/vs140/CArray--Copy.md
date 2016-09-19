---
title: "CArray::Copy"
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
ms.assetid: 74af1eb5-7190-49dc-b767-872e2e87071e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::Copy
Use this member function to copy the elements of one array to another.  
  
## Syntax  
  
```  
  
      void Copy(  
   const CArray& src   
);  
```  
  
#### Parameters  
 *src*  
 Source of the elements to be copied to an array.  
  
## Remarks  
 Call this member function to overwrite the elements of one array with the elements of another array.  
  
 **Copy** does not free memory; however, if necessary, **Copy** may allocate extra memory to accommodate the elements copied to the array.  
  
## Example  
 [!CODE [NVC_MFCCollections#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#25)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::Append](../vs140/CArray--Append.md)