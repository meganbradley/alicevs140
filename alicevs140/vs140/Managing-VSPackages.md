---
title: "Managing VSPackages"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 386e0ce5-4107-4164-b0cd-1cf43eb5e7cf
caps.latest.revision: 37
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Managing VSPackages
In most cases you don’t need to worry about managing VSPackages, since the project and item templates register and load the package automatically. However, in some circumstances you may need to learn a bit more in order to manage your package.  
  
## Using the experimental instance  
 To find out more about the experimental instance, see [The Experimental Instance](../vs140/The-Experimental-Instance.md).  
  
## Registering and Unregistering VSPackages  
 To find out how to register and unregister VSPackages and other types of extension, see [Registering and Unregistering VSPackages](../vs140/Registering-and-Unregistering-VSPackages.md).  
  
## Loading a VSPackage  
 VSPackages can be set to autoload when a particular CMDUICONTEXT GUID is turned on. For more information, see [Loading VSPackages](../Topic/Loading%20VSPackages.md).  
  
## Using AsyncPackage to Load VSPackages in the Background  
 The AsyncPackage class enables package loading on a background thread for better UI responsiveness in Visual Studio. For more information, see [Use AsyncPackage to Load VSPackages in the Background](../Topic/How%20to:%20Use%20AsyncPackage%20to%20Load%20VSPackages%20in%20the%20Background.md).  
  
## Rule-based UI Context for Extensions  
 Rules-based UI Contexts allows extension authors to define the precise conditions under which a UI Context is activated and associated VSPackages loaded. For more information, see [Rule-base UI Context for Visual Studio Extensions](../vs140/How-to--Use-Rule-based-UI-Context-for-Visual-Studio-Extensions.md).  
  
## Troubleshooting VSPackages  
 Find out the techniques for troubleshooting VSPackages that don’t load or are experiencing errors: [Troubleshooting VSPackages](../vs140/Troubleshooting-VSPackages.md)  
  
## See Also  
 [VSPackages](../vs140/VSPackages.md)