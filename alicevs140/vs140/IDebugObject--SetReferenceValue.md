---
title: "IDebugObject::SetReferenceValue"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 08c78a4e-98eb-41cb-8b75-02a6a43d49f7
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject::SetReferenceValue
Sets the reference value of this object.  
  
## Syntax  
  
```cpp#  
HRESULT SetReferenceValue(   
   IDebugObject* pObject  
);  
```  
  
```c#  
int SetReferenceValue(  
   [In] IDebugObject pObject  
);  
```  
  
#### Parameters  
 `pObject`  
 [in] An [IDebugObject](../vs140/IDebugObject.md) object representing the new reference value.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 This method makes this [IDebugObject](../vs140/IDebugObject.md) object a reference to the value of the object given in the `pObject` parameter, throwing away any previous reference. Note that this `IDebugObject` object must already be a reference type.  
  
## See Also  
 [IDebugObject](../vs140/IDebugObject.md)   
 [GetValue](../vs140/IDebugObject--GetValue.md)