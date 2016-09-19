---
title: "IDebugObject2::GetField"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: add6a6b5-e752-47dd-9613-29206ea809b0
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject2::GetField
Gets the type of this object.  
  
## Syntax  
  
```cpp  
HRESULT GetField(  
 IDebugField** ppField  
);  
```  
  
```c#  
int GetField(  
   out IDebugField ppField  
);  
```  
  
#### Parameters  
 `ppField`  
 [out] Returns an [IDebugField](../vs140/IDebugField.md) object if not a null value.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 A field describes the type of the object.  
  
## See Also  
 [IDebugObject2](../vs140/IDebugObject2.md)   
 [IDebugField](../vs140/IDebugField.md)