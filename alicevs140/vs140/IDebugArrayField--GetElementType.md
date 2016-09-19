---
title: "IDebugArrayField::GetElementType"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c46bf625-0a48-4cbb-8f1f-286356f2c065
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugArrayField::GetElementType
Gets the type of element in the array.  
  
## Syntax  
  
```cpp#  
HRESULT GetElementType(   
   IDebugField** ppType  
);  
```  
  
```c#  
int GetElementType(  
   out IDebugField ppType  
);  
```  
  
#### Parameters  
 `ppType`  
 [out] Returns an [IDebugField](../vs140/IDebugField.md) object that describes the type of element.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 The [IDebugArrayField](../vs140/IDebugArrayField.md) object assumes that all elements of the array are the same type.  
  
## See Also  
 [IDebugArrayField](../vs140/IDebugArrayField.md)   
 [IDebugField](../vs140/IDebugField.md)