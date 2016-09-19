---
title: "Source Control Integration Essentials"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 442057cb-fd54-4283-96f8-2f6dc8bf2de7
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Source Control Integration Essentials
[!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] supports two types of source control integration: a source control plug-in that provides basic functionality and is built using the Source Control Plug-in API (formerly known as the MSSCCI API), and a VSPackage-based source control integration solution that provides more robust functionality.  
  
## Source Control Plug-in  
 A Source Control Plug-in is written as a DLL that implements the Source Control Plug-in API. Registration and source control integration functionality is provided through the API. This approach is easier to implement than a source control VSPackage, and it uses the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] user interface (UI) for most source control operations.  
  
 To implement a source control plug-in using the Source Control Plug-in API, follow these steps:  
  
1.  Create a DLL that implements the functions specified in [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md).  
  
2.  Register the DLL by making the appropriate registry entries, as described in [How-to Install a Source Control Plug-in](../vs140/How-to--Install-a-Source-Control-Plug-in.md).  
  
3.  Create a helper UI and display it when prompted by the Source Control Adapter Package (the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] component that handles source control functionality through source control plug-ins).  
  
 For more information, see [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md).  
  
## Source Control VSPackage  
 A source control VSPackage implementation allows you to develop a customized replacement for the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] source control UI. This approach provides complete control over source control integration, but it requires you to provide the UI elements and implement the source control interfaces that otherwise would be provided under the plug-in approach.  
  
 To implement a source control VSPackage, you must:  
  
1.  Create and register your own source control VSPackage, as described in [Source-Control VSPackage Registration and Selection](../Topic/Registration%20and%20Selection%20\(Source%20Control%20VSPackage\).md).  
  
2.  Replace the default source control UI with your custom UI. See [Custom UI (Source-Control VSPackage)](../vs140/Custom-User-Interface--Source-Control-VSPackage-.md).  
  
3.  Specify glyphs to be used, and handle **Solution Explorer** glyph events. See [Glyph Control (Source-Control VSPackage)](../Topic/Glyph%20Control%20\(Source%20Control%20VSPackage\).md).  
  
4.  Handle Query Edit and Query Save events, as shown in [Query Edit Query Save (Source-Control VSPackage)](../vs140/Query-Edit-Query-Save--Source-Control-VSPackage-.md).  
  
 For more information, see [Creating a Source-Control VSPackage](../vs140/Creating-a-Source-Control-VSPackage.md).  
  
## See Also  
 [Overview of Source Control Integration](../vs140/Source-Control-Integration-Overview.md)   
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)   
 [Creating a Source-Control VSPackage](../vs140/Creating-a-Source-Control-VSPackage.md)