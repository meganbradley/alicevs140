---
title: "CTime::GetAsSystemTime"
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
ms.topic: reference
ms.assetid: 544c79fd-12af-4c80-a83c-2a8909126fff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetAsSystemTime
Call this member function to convert the time information stored in the `CTime` object to a Win32–compatible [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure.  
  
## Syntax  
  
```  
  
      bool GetAsSystemTime(  
   SYSTEMTIME& st   
) const throw( );  
```  
  
#### Parameters  
 *timeDest*  
 A reference to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that will hold the converted date/time value of the `CTime` object.  
  
## Return Value  
 True if successful; otherwise false.  
  
## Remarks  
 `GetAsSystemTime` stores the resulting time in the referenced *timeDest* structure. The `SYSTEMTIME` data structure initialized by this function will have its **wMilliseconds** member set to zero.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#151](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#151)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)