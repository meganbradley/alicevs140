---
title: "These project configuration(s) are out of date: &lt;configuration&gt;. Would you like to build them?"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0711f3b-3a2e-4247-afad-9e6468f9df96
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# These project configuration(s) are out of date: &lt;configuration&gt;. Would you like to build them?
You are editing a Visual Studio project or have selected a project in Solution Explorer, and you have chosen to Start (F5) the project or Start Without Debugging (CTRL+F5). One or more projects permit debugging without rebuilding, even if the project has been modified since the last build.  
  
 The integrated development environment (IDE) is asking whether or not to rebuild projects that permit debugging without rebuilding.  
  
### To respond to this message  
  
-   Select one of the buttons at the bottom of the message. The options are:  
  
|Term|Definition|  
|----------|----------------|  
|**Yes**|You will rebuild out-of-date projects. This means:<br /><br /> -   If the project has not yet been built, the project is built.<br />-   If the project has been modified since the last build, the project is rebuilt.<br />-   The project is debugged or started without debugging.|  
|**No**|You will rebuild only those out-of-date projects that must be rebuilt before debugging. This means:<br /><br /> -   If the project permits debugging without rebuilding (for example, a Visual C++ MFC Application project), the project is not rebuilt.<br />-   If the project must be rebuilt before debugging (for example, a Visual Basic project), the project is rebuilt.<br />-   The project is debugged, or started without debugging.|  
|**Cancel**|The current operation is stopped. No project is built, started, or debugged.|  
  
## See Also  
 [Configuration Manager Dialog Box](assetId:///fa182dca-282e-4ae5-bf37-e155344ca18b)   
 [Creating Solution and Project Build Configurations](assetId:///1844bff7-1ba0-4fcf-b6ab-97e26db0024d)   
 [How to: Create and Remove Project Dependencies](../vs140/How-to--Create-and-Remove-Project-Dependencies.md)   
 [Project Dependencies Dialog Box](assetId:///d66e48c3-3722-40dd-99b4-53d93cac128e)   
 [Project Dependencies, Common Properties, Solution Property Pages Dialog Box](assetId:///2ba638fc-719c-4a79-b166-3455a4374e31)   
 [Compiling and Building](../vs140/Compiling-and-Building-in-Visual-Studio.md)   
 [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md)   
 [NIB:Projects as Containers](assetId:///87d40f63-f487-4767-8963-64beec27ba1b)   
 [NIB:Item Management in Projects](assetId:///762e606b-7f44-4b66-97a1-e30a703654a0)