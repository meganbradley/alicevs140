---
title: "IDebugCustomAttribute::GetParentField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcdfdf37-bfcf-4988-a7b8-4c731d0af1b0
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCustomAttribute::GetParentField
Gets the field to which the custom attribute is attached.  
  
## Syntax  
  
```cpp#  
HRESULT GetParentField(   
   IDebugField** ppField  
);  
```  
  
```c#  
int GetParentField(  
   out IDebugField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns the [IDebugField](../vs140/IDebugField.md) object that represents the field to which the custom attribute is attached.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Call the [IDebugField::GetKind](../vs140/IDebugField--GetKind.md) method on the returned [IDebugField](../vs140/IDebugField.md) object to determine what kind of field the parent is.  
  
## See Also  
 [IDebugCustomAttribute](../vs140/IDebugCustomAttribute.md)   
 [IDebugField](../vs140/IDebugField.md)