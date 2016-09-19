---
title: "MSBuild Error MSB3190"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45b45688-9345-45db-adc8-3e200f1c17eb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3190
**MSB3190: ClickOnce does not support the requested execution level '<level\>'.**  
  
 This error is generated on computers running Windows Vista when the application's embedded User Account Control (UAC) manifest specifies that a ClickOnce application run with administrative credentials. ClickOnce and Registration Free COM require an external manifest that specifies that the application run as the current user.  
  
 ClickOnce does not accept the execution levels `requireAdministrator` or `highestAvailable`. If you specify one of these levels, you will receive this error. ClickOnce requires `asInvoker`, but it will also accept no `<requestedExecutionLevel>` node, which specifies file/registry virtualization (meaning that no manifest is generated; this is done for backward compatibility).  
  
> [!NOTE]
>  Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions. The Visual Studio edition that you have and the settings that you use determine these elements. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### To correct this error  
  
-   Generate an external UAC manifest (app.manifest) that specifies that the application run as the current user (`asInvoker`).  
  
     In Visual C# projects, go to the **Application** page of the Project Designer and click **Properties\app.manifest** in the **Manifest** list. For more information, see [Application Page, Project Designer (C#)](../Topic/Application%20Page,%20Project%20Designer%20\(C%23\).md).  
  
     In Visual Basic projects, go to the **Application** page of the Project Designer and click the **View UAC Settings** button. This opens app.manifest for editing. Edit the following tag in the manifest to read as follows:  
  
    ```  
    <requestedExecutionLevel level="asInvoker" />  
    ```  
  
     For more information, see [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md).  
  
-   For more information about how to generate a UAC manifest and specify the execution level, see [ClickOnce Deployment on Windows Vista](../vs140/ClickOnce-Deployment-on-Windows-Vista.md).  
  
## See Also  
 [Application Page, Project Designer (C#)](../Topic/Application%20Page,%20Project%20Designer%20\(C%23\).md)   
 [Application Page, Project Designer (Visual Basic)](../Topic/Application%20Page,%20Project%20Designer%20\(Visual%20Basic\).md)   
 [ClickOnce Deployment on Windows Vista](../vs140/ClickOnce-Deployment-on-Windows-Vista.md)