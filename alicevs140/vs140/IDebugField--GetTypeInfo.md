---
title: "IDebugField::GetTypeInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bb5acfa3-04c3-4088-be84-9ff8926cd16f
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugField::GetTypeInfo
This method gets type-independent information about the symbol or type.  
  
## Syntax  
  
```cpp#  
HRESULT GetTypeInfo(   
   TYPE_INFO* pTypeInfo  
);  
```  
  
```c#  
int GetTypeInfo(  
   TYPE_INFO[] pTypeInfo  
);  
```  
  
#### Parameters  
 `pTypeInfo`  
 [out] Returns type information in the supplied [TYPE_INFO](../vs140/TYPE_INFO.md) structure.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Type-independent information would include, for example, the AppDomain, the module, and the class that contains the symbol.  
  
## See Also  
 [GetType](../vs140/IDebugField--GetType.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [TYPE_INFO](../vs140/TYPE_INFO.md)