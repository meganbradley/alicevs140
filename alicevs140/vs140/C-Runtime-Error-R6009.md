---
title: "C Runtime Error R6009"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: edfb1f8b-3807-48f4-a994-318923b747ae
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Runtime Error R6009
not enough space for environment  
  
> [!NOTE]
>  If you encounter this error message while running an app, the app was shut down because it has an internal memory problem. There are several possible reasons for this error, but often it's caused by an extremely low memory condition, too much memory taken by environment variables, or a bug in the program.  
>   
>  You can try these steps to fix this error:  
>   
>  -   Close other running applications or restart your computer to free up memory.  
> -   Use the **Apps and Features** or **Programs and Features** page in the **Control Panel** to repair or reinstall the program.  
> -   Check **Windows Update** in the **Control Panel** for software updates.  
> -   Check for an updated version of the app. Contact the app vendor if the problem persists.  
  
 **Information for Programmers**  
  
 There was enough memory to load the program, but not enough memory to create the **envp** array.  This can be caused by extremely low memory conditions, or by unusually large environment variable usage. Consider one of the following solutions:  
  
-   Increase the amount of memory available to the program.  
  
-   Reduce the number and size of command-line arguments.  
  
-   Reduce the environment size by removing unnecessary variables.