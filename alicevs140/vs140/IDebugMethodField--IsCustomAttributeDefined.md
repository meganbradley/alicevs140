---
title: "IDebugMethodField::IsCustomAttributeDefined"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b5d95a8-cc87-4acb-9e6a-3928f3632b7c
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugMethodField::IsCustomAttributeDefined
Determines whether a specific custom attribute has been defined.  
  
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
 Returns S_OK if the custom attribute is defined on this method, otherwise returns S_FALSE.  
  
## See Also  
 [IDebugMethodField](../vs140/IDebugMethodField.md)