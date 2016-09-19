---
title: "IDebugCustomAttribute::GetName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba509cc5-5816-4925-a094-4c72d88c360c
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttribute::GetName
Gets the name of the custom attribute.  
  
## Syntax  
  
```cpp#  
HRESULT GetName(   
   BSTR* bstrName  
);  
```  
  
```c#  
int GetName(  
   out string bstrName  
);  
```  
  
#### Parameters  
 `bstrName`  
 [out] Returns a string containing the name of the custom attribute.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 The named returned by this method corresponds to the name of the class used to declare the attribute. This may not exactly correspond to the name of the custom attribute class itself as C# allows the "Attribute" suffix to be dropped from a custom attribute name when it is used in a declaration.  
  
## See Also  
 [IDebugCustomAttribute](../vs140/IDebugCustomAttribute.md)