---
title: "Text and Binary Mode File I-O"
ms.custom: na
ms.date: 09/18/2016
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
H1: Text and Binary Mode File I/O
ms.assetid: 3196e321-8b87-4609-b302-cd6f3c516051
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Text and Binary Mode File I-O
File I/O operations take place in one of two translation modes, text or binary, depending on the mode in which the file is opened. Data files are usually processed in text mode. To control the file translation mode, one can:  
  
-   Retain the current default setting and specify the alternative mode only when you open selected files.  
  
-   Use the function [_set_fmode](../vs140/_set_fmode.md) to change the default mode for newly opened files. Use [_get_fmode](../vs140/_get_fmode.md) to find the current default mode. The initial default setting is text mode (`_O_TEXT`).  
  
-   Change the default translation mode directly by setting the global variable [_fmode](../vs140/_fmode.md) in your program. The function `_set_fmode` sets the value of this variable, but it can also be set directly.  
  
 When you call a file-open function such as [_open](../Topic/_open,%20_wopen.md), [fopen](../vs140/fopen--_wfopen.md), [fopen_s](../Topic/fopen_s,%20_wfopen_s.md), [freopen](../Topic/freopen,%20_wfreopen.md), [freopen_s](../Topic/freopen_s,%20_wfreopen_s.md), [_fsopen](../Topic/_fsopen,%20_wfsopen.md) or [_sopen_s](../vs140/_sopen_s--_wsopen_s.md), you can override the current default setting of `_fmode` by specifying the appropriate argument to the function [_set_fmode](../vs140/_set_fmode.md). The `stdin`, `stdout`, and `stderr` streams always open in text mode by default; you can also override this default when opening any of these files. Use [_setmode](../vs140/_setmode.md) to change the translation mode using the file descriptor after the file is open.  
  
## See Also  
 [Input and Output](../vs140/Input-and-Output.md)   
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)