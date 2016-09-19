---
title: "Input and Output"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c177301-e341-4ca0-aedc-0a87fe1c75ae
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Input and Output
The I/O functions read and write data to and from files and devices. File I/O operations take place in text mode or binary mode. The Microsoft run-time library has three types of I/O functions:  
  
-   [Stream I/O](../vs140/Stream-I-O.md) functions treat data as a stream of individual characters.  
  
-   [Low-level I/O](../vs140/Low-Level-I-O.md) functions invoke the operating system directly for lower-level operation than that provided by stream I/O.  
  
-   [Console and port I/O](../vs140/Console-and-Port-I-O.md) functions read or write directly to a console (keyboard and screen) or an I/O port (such as a printer port).  
  
    > [!NOTE]
    >  Because stream functions are buffered and low-level functions are not, these two types of functions are generally incompatible. For processing a particular file, use either stream or low-level functions exclusively.  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)