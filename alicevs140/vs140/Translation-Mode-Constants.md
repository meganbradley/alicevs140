---
title: "Translation Mode Constants"
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
ms.assetid: a5993bf4-7e7a-47f9-83c3-e46332b85579
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Translation Mode Constants
## Syntax  
  
```  
  
#include <fcntl.h>  
  
```  
  
## Remarks  
 The `_O_BINARY` and `_O_TEXT` manifest constants determine the translation mode for files (`_open` and `_sopen`) or the translation mode for streams (`_setmode`).  
  
 The allowed values are:  
  
 `_O_TEXT`  
 Opens file in text (translated) mode. Carriage return – linefeed (CR-LF) combinations are translated into a single linefeed (LF) on input. Linefeed characters are translated into CR-LF combinations on output. Also, CTRL+Z is interpreted as an end-of-file character on input. In files opened for reading and reading/writing, `fopen` checks for CTRL+Z at the end of the file and removes it, if possible. This is done because using the `fseek` and `ftell` functions to move within a file ending with CTRL+Z may cause `fseek` to behave improperly near the end of the file.  
  
 `_O_BINARY`  
 Opens file in binary (untranslated) mode. The above translations are suppressed.  
  
 `_O_RAW`  
 Same as `_O_BINARY`. Supported for C 2.0 compatibility.  
  
 For more information, see [Text and Binary Mode File I/O](../vs140/Text-and-Binary-Mode-File-I-O.md) and [File Translation](../vs140/File-Translation-Constants.md).  
  
## See Also  
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_pipe](../vs140/_pipe.md)   
 [_sopen, _wsopen](../vs140/_sopen--_wsopen.md)   
 [_setmode](../vs140/_setmode.md)   
 [Global Constants](../vs140/Global-Constants.md)