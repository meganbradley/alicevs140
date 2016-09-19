---
title: "CDumpContext::SetDepth"
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
ms.assetid: 9a1c7877-c19a-4cfc-a258-68b725fe96ae
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDumpContext::SetDepth
Sets the depth for the dump.  
  
## Syntax  
  
```  
  
      void SetDepth(  
   int nNewDepth   
);  
```  
  
#### Parameters  
 *nNewDepth*  
 The new depth value.  
  
## Remarks  
 If you are dumping a primitive type or simple `CObject` that contains no pointers to other objects, then a value of 0 is sufficient. A value greater than 0 specifies a deep dump where all objects are dumped recursively. For example, a deep dump of a collection will dump all elements of the collection. You may use other specific depth values in your derived classes.  
  
> [!NOTE]
>  Circular references are not detected in deep dumps and can result in infinite loops.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#16)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CDumpContext Class](../vs140/CDumpContext-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::Dump](../vs140/CObject--Dump.md)