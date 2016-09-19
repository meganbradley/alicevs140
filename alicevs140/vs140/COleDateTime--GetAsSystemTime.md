---
title: "COleDateTime::GetAsSystemTime"
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
ms.assetid: 6f80b751-5d2e-4fd9-a5a6-a87ac9db5bbf
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::GetAsSystemTime
Call this method to obtain the time in the `COleDateTime` object as a `SYSTEMTIME` data structure.  
  
## Syntax  
  
```  
  
      bool GetAsSystemTime(  
   SYSTEMTIME& sysTime   
) const throw( );  
```  
  
#### Parameters  
 *sysTime*  
 A reference to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure to receive the converted date/time value from the `COleDateTime` object.  
  
## Return Value  
 Returns **true** if successful; **false** if the conversion fails, or if the `COleDateTime` object is **NULL** or invalid.  
  
## Remarks  
 `GetAsSystemTime` stores the resulting time in the referenced *sysTime* object. The `SYSTEMTIME` data structure initialized by this function will have its **wMilliseconds** member set to zero.  
  
 See [GetStatus](../vs140/COleDateTime--GetStatus.md) for more information on the status information held in a `COleDateTime` object.  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)