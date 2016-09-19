---
title: "COleSafeArray::GetElement"
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
ms.assetid: 10567368-822a-40f7-ac4f-7738747b1809
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::GetElement
Retrieves a single element of the safe array.  
  
## Syntax  
  
```  
  
      void GetElement(  
   long* rgIndices,  
   void* pvData   
);  
```  
  
#### Parameters  
 `rgIndices`  
 Pointer to an array of indexes for each dimension of the array.  
  
 `pvData`  
 Pointer to the location to place the element of the array.  
  
## Remarks  
 This function automatically calls the windows functions `SafeArrayLock` and `SafeArrayUnlock` before and after retrieving the element. If the data element is a string, object, or variant, the function copies the element in the correct way. The parameter `pvData` should point to a large enough buffer to contain the element.  
  
 On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#29)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::PutElement](../vs140/COleSafeArray--PutElement.md)