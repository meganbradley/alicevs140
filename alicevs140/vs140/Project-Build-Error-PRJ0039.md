---
title: "Project Build Error PRJ0039"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 207bbc28-922f-44d6-8bdd-3016c850f5b9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0039
Unable to create a temporary file. The ability to do this is required in order for the NMake tool to be able to run.  
  
 When building a makefile project (see [Creating a Makefile Project](../vs140/Creating-a-Makefile-Project.md)), the Visual C++ project system needs to create some temporary files. This error indicates that the project system was unable to create one or more of those files.  
  
 The TMP environment variable contains the name of the temp directory.  
  
 Possible causes for this error, and suggested resolutions, are listed below:  
  
 User doesn't have write access to temp directory  
 Make sure you have write access to the temp directory.  
  
 Too many temp files in temp directory  
 Other processes may have created temp files, but not deleted them. Delete some or all of these temp files.  
  
 No free disk space  
 Delete some files on your disk or change your temp directory to a disk with free space.  
  
 TMP environment variable is bad  
 It is possible that the TMP environment variable points to a directory that does not exist.