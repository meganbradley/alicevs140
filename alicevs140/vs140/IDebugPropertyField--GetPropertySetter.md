---
title: "IDebugPropertyField::GetPropertySetter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 744d76fd-2bcc-4917-a040-ce4cc714ef61
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPropertyField::GetPropertySetter
Gets the method that sets the property.  
  
## Syntax  
  
```cpp#  
HRESULT GetPropertySetter(   
   IDebugMethodField** ppField  
);  
```  
  
```c#  
int GetPropertySetter(  
   out IDebugMethodField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns an [IDebugMethodField](../vs140/IDebugMethodField.md) object representing the method that sets the property.  
  
## Return Value  
 If successful, returns S_OK; otherwise returns an error code.  
  
## Remarks  
 To get the method that gets the property, call the [GetPropertyGetter](../vs140/IDebugPropertyField--GetPropertyGetter.md) method.  
  
## See Also  
 [IDebugPropertyField](../vs140/IDebugPropertyField.md)   
 [IDebugMethodField](../vs140/IDebugMethodField.md)   
 [GetPropertyGetter](../vs140/IDebugPropertyField--GetPropertyGetter.md)