---
title: "IDebugPropertyField::GetPropertyGetter"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab9f861a-42ad-4a82-9ae6-2606176f755a
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPropertyField::GetPropertyGetter
Gets the method that gets the property.  
  
## Syntax  
  
```cpp#  
HRESULT GetPropertyGetter(   
   IDebugMethodField** ppField  
);  
```  
  
```cpp#  
int GetPropertyGetter(  
   out IDebugMethodField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns an [IDebugMethodField](../vs140/IDebugMethodField.md) object representing the method that gets the property.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 To get the method that sets the property, [GetPropertySetter](../vs140/IDebugPropertyField--GetPropertySetter.md) call the method.  
  
## See Also  
 [IDebugPropertyField](../vs140/IDebugPropertyField.md)   
 [GetPropertySetter](../vs140/IDebugPropertyField--GetPropertySetter.md)   
 [IDebugMethodField](../vs140/IDebugMethodField.md)