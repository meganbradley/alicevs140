---
title: "file_type Enumeration"
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
ms.assetid: a6a35986-167a-4142-9de4-ccfe5c1576f8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# file_type Enumeration
An enumeration for file types. The supported values are regular, and directory, not_found and unknown.  
  
## Syntax  
  
```  
enum file_type;  
```  
  
## Values  
  
|Name|Value|Description|  
|----------|-----------|-----------------|  
|`not_found`|-1|Represents a file that does not exist.|  
|`none`|0|Represents a file that has no type attribute. (Not supported.)|  
|`regular`|1|Represents a conventional disk file.|  
|`directory`|2|Represents a directory.|  
|`symlink`|3|Represents a symbolic link. (Not supported.)|  
|`block`|4|Represents a block-special file on UNIX-based systems. (Not supported.)|  
|`character`|5|Represents a character-special file on UNIX-based systems. (Not supported.)|  
|`fifo`|6|Represents a FIFO file on UNIX-based systems. (Not supported.)|  
|`socket`|7|Represents a socket on UNIX based systems. (Not supported.)|  
|`unknown`|8|Represents a file whose status cannot be determined.|  
  
## Requirements  
 **Header:** filesystem  
  
 **Namespace:** std::tr2::sys  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<filesystem\>](../vs140/-filesystem-.md)   
 [file_status Class](../vs140/file_status-Class.md)