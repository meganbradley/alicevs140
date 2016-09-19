---
title: "Cannot specify both -win32icon and -win32resource"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Cannot specify both /win32icon and /win32resource
ms.assetid: 60914807-1fde-4fef-9c6f-6f4a62527eed
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cannot specify both -win32icon and -win32resource
The `/win32resource` and `/win32icon` options are mutually exclusive, because they both insert icons information into the output file.  
  
 **Error ID:** BC2023  
  
### To correct this error  
  
-   Use only the `/win32icon` option to insert an .ico file in the output file. This .ico file represents the output file in Windows Explorer.  
  
     — or —  
  
-   Use only the `/win32resource` option to insert a Win32 resource file in the output file. A Win32 resource can contain version or bitmap (icon) information that helps identify your application in Windows Explorer.  
  
## See Also  
 [/win32icon](../vs140/-win32icon.md)   
 [/win32resource](../vs140/-win32resource.md)