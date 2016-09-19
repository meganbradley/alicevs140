---
title: "IDebugExtendedField::GetExtendedKind"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 20dc1c13-3cc0-4bb4-9c99-fa85587c86c3
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugExtendedField::GetExtendedKind
Retrieves the specified extended field kind.  
  
## Syntax  
  
```cpp#  
HRESULT GetExtendedKind(  
   FIELD_KIND_EX* pdwKind  
);  
```  
  
```c#  
int GetExtendedKind(  
   ref enum_FIELD_KIND_EX pdwKind  
);  
```  
  
#### Parameters  
 `pdwKind`  
 [in, out] Value from the [FIELD_KIND_EX](../vs140/FIELD_KIND_EX.md) enumeration that defines the kind of field.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugExtendedField](../vs140/IDebugExtendedField.md)