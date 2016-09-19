---
title: "IDebugField::GetSize"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 73329924-3751-4f44-af54-5986b7943374
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugField::GetSize
This method gets the size of a field, in bytes.  
  
## Syntax  
  
```cpp#  
HRESULT GetSize(   
   DWORD* pdwSize  
);  
```  
  
```c#  
int GetSize(  
   out uint pdwSize  
);  
```  
  
#### Parameters  
 `pdwSize`  
 [out] Returns the size.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 All fields have a type and all types have a size. For example, a field with a type of byte has a size of 1 byte.  
  
## See Also  
 [IDebugField](../vs140/IDebugField.md)