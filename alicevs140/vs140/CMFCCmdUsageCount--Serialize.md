---
title: "CMFCCmdUsageCount::Serialize"
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
ms.assetid: 6d06bd6d-74f9-48f2-96d9-0d568cb72a00
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCmdUsageCount::Serialize
Reads this object from an archive, or writes it to an archive.  
  
## Syntax  
  
```  
virtual void Serialize(  
   CArchive& ar  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `ar`|A `CArchive` object to serialize from or to.|  
  
## Remarks  
 This method serializes the map structure of command counts, `m_CmdUsage`, and the total command usage, `m_nTotalUsage`, counter from or to the specified archive.  
  
 For serialization examples, see [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md).  
  
## Requirements  
 **Header:** afxcmdusagecount.h  
  
## See Also  
 [CMFCCmdUsageCount Class](../vs140/CMFCCmdUsageCount-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md)