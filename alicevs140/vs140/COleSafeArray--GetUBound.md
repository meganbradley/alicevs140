---
title: "COleSafeArray::GetUBound"
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
ms.assetid: f596ea83-ce8e-47c9-bf55-c36f0f6496b0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::GetUBound
Returns the upper bound for any dimension of a safe array.  
  
## Syntax  
  
```  
  
      void GetUBound(  
   DWORD dwDim,  
   long* pUBound   
);  
```  
  
#### Parameters  
 `dwDim`  
 The array dimension for which to get the upper bound.  
  
 *pUBound*  
 Pointer to the location to return the upper bound.  
  
## Remarks  
 On error, the function throws a [COleException](../vs140/COleException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#31](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#31)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::GetLBound](../vs140/COleSafeArray--GetLBound.md)   
 [SafeArrayGetUBound](assetId:///aed339d5-d962-4adc-ac01-6c15a54c51ca)