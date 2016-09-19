---
title: "IDebugAlias::GetObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 97bc3af6-6e55-4940-8a6d-692c61257806
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAlias::GetObject
Gets the object that this alias is for.  
  
## Syntax  
  
```cpp  
HRESULT GetObject(  
   IDebugObject2** ppObject  
);  
```  
  
```c#  
int GetObject(  
   Out IDebugObject2 ppObject  
)  
```  
  
#### Parameters  
 `ppObject`  
 [out] The [IDebugObject2](../vs140/IDebugObject2.md) this alias represents.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## See Also  
 [IDebugAlias](../vs140/IDebugAlias.md)   
 [IDebugObject2](../vs140/IDebugObject2.md)