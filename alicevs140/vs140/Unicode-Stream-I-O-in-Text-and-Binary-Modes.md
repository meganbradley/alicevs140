---
title: "Unicode Stream I-O in Text and Binary Modes"
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
H1: Unicode Stream I/O in Text and Binary Modes
ms.assetid: 68be0c3e-a9e6-4fd5-b34a-1b5207f0e7d6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Unicode Stream I-O in Text and Binary Modes
When a Unicode stream I/O routine (such as `fwprintf`, `fwscanf`, `fgetwc`, `fputwc`, `fgetws`, or `fputws`) operates on a file that is open in text mode (the default), two kinds of character conversions take place:  
  
-   Unicode-to-MBCS or MBCS-to-Unicode conversion. When a Unicode stream-I/O function operates in text mode, the source or destination stream is assumed to be a sequence of multibyte characters. Therefore, the Unicode stream-input functions convert multibyte characters to wide characters (as if by a call to the `mbtowc` function). For the same reason, the Unicode stream-output functions convert wide characters to multibyte characters (as if by a call to the `wctomb` function).  
  
-   Carriage return – linefeed (CR-LF) translation. This translation occurs before the MBCS – Unicode conversion (for Unicode stream input functions) and after the Unicode – MBCS conversion (for Unicode stream output functions). During input, each carriage return – linefeed combination is translated into a single linefeed character. During output, each linefeed character is translated into a carriage return – linefeed combination.  
  
 However, when a Unicode stream-I/O function operates in binary mode, the file is assumed to be Unicode, and no CR-LF translation or character conversion occurs during input or output. Use the _setmode( _fileno( stdin ), _O_BINARY ); instruction in order to correctly use wcin on a UNICODE text file.  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)   
 [Input and Output](../vs140/Input-and-Output.md)