---
title: "space_info Structure"
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
ms.assetid: f2b35b42-06ff-45bd-8617-39a0f5358a54
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# space_info Structure
Holds information about a volume.  
  
## Syntax  
  
```  
struct space_info;  
```  
  
## Members  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|`unsigned long long available`|Represents the number of bytes that are available to represent data on the volume.|  
|`unsigned long long capacity`|Represents the total number of bytes that the volume can represent.|  
|`unsigned long long free`|Represents the number of bytes that are not used to represent data on the volume.|  
  
## Requirements  
 **Header:** filesystem  
  
 **Namespace:** std::tr2::sys  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<filesystem\>](../vs140/-filesystem-.md)   
 [space Function](assetId:///7fce0b0e-523b-4598-b218-47245d0204ca)   
 [File System Navigation](../vs140/File-System-Navigation.md)