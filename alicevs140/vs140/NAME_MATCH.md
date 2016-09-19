---
title: "NAME_MATCH"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3842c417-a3c9-4259-a05f-52b64b829ef6
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# NAME_MATCH
Selects the case option for matching names.  
  
## Syntax  
  
```cpp#  
typedef enum {   
   nmNone            = 0,  
   nmCaseSensitive   = 1,  
   nmCaseInsensitive = 2  
} NAME_MATCH;  
```  
  
```c#  
public enum NameMatchOptions {   
   nmNone            = 0,  
   nmCaseSensitive   = 1,  
   nmCaseInsensitive = 2  
}  
```  
  
## Members  
 nmNone  
 No options are specified.  
  
 nmCaseSensitive  
 Indicates that names to be matched are case-sensitive.  
  
 nmCaseInsensitive  
 Indicates that names to be matched are not case-sensitive.  
  
## Remarks  
 Passed as an argument to the following methods:  
  
-   [IDebugSymbolProvider::GetTypeByName](../vs140/IDebugSymbolProvider--GetTypeByName.md)  
  
-   [IDebugSymbolProvider::GetClassTypeByName](../vs140/IDebugSymbolProvider--GetClassTypeByName.md)  
  
-   [IDebugContainerField::EnumFields](../vs140/IDebugContainerField--EnumFields.md)  
  
-   [IDebugSymbolProvider::GetMethodFieldsByName](../vs140/IDebugSymbolProvider--GetMethodFieldsByName.md)  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugSymbolProvider::GetTypeByName](../vs140/IDebugSymbolProvider--GetTypeByName.md)   
 [IDebugSymbolProvider::GetClassTypeByName](../vs140/IDebugSymbolProvider--GetClassTypeByName.md)   
 [IDebugContainerField::EnumFields](../vs140/IDebugContainerField--EnumFields.md)   
 [IDebugSymbolProvider::GetMethodFieldsByName](../vs140/IDebugSymbolProvider--GetMethodFieldsByName.md)