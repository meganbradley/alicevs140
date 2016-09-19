---
title: "GETNAME_TYPE"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2f9f1679-e9e8-4c9c-ac90-aa07bfe69914
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# GETNAME_TYPE
Specifies the name type of files to retrieve.  
  
## Syntax  
  
```cpp#  
enum enum_GETNAME_TYPE {   
   GN_NAME         = 0,  
   GN_FILENAME     = 1,  
   GN_BASENAME     = 2,  
   GN_MONIKERNAME  = 3,  
   GN_URL          = 4,  
   GN_TITLE        = 5,  
   GN_STARTPAGEURL = 6  
};  
typedef DWORD GETNAME_TYPE;  
```  
  
```c#  
public enum enum_GETNAME_TYPE {   
   GN_NAME         = 0,  
   GN_FILENAME     = 1,  
   GN_BASENAME     = 2,  
   GN_MONIKERNAME  = 3,  
   GN_URL          = 4,  
   GN_TITLE        = 5,  
   GN_STARTPAGEURL = 6  
};  
```  
  
## Members  
 GN_NAME  
 Specifies a friendly name of the document or context.  
  
 GN_FILENAME  
 Specifies the full path of the document or context.  
  
 GN_BASENAME  
 Specifies a base file name instead of a full path of the document or context.  
  
 GN_MONIKERNAME  
 Specifies a unique name of the document or context in the form of a moniker.  
  
 GN_URL  
 Specifies a URL name of the document or context.  
  
 GN_TITLE  
 Specifies a title of the document, if one exists.  
  
 GN_STARTPAGEURL  
 Gets the starting page URL for processes.  
  
## Remarks  
 These values are passed as parameters to the [GetName](../vs140/IDebugDocument2--GetName.md), [GetName](../vs140/IDebugDocumentContext2--GetName.md), and [GetName](../vs140/IDebugProcess2--GetName.md) methods to specify what kind of name to return.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [GetName](../vs140/IDebugDocument2--GetName.md)   
 [GetName](../vs140/IDebugDocumentContext2--GetName.md)   
 [GetName](../vs140/IDebugProcess2--GetName.md)