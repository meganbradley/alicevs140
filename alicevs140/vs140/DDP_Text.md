---
title: "DDP_Text"
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
ms.assetid: 1c08d2f1-b387-4d67-a58a-d0ed01b6cb23
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDP_Text
Call this function in your control's `DoDataExchange` function to synchronize the value of the property with the associated property page control.  
  
## Syntax  
  
```  
  
      void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   BYTE &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   int &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   UINT &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   long &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   DWORD &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   float &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   double &member,  
   LPCTSTR pszPropName   
);  
void AFXAPI DDP_Text(  
   CDataExchange*pDX,  
   int id,  
   CString &member,  
   LPCTSTR pszPropName   
);  
```  
  
#### Parameters  
 `pDX`  
 Pointer to a `CDataExchange` object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `id`  
 The resource ID of the control associated with the control property specified by `pszPropName`.  
  
 `member`  
 The member variable associated with the property page control specified by `id` and the property specified by `pszPropName`.  
  
 `pszPropName`  
 The property name of the control property to be exchanged with the control specified by `id`.  
  
## Remarks  
 This function should be called before the corresponding `DDX_Text` function call.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DDP_Check](../vs140/DDP_Check.md)   
 [DDP_Radio](../vs140/DDP_Radio.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [DDX_Text](../vs140/DDX_Text.md)