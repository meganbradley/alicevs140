---
title: "IDebugBinder3::FindAlias"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8333701-2718-4983-8513-0875fb7cb730
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBinder3::FindAlias
This method locates an alias, given a name. This will search all aliases in the program.  
  
## Syntax  
  
```cpp  
HRESULT FindAlias(  
   LPCOLESTR     pcstrName,  
   IDebugAlias** ppAlias  
);  
```  
  
```c#  
int FindAlias(  
   string          pcstrName,  
   out IDebugAlias ppAlias  
);  
```  
  
#### Parameters  
 `pcstrName`  
 [in] Name of alias to find.  
  
 `ppAlias`  
 [out] Alias found (if any) represented by the [IDebugAlias](../vs140/IDebugAlias.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` (if alias is not found) or an error code.  
  
## Remarks  
 This method initializes the destination object to null before calling; then it tests for a null value afterward to determine whether or not the alias was found.  
  
## See Also  
 [IDebugBinder3](../vs140/IDebugBinder3.md)   
 [IDebugAlias](../vs140/IDebugAlias.md)