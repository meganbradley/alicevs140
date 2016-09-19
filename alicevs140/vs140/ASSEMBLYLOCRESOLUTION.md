---
title: "ASSEMBLYLOCRESOLUTION"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0bcfe85c-5f37-4a9d-bf2b-141acd96ad67
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# ASSEMBLYLOCRESOLUTION
Specifies where an assembly is located.  
  
## Syntax  
  
```cpp#  
enum enum_ASSEMBLYLOCRESOLUTION {  
   ALR_NAME      = 0x0,  
   ALR_USERDIR   = 0x1,  
   ALR_SHAREDDIR = 0x2,  
   ALR_REMOTEDIR = 0x4,  
};  
typedef DWORD ASSEMBLYLOCRESOLUTION;  
```  
  
```c#  
public enum enum_ASSEMBLYLOCRESOLUTION {  
   ALR_NAME      = 0x0,  
   ALR_USERDIR   = 0x1,  
   ALR_SHAREDDIR = 0x2,  
   ALR_REMOTEDIR = 0x4,  
};  
```  
  
## Members  
 ALR_NAME  
 Assembly is located in the current namespace.  
  
 ALR_USERDIR  
 Assembly is located in a user directory.  
  
 ALR_SHAREDDIR  
 Assembly is located in shared directory.  
  
 ALR_REMOTEDIR  
 Assembly is located in a remote directory.  
  
## Remarks  
 These values are returned by the [IPropertyProxyEESide::ResolveAssemblyRef](../vs140/IPropertyProxyEESide--ResolveAssemblyRef.md) and [IPropertyProxyEESide::GetManagedViewerCreationData](../vs140/IPropertyProxyEESide--GetManagedViewerCreationData.md) methods.  
  
 These values can be combined with the `OR` operation.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations (Visual Studio Debugging SDK)](../vs140/Enumerations--Visual-Studio-Debugging-.md)   
 [IPropertyProxyEESide::ResolveAssemblyRef](../vs140/IPropertyProxyEESide--ResolveAssemblyRef.md)   
 [IPropertyProxyEESide::GetManagedViewerCreationData](../vs140/IPropertyProxyEESide--GetManagedViewerCreationData.md)