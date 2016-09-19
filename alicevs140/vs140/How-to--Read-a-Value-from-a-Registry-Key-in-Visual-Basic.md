---
title: "How to: Read a Value from a Registry Key in Visual Basic"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 775d0a57-68c9-464e-8949-9a39bd29cc64
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Read a Value from a Registry Key in Visual Basic
The `GetValue` method of the `My.Computer.Registry` object can be used to read values in the Windows registry.  
  
 If the key, "Software\MyApp" in the following example, does not exist, an exception is thrown. If the `ValueName`,  "Name" in the following example, does not exist, `Nothing` is returned.  
  
 The `GetValue` method can also be used to determine whether a given value exists in a specific registry key.  
  
 When code reads the registry from a Web application, the current user is determined by the authentication and impersonation that is implemented in the Web application.  
  
### To read a value from a registry key  
  
-   Use the `GetValue` method, specifying the path and name) to read a value from registry key. The following example reads the value `Name` from `HKEY_CURRENT_USER\Software\MyApp` and displays it in a message box.  
  
     [!CODE [VbResourceTasks#4](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#4)]  
  
 This code example is also available as an IntelliSense code snippet. In the code snippet picker, it is located in **Windows Operating System > Registry**. For more information, see [Code Snippets](../vs140/Code-Snippets.md).  
  
### To determine whether a value exists in a registry key  
  
-   Use the `GetValue` method to retrieve the value. The following code checks whether the value exists and returns a message if it does not.  
  
     [!CODE [VbResourceTasks#12](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#12)]  
  
## Robust Programming  
 The registry holds top-level, or root, keys that are used to store data. For instance, the HKEY_LOCAL_MACHINE root key is used for storing machine-level settings used by all users, while HKEY_CURRENT_USER is used for storing data specific to an individual user.  
  
 The following conditions may cause an exception:  
  
-   The name of the key is `Nothing` (<xref:System.ArgumentNullException?qualifyHint=False>).  
  
-   The user does not have permissions to read from registry keys (<xref:System.Security.SecurityException?qualifyHint=False>).  
  
-   The key name exceeds the 255-character limit (<xref:System.ArgumentException?qualifyHint=False>).  
  
## .NET Framework Security  
 To run this process, your assembly requires a privilege level granted by the <xref:System.Security.Permissions.RegistryPermission?qualifyHint=False> class. If you are running in a partial-trust context, the process might throw an exception due to insufficient privileges. Similarly, the user must have the correct ACLs for creating or writing to settings. For example, a local application that has the code access security permission might not have operating system permission. For more information, see [Code Access Security Basics](assetId:///4eaa6535-d9fe-41a1-91d8-b437cfc16921).  
  
## See Also  
 <xref:Microsoft.VisualBasic.MyServices.RegistryProxy?qualifyHint=False>   
 <xref:Microsoft.Win32.RegistryHive?qualifyHint=False>   
 [Reading from and Writing to the Registry (Visual Basic)](../Topic/Reading%20from%20and%20Writing%20to%20the%20Registry%20\(Visual%20Basic\).md)