---
title: "Project Build Error PRJ0035"
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
ms.assetid: 0667116d-338c-40a4-972c-da875f778cb5
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0035
XML file 'file' contains Unicode contents that could not be translated to user's ANSI code page.  
  
 ***UNICODE contents of file***  
  
 ***file***  is the XML file created as the command line to the Web Deployment tool.  
  
 The project system found Unicode characters in some property on the Web Deployment property page that can't properly be translated to ANSI.  
  
 The resolution for this error is to update the contents of the property to use ANSI or to install the code page on your computer and set it as the system default.