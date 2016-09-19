---
title: "IDebugEnumField::GetUnderlyingSymbol"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c3b8a117-6708-4cfd-8ffc-5f007d706bc5
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEnumField::GetUnderlyingSymbol
This method returns an [IDebugField](../vs140/IDebugField.md) that represents the name of the enumeration.  
  
## Syntax  
  
```cpp#  
HRESULT GetUnderlyingSymbol(  
   IDebugField** ppField  
);  
```  
  
```c#  
int GetUnderlyingSymbol(  
   out IDebugField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns the [IDebugField](../vs140/IDebugField.md) describing the name of this enumeration.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The name of the enumeration also contains the type of the enumeration, which is bound to a memory location by using [IDebugBinder::Bind](../vs140/IDebugBinder--Bind.md).  
  
## See Also  
 [IDebugEnumField](../vs140/IDebugEnumField.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugBinder::Bind](../vs140/IDebugBinder--Bind.md)