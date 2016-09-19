---
title: "Error: Windows file sharing has been configured..."
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c45a1b74-61ec-4c64-9e2c-13051a4f50a5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: Windows file sharing has been configured...
Windows file sharing has been configured so that you will connect to the remote computer using a different user name. This is incompatible with remote debugging  
  
 The current file sharing configuration is set up to connect to the remote computer using a different user name. Remote debugging is not possible in this scenario.  
  
 To correct this error, log onto the computer using the other account name, or change file sharing to use the account name you are debugging under.  
  
 If you want to connect to the remote computer using this user name, you must first disconnect from the remote computer.  
  
### To correct this error  
  
1.  Log onto your local machine, the machine you are debugging from, using the other account name.  
  
     —or—  
  
     . Disconnect from the remote computer, and then reconfigure file sharing to connect to the other machine using your account name:  
  
    1.  On the **Start** menu, point to **Accessories**, and then click **Command Prompt**.  
  
    2.  At the Windows command prompt, type:  
  
         `net use /delete computer_name`  
  
    3.  Change your file-sharing settings using any of the methods documented in Windows help.