---
title: "IDebugEnumField::GetValueFromString"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ef8ac5e-a3e0-4078-b876-7f5615aedcbb
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEnumField::GetValueFromString
This method returns the value associated with the name of an enumeration constant.  
  
## Syntax  
  
```cpp#  
HRESULT GetValueFromString(  
   LPCOLESTR  pszValue,  
   ULONGLONG* pvalue  
);  
```  
  
```c#  
int GetValueFromString(  
   string    pszValue,  
   out ulong pValue  
);  
```  
  
#### Parameters  
 `pszValue`  
 [in] A string specifying the name for which to get the value. Note that for C++, this is a wide character string.  
  
 `pValue`  
 [out] Returns the associated numerical value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE`, if the name is not part of the enumeration, or an error code.  
  
## Remarks  
 This method is case-sensitive. If a case-insensitive search is needed (for example, in a language such as Visual Basic where names are not case sensitive), use [IDebugEnumField::GetValueFromStringCaseInsensitive](../vs140/IDebugEnumField--GetValueFromStringCaseInsensitive.md).  
  
## See Also  
 [IDebugEnumField](../vs140/IDebugEnumField.md)   
 [IDebugEnumField::GetValueFromStringCaseInsensitive](../vs140/IDebugEnumField--GetValueFromStringCaseInsensitive.md)