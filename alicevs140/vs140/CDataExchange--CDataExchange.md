---
title: "CDataExchange::CDataExchange"
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
ms.assetid: d8c3dd91-f989-4daf-8152-fdbf132042e7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDataExchange::CDataExchange
Call this member function to construct a `CDataExchange` object.  
  
## Syntax  
  
```  
  
      CDataExchange(  
   CWnd* pDlgWnd,  
   BOOL bSaveAndValidate   
);  
```  
  
#### Parameters  
 *pDlgWnd*  
 A pointer to the parent window that contains the control. Usually this is a [CDialog](../vs140/CDialog-Class.md)-derived object.  
  
 `bSaveAndValidate`  
 If **TRUE**, this object validates data, then writes data from the controls to the members. If **FALSE**, this object will move data from members to controls.  
  
## Remarks  
 Construct a `CDataExchange` object yourself to store extra information in the data exchange object to pass to your window's [CWnd::DoDataExchange](../vs140/CWnd--DoDataExchange.md) member function.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#70](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#70)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDataExchange Class](../vs140/CDataExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)