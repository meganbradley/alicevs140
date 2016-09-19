---
title: "AfxDaoInit"
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
ms.assetid: ce6a6d77-c2c1-4724-90da-f7993ec153ff
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxDaoInit
This function initializes the DAO database engine.  
  
## Syntax  
  
```  
  
      void AfxDaoInit( );  
throw(  
   CDaoException*   
);  
```  
  
## Remarks  
 In most cases, you don't need to call `AfxDaoInit` because the application automatically calls it when it is needed.  
  
 For related information, and for an example of calling `AfxDaoInit`, see [Technical Note 54](../vs140/TN054--Calling-DAO-Directly-While-Using-MFC-DAO-Classes.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxDaoTerm](../vs140/AfxDaoTerm.md)