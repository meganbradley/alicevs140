---
title: "IDebugCustomAttributeQuery2::IsCustomAttributeDefined"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c07cc52-6d2d-42df-9d76-9f1f769641db
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttributeQuery2::IsCustomAttributeDefined
Determines whether a custom attribute exists by name.  
  
## Syntax  
  
```cpp#  
HRESULT IsCustomAttributeDefined(   
   LPCOLESTR pszCustomAttributeName  
);  
```  
  
```c#  
int IsCustomAttributeDefined(  
   [In] string pszCustomAttributeName  
);  
```  
  
#### Parameters  
 `pszCustomAttributeName`  
 [in] A string containing the name of the custom attribute to find.  
  
## Return Value  
 Returns S_OK if the custom attribute is defined on this field, otherwise returns S_FALSE.  
  
## Remarks  
 To obtain the attribute bytes associated with the custom attribute, call the [IDebugCustomAttributeQuery2::GetCustomAttributeByName](../vs140/IDebugCustomAttributeQuery2--GetCustomAttributeByName.md) method.  
  
## See Also  
 [IDebugCustomAttributeQuery2](../vs140/IDebugCustomAttributeQuery2.md)