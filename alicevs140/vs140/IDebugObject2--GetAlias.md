---
title: "IDebugObject2::GetAlias"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa6824d5-c932-42ba-8713-950e7d1fb42f
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugObject2::GetAlias
Gets the alias associated with this object, if any.  
  
## Syntax  
  
```cpp  
HRESULT GetAlias(  
   IDebugAlias** ppAlias  
);  
```  
  
```c#  
int GetAlias(  
   out IDebugAlias ppAlias  
);  
```  
  
#### Parameters  
 `ppAlias`  
 [out] Returns an [IDebugAlias](../vs140/IDebugAlias.md) object representing the alias for this object; otherwise, returns a null value.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 An alias for an object is created with a call to the [IDebugObject2::CreateAlias](../vs140/IDebugObject2--CreateAlias.md) method.  
  
## See Also  
 [IDebugObject2](../vs140/IDebugObject2.md)   
 [IDebugAlias](../vs140/IDebugAlias.md)