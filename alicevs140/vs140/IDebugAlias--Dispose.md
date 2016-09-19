---
title: "IDebugAlias::Dispose"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e84909a4-d378-4f48-bf25-2c014c77c8e3
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugAlias::Dispose
Marks this alias for removal.  
  
## Syntax  
  
```cpp  
HRESULT Dispose();  
```  
  
```c#  
int Dispose();  
```  
  
#### Parameters  
 None.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Once this method is called, the alias is no longer available.  
  
## See Also  
 [IDebugAlias](../vs140/IDebugAlias.md)