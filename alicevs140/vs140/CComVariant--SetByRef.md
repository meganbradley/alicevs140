---
title: "CComVariant::SetByRef"
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
ms.assetid: c246113b-9918-45be-b669-4f11764cae4d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComVariant::SetByRef
Initializes the `CComVariant` object and sets the **vt** member to **VT_BYREF**.  
  
## Syntax  
  
```  
  
      template< typename   
      T  
       >  
void SetByRef(  
   T* pT   
) throw();  
```  
  
#### Parameters  
 `T`  
 The type of **VARIANT**, for example, `BSTR`, `int`, or `char`.  
  
 *pT*  
 The pointer used to initialize the `CComVariant` object.  
  
## Remarks  
 `SetByRef` is a function template that initializes the `CComVariant` object to the pointer *pT* and sets the **vt** member to **VT_BYREF**. For example:  
  
 [!CODE [NVC_ATL_Utilities#76](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#76)]  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComVariant Class](../vs140/CComVariant-Class.md)