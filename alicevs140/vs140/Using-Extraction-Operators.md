---
title: "Using Extraction Operators"
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
ms.assetid: a961e1a9-4897-41de-b210-89d5b2d051ae
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Extraction Operators
The extraction operator (`>>`), which is preprogrammed for all standard C++ data types, is the easiest way to get bytes from an input stream object.  
  
 Formatted text input extraction operators depend on white space to separate incoming data values. This is inconvenient when a text field contains multiple words or when commas separate numbers. In such a case, one alternative is to use the unformatted input member function [istream::getline](../vs140/basic_istream--getline.md) to read a block of text with white space included, then parse the block with special functions. Another method is to derive an input stream class with a member function such as `GetNextToken`, which can call istream members to extract and format character data.  
  
## See Also  
 [Input Streams](../vs140/Input-Streams.md)