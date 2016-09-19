---
title: "Input-Output Alternatives"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: Input/Output Alternatives
ms.assetid: 9f8401c7-d90d-4285-8918-63573df74a80
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Input-Output Alternatives
Visual C++ provides several alternatives for I/O programming:  
  
-   C run-time library direct, unbuffered I/O.  
  
-   ANSI C run-time library stream I/O.  
  
-   Console and port direct I/O.  
  
-   Microsoft Foundation Class Library.  
  
-   Microsoft Standard C++ Library.  
  
 The iostream classes are useful for buffered, formatted text I/O. They are also useful for unbuffered or binary I/O if you need a C++ programming interface and decide not to use the Microsoft Foundation Class (MFC) library. The iostream classes are an object-oriented I/O alternative to the C run-time functions.  
  
 You can use iostream classes with the Microsoft Windows operating system. String and file streams work without restrictions, but the character-mode stream objects `cin`, `cout`, `cerr`, and `clog` are inconsistent with the Windows graphical user interface. You can also derive custom stream classes that interact directly with the Windows environment.  
  
## See Also  
 [What a Stream Is](../vs140/What-a-Stream-Is.md)