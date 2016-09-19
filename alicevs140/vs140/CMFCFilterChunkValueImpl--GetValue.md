---
title: "CMFCFilterChunkValueImpl::GetValue"
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
ms.assetid: 8d4b9f7d-bc03-4789-8da3-4b1dc4f213b4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFilterChunkValueImpl::GetValue
Retrieves the value as an allocated propvariant.  
  
## Syntax  
  
```  
HRESULT GetValue(  
   PROPVARIANT **ppPropVariant  
);  
```  
  
#### Parameters  
 `ppPropVariant`  
 When the function returns, this parameter contains the chunk value.  
  
## Return Value  
 S_OK if PROPVARIANT was allocated successfully and the chunk value was successfully copied to `ppPropVariant`; otherwise an error code.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMFCFilterChunkValueImpl Class](../vs140/CMFCFilterChunkValueImpl-Class.md)