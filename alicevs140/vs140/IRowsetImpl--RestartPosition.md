---
title: "IRowsetImpl::RestartPosition"
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
ms.assetid: 14de66ef-8d2c-4404-adb6-3f6c74ac6cf1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRowsetImpl::RestartPosition
Repositions the next fetch position to its initial position; that is, its position when the rowset was first created.  
  
## Syntax  
  
```  
  
      STDMETHOD( RestartPosition )(  
   HCHAPTER /* hReserved */   
);  
```  
  
#### Parameters  
 See [IRowset::RestartPosition](https://msdn.microsoft.com/en-us/library/ms712877.aspx) in the *OLE DB Programmer's Reference*.  
  
## Remarks  
 The rowset position is undefined until **GetNextRow** is called. You can move backwards in a rowet by calling [RestartPosition](#vcrefirowsetimplrestartposition) and then fetching or scrolling backwards.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IRowsetImpl Class](../vs140/IRowsetImpl-Class.md)