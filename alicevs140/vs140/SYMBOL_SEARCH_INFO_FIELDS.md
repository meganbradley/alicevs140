---
title: "SYMBOL_SEARCH_INFO_FIELDS"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bce35af0-722d-46d4-afa6-eaae598c51ff
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SYMBOL_SEARCH_INFO_FIELDS
Specifies the kind of symbol information to retrieve.  
  
## Syntax  
  
```cpp#  
enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
typedef DWORD SYMBOL_SEARCH_INFO_FIELDS;  
```  
  
```c#  
public enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
  
```  
  
## Members  
 SSIF_NONE  
 Indicates no flags  
  
 SSIF_VERBOSE_SEARCH_INFO  
 Returns all search paths used for finding symbols  
  
## Remarks  
 These flags are passed as a parameter to the [IDebugModule3::GetSymbolInfo](../vs140/IDebugModule3--GetSymbolInfo.md) method to determine the amount of information returned.  
  
> [!NOTE]
>  Currently, only `SSIF_VERBOSE_SEARCH_INFO` is supported, and it must be specified as the `dwFlags` parameter to `IDebugModule3::GetSymbolInfo`. All other values return an error.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IDebugModule3::GetSymbolInfo](../vs140/IDebugModule3--GetSymbolInfo.md)