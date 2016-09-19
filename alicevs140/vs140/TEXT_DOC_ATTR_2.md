---
title: "TEXT_DOC_ATTR_2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2333b33b-042b-4ac6-9ebe-e66f95f52f51
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# TEXT_DOC_ATTR_2
Describes the attributes of a document.  
  
## Syntax  
  
```cpp#  
typedef DWORD TEXT_DOC_ATTR_2;  
const TEXT_DOC_ATTR_2 TEXT_DOC_ATTR_READONLY_2 = 0x00000001;  
```  
  
```c#  
public const uint TEXT_DOC_ATTR_READONLY_2 = 0x00000001;  
```  
  
## Members  
 TEXT_DOC_ATTR_READONLY_2  
 Indicates that the document is read-only.  
  
## Remarks  
  
> [!NOTE]
>  This value is not actually defined in the assembly for C#. Instead, you must copy the definition to your source file.  
  
 Passed as an argument to the [onUpdateDocumentAttributes](../vs140/IDebugDocumentTextEvents2--onUpdateDocumentAttributes.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [onUpdateDocumentAttributes](../vs140/IDebugDocumentTextEvents2--onUpdateDocumentAttributes.md)