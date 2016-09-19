---
title: "IDebugDocument2::GetName"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f09ff09-b0cf-4472-8fc8-143991f0ceb1
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDocument2::GetName
Gets the name of the document in one of several forms.  
  
## Syntax  
  
```cpp#  
HRESULT GetName(   
   GETNAME_TYPE gnType,  
   BSTR*        pbstrFileName  
);  
```  
  
```c#  
int GetName(   
   enum_GETNAME_TYPE gnType,  
   out string        pbstrFileName  
);  
```  
  
#### Parameters  
 `gnType`  
 [in] A value from the [GETNAME_TYPE](../vs140/GETNAME_TYPE.md) enumeration that determines the type of name to return.  
  
 `pbstrFileName`  
 [out] Returns a string containing the document name.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method can, for example, return the name of the document as a title or as a file name or even part of a file name.  
  
## See Also  
 [IDebugDocument2](../vs140/IDebugDocument2.md)   
 [GETNAME_TYPE](../vs140/GETNAME_TYPE.md)