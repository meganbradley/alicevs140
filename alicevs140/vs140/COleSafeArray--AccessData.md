---
title: "COleSafeArray::AccessData"
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
ms.assetid: e34428c7-10b6-4bbb-a0ec-cb7b9655bedf
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::AccessData
Retrieves a pointer to the array data.  
  
## Syntax  
  
```  
  
      void AccessData(  
   void** ppvData   
);  
```  
  
#### Parameters  
 `ppvData`  
 A pointer to a pointer to the array data.  
  
## Remarks  
 On error, the function throws a [CMemoryException](../vs140/CMemoryException-Class.md) or [COleException](../vs140/COleException-Class.md).  
  
## Example  
 [!CODE [NVC_MFCOleContainer#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#26)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::UnaccessData](../vs140/COleSafeArray--UnaccessData.md)   
 [SafeArrayAccessData](assetId:///ded2112e-f6cd-4982-bacb-b95370e80187)