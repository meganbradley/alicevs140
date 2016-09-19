---
title: "Referencing a Property in Your Provider"
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
ms.assetid: bfbb3851-5eed-467a-a179-4a97a9515525
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Referencing a Property in Your Provider
Find the property group and property ID for the property you want. For more information, see [OLE DB Properties](https://msdn.microsoft.com/en-us/library/ms722734.aspx) in the *OLE DB Programmer's Reference*.  
  
 The following example assumes that you are trying to get a property from the rowset. The code for using the session or command is similar, but uses a different interface.  
  
 Create a [CDBPropSet](../vs140/CDBPropSet-Class.md) object using the property group as the parameter to the constructor. For example:  
  
```  
CDBPropSet propset(DBPROPSET_ROWSET);  
```  
  
 Call [AddProperty](../vs140/CDBPropSet--AddProperty.md), passing it the property ID and a value to be assigned to the property. The type of the value depends on the property you are using.  
  
```  
CDBPropSet propset(DBPROPSET_ROWSET);  
propset.AddProperty(DBPROP_IRowsetChange, true);  
propset.AddProperty(DBPROP_UPDATABILITY,  
DBPROPVAL_UP_INSERT | DBPROPVAL_UP_CHANGE | DBPROPVAL_UP_DELETE);  
```  
  
 Use the `IRowset` interface to call **GetProperties**. Pass the property set as a parameter. Here is the final code:  
  
```  
CAgentRowset<CMyProviderCommand>* pRowset = (CAgentRowset<CMyProviderCommand>*) pThis;  
  
CComQIPtr<IRowsetInfo, &IID_IRowsetInfo> spRowsetProps = pRowset;  
  
DBPROPIDSET set;  
set.AddPropertyID(DBPROP_BOOKMARKS);  
DBPROPSET* pPropSet = NULL;  
ULONG ulPropSet = 0;  
HRESULT hr;  
  
if (spRowsetProps)  
   hr = spRowsetProps->GetProperties(1, &set, &ulPropSet, &pPropSet);  
  
if (pPropSet)  
{  
   CComVariant var = pPropSet->rgProperties[0].vValue;  
   CoTaskMemFree(pPropSet->rgProperties);  
   CoTaskMemFree(pPropSet);  
  
   if (SUCCEEDED(hr) && (var.boolVal == VARIANT_TRUE))  
   {  
      ...  // Use property here  
   }  
}  
```  
  
## See Also  
 [Working with OLE DB Provider Templates](../vs140/Working-with-OLE-DB-Provider-Templates.md)