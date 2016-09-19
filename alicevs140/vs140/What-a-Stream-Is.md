---
title: "What a Stream Is"
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
ms.assetid: a7e661e9-6cd1-4543-a9a4-c58ee9fd32f3
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# What a Stream Is
Like C, C++ does not have built-in input/output capability. All C++ compilers, however, come bundled with a systematic, object-oriented I/O package, known as the iostream classes. The stream is the central concept of the iostream classes. You can think of a stream object as a smart file that acts as a source and destination for bytes. A stream's characteristics are determined by its class and by customized insertion and extraction operators.  
  
 Through device drivers, the disk operating system deals with the keyboard, screen, printer, and communication ports as extended files. The iostream classes interact with these extended files. Built-in classes support reading from and writing to memory with syntax identical to that for disk I/O, which makes it easy to derive stream classes.  
  
## In This Section  
 [Input/Output Alternatives](../vs140/Input-Output-Alternatives.md)  
  
## See Also  
 [iostream Programming](../vs140/iostream-Programming.md)