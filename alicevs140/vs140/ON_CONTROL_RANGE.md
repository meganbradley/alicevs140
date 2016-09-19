---
title: "ON_CONTROL_RANGE"
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
ms.assetid: 46f0e1bb-569b-4b8b-9b80-89701d1cd7fd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_CONTROL_RANGE
Use this macro to map a contiguous range of control IDs to a single message handler function for a specified Windows notification message, such as **BN_CLICKED**.  
  
## Syntax  
  
```  
  
ON_CONTROL_RANGE(  
wNotifyCode  
,   
id1  
,   
id2  
,   
memberFxn )  
```  
  
#### Parameters  
 `wNotifyCode`  
 The notification code to which your handler is responding.  
  
 *id1*  
 Command ID at the beginning of a contiguous range of control IDs.  
  
 `id2`  
 Command ID at the end of a contiguous range of control IDs.  
  
 `memberFxn`  
 The name of the message-handler function to which the controls are mapped.  
  
## Remarks  
 The range of IDs starts with *id1* and ends with `id2`. The handler is called for the specified notification coming from any of the mapped controls.  
  
 There is no automatic support for message map ranges, so you must place the macro yourself.  
  
 For more information on implementing handler functions for a range of control IDs, refer to [Handlers for Message-Map Ranges](../vs140/Handlers-for-Message-Map-Ranges.md).  
  
## Requirements  
 **Header:** afxmsg_.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_UPDATE_COMMAND_UI_RANGE](../vs140/ON_UPDATE_COMMAND_UI_RANGE.md)   
 [ON_COMMAND_RANGE](../vs140/ON_COMMAND_RANGE.md)