---
title: "IDispEventImpl::GetUserDefinedType"
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
ms.assetid: 9958c5d0-8918-4b49-a9dc-fee33e6a75ed
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventImpl::GetUserDefinedType
Retrieves the basic type of a user-defined type.  
  
## Syntax  
  
```  
  
      VARTYPE GetUserDefinedType(  
   ITypeInfo *pTI,  
   HREFTYPE hrt   
);  
```  
  
#### Parameters  
 `pTI`  
 [in] A pointer to the [ITypeInfo](assetId:///f3356463-3373-4279-bae1-953378aa2680) interface containing the user-defined type.  
  
 *hrt*  
 [in] A handle to the type description to be retrieved.  
  
## Return Value  
 The type of variant.  
  
## Remarks  
 See [ITypeInfo::GetRefTypeInfo](assetId:///61d3b31d-6591-4e55-9e82-5246a168be00).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventImpl Class](../vs140/IDispEventImpl-Class.md)   
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)