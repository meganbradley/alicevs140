---
title: "CDaoDatabase::CDaoDatabase"
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
ms.assetid: 849e6244-6a2f-4d0c-9e2e-dfffe47f6b02
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::CDaoDatabase
Constructs a `CDaoDatabase` object.  
  
## Syntax  
  
```  
  
      CDaoDatabase(  
  CDaoWorkspace* pWorkspace = NULL   
);  
```  
  
#### Parameters  
 *pWorkspace*  
 A pointer to the `CDaoWorkspace` object that will contain the new database object. If you accept the default value of **NULL**, the constructor creates a temporary `CDaoWorkspace` object that uses the default DAO workspace. You can get a pointer to the workspace object via the [m_pWorkspace](../vs140/CDaoDatabase--m_pWorkspace.md) data member.  
  
## Remarks  
 After constructing the object, if you are creating a new Microsoft Jet (.MDB) database, call the object's [Create](../vs140/CDaoDatabase--Create.md) member function. If you are, instead, opening an existing database, call the object's [Open](../vs140/CDaoDatabase--Open.md) member function.  
  
 When you finish with the object, you should call its [Close](../vs140/CDaoDatabase--Close.md) member function and then destroy the `CDaoDatabase` object.  
  
 You might find it convenient to embed the `CDaoDatabase` object in your document class.  
  
> [!NOTE]
>  A `CDaoDatabase` object is also created implicitly if you open a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object without passing a pointer to an existing `CDaoDatabase` object. This database object is closed when you close the recordset object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)