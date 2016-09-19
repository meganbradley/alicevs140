---
title: "Combo Box Handlers"
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
ms.assetid: 7f092412-01b7-4242-95ec-41ba506b9d71
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Combo Box Handlers
The following map entries correspond to the function prototypes.  
  
|Map entry|Function prototype|  
|---------------|------------------------|  
|ON_CBN_CLOSEUP( <id\>, <memberFxn\> )|afx_msg void memberFxn( )|  
|ON_CBN_DBLCLK( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_DROPDOWN( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_EDITCHANGE( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_EDITUPDATE( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_ERRSPACE( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_KILLFOCUS( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_SELCHANGE( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_SELENDCANCEL( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_SELENDOK( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
|ON_CBN_SETFOCUS( <id\>, <memberFxn\> )|afx_msg void memberFxn( );|  
  
## See Also  
 [Message Maps](../vs140/Message-Maps--MFC-.md)