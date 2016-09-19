---
title: "DDX_Text"
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
ms.assetid: 87677d45-9df7-4ff8-af6a-8ba1e0cb1172
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DDX_Text
The `DDX_Text` function manages the transfer of `int`, **UINT**, **long**, `DWORD`, `CString`, **float**, or **double** data between an edit control in a dialog box, form view, or control view and a [CString](../vs140/CStringT-Class.md) data member of the dialog box, form view, or control view object.  
  
## Syntax  
  
```  
  
      void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   BYTE& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   short& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   int& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   UINT& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   long& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   DWORD& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   CString& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   float& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   double& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   COleCurrency& value   
);  
void AFXAPI DDX_Text(  
   CDataExchange* pDX,  
   int nIDC,  
   COleDateTime& value   
);  
```  
  
#### Parameters  
 `pDX`  
 A pointer to a [CDataExchange](../vs140/CDataExchange-Class.md) object. The framework supplies this object to establish the context of the data exchange, including its direction.  
  
 `nIDC`  
 The ID of an edit control in the dialog box, form view, or control view object.  
  
 *value*  
 A reference to a data member in the dialog box, form view, or control view object. The data type of *value* depends on which of the overloaded versions of `DDX_Text` you use.  
  
## Remarks  
 For more information about DDX, see [Dialog Data Exchange and Validation](../vs140/Dialog-Data-Exchange-and-Validation.md).  
  
## Requirements  
 **Header:** afxdd_.h  
  
## See Also  
 [Standard Dialog Data Exchange Routines](../vs140/Standard-Dialog-Data-Exchange-Routines.md)   
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)