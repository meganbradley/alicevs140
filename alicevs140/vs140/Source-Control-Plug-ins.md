---
title: "Source Control Plug-ins"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 964980ca-21c5-4706-8535-6ea23e1c9cc9
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Source Control Plug-ins
The Source Control Plug-in SDK reference section contains the complete interface specification that enables source control systems to be integrated with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. It specifies the syntax and semantics of the various functions and data types that the source control plug-in must implement to interface with the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE).  
  
## In This Section  
 [Source Control Plug-in API Functions](../vs140/Source-Control-Plug-in-API-Functions.md)  
 Lists functions that must be implemented by the source control plug-in in order to comply with the Source Control Plug-in API.  
  
 [Callback Functions Implemented by the IDE](../vs140/Callback-Functions-Implemented-by-the-IDE.md)  
 Describes functions that the source control plug-in uses to pass information back to the IDE while certain commands are executed.  
  
 [Enumerators](../vs140/Enumerators.md)  
 Lists the enumerator data types in the Source Control Plug-in API that the source control plug-in must know about.  
  
 [Capability Flags](../vs140/Capability-Flags.md)  
 Describes the `SCC_CAP_xxx` flags, which are indicate a provider's capabilities.  
  
 [Bitflags Used by Specific Commands](../vs140/Bitflags-Used-by-Specific-Commands.md)  
 Lists flags that are useful in the context of particular commands.  
  
 [Error Codes](../vs140/Error-Codes.md)  
 Lists common error values returned by functions as `SCCTRN`.  
  
 [Strings Used as Keys for Finding a Source Control Plug-in](../vs140/Strings-Used-as-Keys-for-Finding-a-Source-Control-Plug-in.md)  
 Describes keys for accessing the registry to find the source control plug-in.  
  
 [MSSCCPRJ.SCC File](../vs140/MSSCCPRJ.SCC-File.md)  
 Describes a client-side file that contains information opaque to the IDE, but that is used by the source control plug-in to locate the solution or project in version control.  
  
 [Best Practices for Implementing a Source Control Plug-in](../vs140/Best-Practices-for-Implementing-a-Source-Control-Plug-in.md)  
 Provides a collection of important technical reminders to remember while you are implementing the Source Control Plug-in API.  
  
 [Restrictions on String Lengths](../vs140/Restrictions-on-String-Lengths.md)  
 Describes limitations in the Source Control Plug-in API on the lengths of strings used in various functions.  
  
 [Glossary](../vs140/Source-Control-Plug-in-Glossary.md)  
 Provides helpful terms and their definitions for reading the Source Control Plug-in SDK documentation.  
  
 [How to: Turn Off Compatibility Warnings for Source Control Plug-ins](../vs140/How-to--Turn-Off-Compatibility-Warnings-for-Source-Control-Plug-ins.md)  
 Describes how to disable warnings.  
  
## Related Sections  
 [Source Control Plug-in Sample](assetId:///61de7d2b-71db-451e-8e3e-d41b11c7a4ca)  
 Provides a sample of source control plug-in functionality.  
  
 [Test Guide for Source Control Plug-ins](../vs140/Test-Guide-for-Source-Control-Plug-ins.md)  
 Describes testing procedures related to a source control plug-in.  
  
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)  
 Discusses how to create a source control plug-in that supplies source control functionality while you are using the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] source control user interface (UI).  
  
 [Visual Studio SDK Reference](../Topic/Visual%20Studio%20SDK%20Reference.md)  
 Presents a list of reference topics.