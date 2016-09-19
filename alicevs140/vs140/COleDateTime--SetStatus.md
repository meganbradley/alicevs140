---
title: "COleDateTime::SetStatus"
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
ms.assetid: 0bc272bb-d37d-4e19-94eb-35dff49b1829
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDateTime::SetStatus
Sets the status of this `COleDateTime` object.  
  
## Syntax  
  
```  
  
      void SetStatus(  
   DateTimeStatus status   
) throw( );  
```  
  
#### Parameters  
 *status*  
 The new status value for this `COleDateTime` object.  
  
## Remarks  
 The *status* parameter value is defined by the **DateTimeStatus** enumerated type, which is defined within the `COleDateTime` class. See [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md) for details.  
  
> [!CAUTION]
>  This function is for advanced programming situations. This function does not alter the data in this object. It will most often be used to set the status to `null` or **invalid**. Note that the assignment operator ([operator =](../vs140/COleDateTime--operator-=.md)) and [SetDateTime](../vs140/COleDateTime--SetDateTime.md) do set the status of the object based on the source value(s).  
  
## Example  
 See the example for [GetStatus](../vs140/COleDateTime--GetStatus.md).  
  
## Requirements  
 **Header:** atlcomtime.h  
  
## See Also  
 [COleDateTime Class](../vs140/COleDateTime-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDateTime::GetStatus](../vs140/COleDateTime--GetStatus.md)   
 [COleDateTime::operator =](../vs140/COleDateTime--operator-=.md)   
 [COleDateTime::SetDateTime](../vs140/COleDateTime--SetDateTime.md)   
 [COleDateTime::m_dt](../vs140/COleDateTime--m_dt.md)