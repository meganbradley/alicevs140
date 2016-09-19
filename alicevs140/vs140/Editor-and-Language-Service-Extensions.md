---
title: "Editor and Language Service Extensions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5653bac9-724f-4948-a820-68ce6aa96365
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Editor and Language Service Extensions
You can extend most features of the Visual Studio code editor. The editor is based on the Windows Presentation Foundation (WPF) and is written in managed code. Although this design differs from the designs in earlier versions of Visual Studio, it provides most of the same features. To extend the editor, use the Managed Extensibility Framework (MEF).  
  
 The Visual Studio SDK provides adapters known as *shims* to support VSPackages that were written for earlier versions. Nevertheless, if you have an existing VSPackage, we recommend that you update it to the new technology to obtain better performance and reliability.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Creating an Extension with an Editor Item Template](../vs140/Creating-an-Extension-with-an-Editor-Item-Template.md)|Introduction to using the Editor item templates.|  
|[Extending the Editor](../Topic/Extending%20the%20Editor%20and%20Language%20Services.md)|Links to documents that introduce the design and features of the core editor and show how to extend it.|  
|[Accessing the Editor By Using Legacy Interfaces](../vs140/Legacy-Interfaces-in-the-Editor.md)|Links to documents that explain how to access the core editor from existing code.|  
|[Creating Custom Text Editors and Designers](../Topic/Creating%20Custom%20Editors%20and%20Designers.md)|Links to documents that explain how to create custom editors.|  
|[Language Services](../vs140/Legacy-Language-Service-Extensibility.md)|Links to documents that describe how to integrate programming languages into Visual Studio.|  
|[Managed Extensibility Framework Overview](assetId:///6c61b4ec-c6df-4651-80f1-4854f8b14dde)|Introduces the Managed Extensibility Framework (MEF).|  
|[Windows Presentation Foundation](assetId:///f667bd15-2134-41e9-b4af-5ced6fafab5d)|Introduces the Windows Presentation Foundation (WPF).|