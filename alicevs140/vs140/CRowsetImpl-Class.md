---
title: "CRowsetImpl Class"
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
ms.assetid: e97614b3-b11d-4806-a0d3-b9401331473f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowsetImpl Class
Provides a standard OLE DB rowset implementation without requiring multiple inheritance of many implementation interfaces.  
  
## Syntax  
  
```  
template <  
   class T,  
   class Storage,  
   class CreatorClass,  
   class ArrayType = CAtlArray<Storage>,   
   class RowClass = CSimpleRow,   
   class RowsetInterface = IRowsetImpl < T, IRowset >   
>  
class CRowsetImpl :    
   public CComObjectRootEx<CreatorClass::_ThreadModel>,   
   public CRowsetBaseImpl<T, Storage, ArrayType, RowsetInterface>,   
   public IRowsetInfoImpl<T, CreatorClass::_PropClass>  
```  
  
#### Parameters  
 `T`  
 The user's class that derives from `CRowsetImpl`.  
  
 `Storage`  
 The user record class.  
  
 `CreatorClass`  
 The class that contains properties for the rowset; typically the command.  
  
 `ArrayType`  
 The class that will act as storage for the rowset's data. This parameter defaults to `CAtlArray`, but it can be any class that supports the required functionality.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[NameFromDBID](../vs140/CRowsetImpl--NameFromDBID.md)|Extracts a string from a **DBID** and copies it to the `bstr` passed in.|  
|[SetCommandText](../vs140/CRowsetImpl--SetCommandText.md)|Validates and stores the **DBID**s in the two strings ([m_strCommandText](../vs140/CRowsetImpl--m_strCommandText.md) and [m_strIndexText](../vs140/CRowsetImpl--m_strIndexText.md)).|  
  
### Overridable Methods  
  
|||  
|-|-|  
|[GetColumnInfo](../vs140/CRowsetImpl--GetColumnInfo.md)|Retrieves column information for a particular client request.|  
|[GetCommandFromID](../vs140/CRowsetImpl--GetCommandFromID.md)|Checks to see if either or both parameters contain string values, and if so, copies the string values to the data members [m_strCommandText](../vs140/CRowsetImpl--m_strCommandText.md) and [m_strIndexText](../vs140/CRowsetImpl--m_strIndexText.md).|  
|[ValidateCommandID](../vs140/CRowsetImpl--ValidateCommandID.md)|Checks to see if either or both **DBID**s contain string values, and if so, copies them to its data members [m_strCommandText](../vs140/CRowsetImpl--m_strCommandText.md) and [m_strIndexText](../vs140/CRowsetImpl--m_strIndexText.md).|  
  
### Data Members  
  
|||  
|-|-|  
|[m_rgRowData](../vs140/CRowsetImpl--m_rgRowData.md)|By default, a `CAtlArray` that templatizes on the user record template argument to `CRowsetImpl`. Another array type class can be used by changing the `ArrayType` template argument to `CRowsetImpl`.|  
|[m_strCommandText](../vs140/CRowsetImpl--m_strCommandText.md)|Contains the rowset's initial command.|  
|[m_strIndexText](../vs140/CRowsetImpl--m_strIndexText.md)|Contains the rowset's initial index.|  
  
## Remarks  
 `CRowsetImpl` provides overrides in the form of static upcasts. The methods control the manner in which a given rowset will validate command text. You can create your own `CRowsetImpl`-style class by making your implementation interfaces multiple-inherited. The only method for which you must provide implementation is **Execute**. Depending on what type of rowset you are creating, the creator methods will expect different signatures for **Execute**. For example, if you are using a `CRowsetImpl`-derived class to implement a schema rowset, the **Execute** method will have the following signature:  
  
 `HRESULT Execute(LONG* pcRows, ULONG cRestrictions, const VARIANT* rgRestrictions)`  
  
 If you are creating a `CRowsetImpl`-derived class to implement a command or session's rowset, the **Execute** method will have the following signature:  
  
 `HRESULT Execute(LONG* pcRows, DBPARAMS* pParams)`  
  
 To implement any of the `CRowsetImpl`-derived **Execute** methods, you must populate your internal data buffers ([m_rgRowData](../vs140/CRowsetImpl--m_rgRowData.md)).  
  
## Requirements  
 **Header:** atldb.h