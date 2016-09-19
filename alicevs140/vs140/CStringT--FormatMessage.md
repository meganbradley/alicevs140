---
title: "CStringT::FormatMessage"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 30b65e13-fd06-49b7-9438-ca5089afae63
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringT::FormatMessage
Formats a message string.  
  
## Syntax  
  
```  
void __cdecl FormatMessage(  
   UINT nFormatID,  
   [, argument]...  
);  
void __cdecl FormatMessage(  
   PCXSTR pszFormat,  
   [, argument]...  
);  
```  
  
#### Parameters  
 `nFormatID`  
 The string resource identifier that contains the unformatted message text.  
  
 `pszFormat`  
 Points to the format-control string. It will be scanned for inserts and formatted accordingly. The format string is similar to run-time function `printf`-style format strings, except it allows for the parameters to be inserted in an arbitrary order.  
  
 `argument`  
 Optional arguments.  
  
## Remarks  
 The function requires a message definition as input. The message definition is determined by `pszFormat` or from the string resource identified by `nFormatID`. The function copies the formatted message text to the `CStringT` object, processing any embedded insert sequences if requested.  
  
> [!NOTE]
>  `FormatMessage` attempts to allocate system memory for the newly formatted string. If this attempt fails, a memory exception is automatically thrown.  
  
 Each insert must have a corresponding parameter following the `pszFormat` or `nFormatID` parameter. Within the message text, several escape sequences are supported for dynamically formatting the message. For more information, see the Windows [FormatMessage](http://msdn.microsoft.com/library/windows/desktop/ms679351) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#118](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#118)]  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CStringT Class](../vs140/CStringT-Class.md)   
 [CStringT::FormatMessageV](../vs140/CStringT--FormatMessageV.md)