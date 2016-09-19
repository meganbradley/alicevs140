---
title: "CDBPropSet::AddProperty"
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
ms.assetid: dc9539d3-1ee4-40f3-9281-2068e6d65e93
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDBPropSet::AddProperty
Adds a property to the property set.  
  
## Syntax  
  
```  
  
      bool AddProperty(   
   DWORD dwPropertyID,   
   const VARIANT& var,   
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
bool AddProperty(  
   DWORD dwPropertyID,  
   LPCSTR szValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
bool AddProperty(  
   DWORD dwPropertyID,  
   LPCWSTR szValue,   
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
bool AddProperty(  
   DWORD dwPropertyID,  
   bool bValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
bool AddProperty(  
   DWORD dwPropertyID,  
   BYTE bValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
);  
bool AddProperty(  
   DWORD dwPropertyID,  
   short nValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
);  
bool AddProperty(  
   DWORD dwPropertyID,  
   long nValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
);  
bool AddProperty(  
   DWORD dwPropertyID,  
   float fltValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
);  
bool AddProperty(  
   DWORD dwPropertyID,  
   double dblValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
bool AddProperty(  
   DWORD dwPropertyID,  
   CY cyValue,  
   DBPROPOPTIONS propoptions = DBPROPOPTIONS_REQUIRED    
) throw( );  
```  
  
#### Parameters  
 *dwPropertyID*  
 [in] The ID of the property to be added. Used to initialize the **dwPropertyID** of the `DBPROP` structure added to the property set.  
  
 `var`  
 [in] A variant used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 `szValue`  
 [in] A string used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 `bValue`  
 [in] A **BYTE** or boolean value used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 `nValue`  
 [in] An integer value used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 *fltValue*  
 [in] A floating-point value used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 `dblValue`  
 [in] A double-precision floating-point value used to initialize the property value for the `DBPROP` structure added to the property set.  
  
 `cyValue`  
 [in] A CY currency value used to initialize the property value for the `DBPROP` structure added to the property set.  
  
## Return Value  
 **true** if the property was successfully added. Otherwise, **false**.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CDBPropSet Class](../vs140/CDBPropSet-Class.md)   
 [DBPROP Structure](https://msdn.microsoft.com/en-us/library/ms717970.aspx)