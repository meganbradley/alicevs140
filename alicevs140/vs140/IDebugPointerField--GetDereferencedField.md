---
title: "IDebugPointerField::GetDereferencedField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8de988ab-cd79-4287-be72-3c900f2fe407
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPointerField::GetDereferencedField
This method returns the type of object to which this pointer object points.  
  
## Syntax  
  
```cpp#  
HRESULT GetDereferencedField(  
   IDebugField** ppField  
);  
```  
  
```c#  
int GetDereferencedField(  
   out IDebugField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns an [IDebugField](../vs140/IDebugField.md) describing the type of target object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 If, for example, the [IDebugPointerField](../vs140/IDebugPointerField.md) object points to an integer, the [IDebugField](../vs140/IDebugField.md) type returned by this method describes that integer type.  
  
## See Also  
 [IDebugPointerField](../vs140/IDebugPointerField.md)   
 [IDebugField](../vs140/IDebugField.md)