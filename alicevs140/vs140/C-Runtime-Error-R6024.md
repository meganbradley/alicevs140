---
title: "C Runtime Error R6024"
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
ms.assetid: 0fb11c0f-9b81-4cab-81bd-4785742946a5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Runtime Error R6024
not enough space for _onexit/atexit table  
  
> [!NOTE]
>  If you encounter this error message while running an app, the app was shut down because it has an internal memory problem. This error is usually caused by an extremely low memory condition, or rarely, by a bug in the program or by corruption of the Visual C++ libraries that it uses.  
>   
>  You can try these steps to fix this error:  
>   
>  -   Close other running applications or restart your computer to free up memory.  
> -   Use the **Apps and Features** or **Programs and Features** page in the **Control Panel** to repair or reinstall the program.  
> -   Use the **Apps and Features** or **Programs and Features** page in the **Control Panel** to repair or reinstall all copies of the Microsoft Visual C++ Redistributable.  
> -   Check **Windows Update** in the **Control Panel** for software updates.  
> -   Check for an updated version of the app. Contact the app vendor if the problem persists.  
  
 **Information for Programmers**  
  
 This error occurs because there was no memory available for the `_onexit` or `atexit` function. This error is caused by a low-memory condition. You may consider pre-allocating buffers at app startup to assist in saving user data and performing a clean app exit in low-memory conditions.