---
title: "Text and Binary Streams"
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
ms.assetid: 57035e4a-955d-4e04-a560-fcf67ce68b4e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Text and Binary Streams
A text stream consists of one or more lines of text that can be written to a text-oriented display so that they can be read. When reading from a text stream, the program reads an `NL` (newline) at the end of each line. When writing to a text stream, the program writes an `NL` to signal the end of a line. To match differing conventions among target environments for representing text in files, the library functions can alter the number and representations of characters transmitted between the program and a text stream.  
  
 Thus, positioning within a text stream is limited. You can obtain the current file-position indicator by calling [fgetpos](../vs140/fgetpos.md) or [ftell](../vs140/ftell--_ftelli64.md). You can position a text stream at a position obtained this way, or at the beginning or end of the stream, by calling [fsetpos](../vs140/fsetpos.md) or [fseek](../vs140/fseek--_fseeki64.md). Any other change of position might well be not supported.  
  
 For maximum portability, the program should not write:  
  
-   Empty files.  
  
-   Space characters at the end of a line.  
  
-   Partial lines (by omitting the `NL` at the end of a file).  
  
-   characters other than the printable characters, NL, and `HT` (horizontal tab).  
  
 If you follow these rules, the sequence of characters you read from a text stream (either as byte or multibyte characters) will match the sequence of characters you wrote to the text stream when you created the file. Otherwise, the library functions can remove a file you create if the file is empty when you close it. Or they can alter or delete characters you write to the file.  
  
 A binary stream consists of one or more bytes of arbitrary information. You can write the value stored in an arbitrary object to a (byte-oriented) binary stream and read exactly what was stored in the object when you wrote it. The library functions do not alter the bytes you transmit between the program and a binary stream. They can, however, append an arbitrary number of null bytes to the file that you write with a binary stream. The program must deal with these additional null bytes at the end of any binary stream.  
  
 Thus, positioning within a binary stream is well defined, except for positioning relative to the end of the stream. You can obtain and alter the current file-position indicator the same as for a text stream. Moreover, the offsets used by [ftell](../vs140/ftell--_ftelli64.md) and [fseek](../vs140/fseek--_fseeki64.md) count bytes from the beginning of the stream (which is byte zero), so integer arithmetic on these offsets yields predictable results.  
  
 A byte stream treats a file as a sequence of bytes. Within the program, the stream looks like the same sequence of bytes, except for the possible alterations described above.  
  
## See Also  
 [Files and Streams](../vs140/Files-and-Streams.md)