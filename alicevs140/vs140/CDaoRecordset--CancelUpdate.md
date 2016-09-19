---
title: "CDaoRecordset::CancelUpdate"
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
ms.assetid: ca37a873-1156-4bea-8da5-2aa0a53a615b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::CancelUpdate
The `CancelUpdate` member function cancels any pending updates due to an [Edit](../vs140/CDaoRecordset--Edit.md) or [AddNew](../vs140/CDaoRecordset--AddNew.md) operation.  
  
## Syntax  
  
```  
  
virtual void CancelUpdate( );  
  
```  
  
## Remarks  
 For example, if an application calls the **Edit** or `AddNew` member function and has not called [Update](../vs140/CDaoRecordset--Update.md), `CancelUpdate` cancels any changes made after **Edit** or `AddNew` was called.  
  
> [!NOTE]
>  If records are double-buffered (that is, automatic field checking is enabled), calling `CancelUpdate` will restore the member variables to the values they had before `AddNew` or **Edit** was called.  
  
 If there is no **Edit** or `AddNew` operation pending, `CancelUpdate` causes MFC to throw an exception. Call the [GetEditMode](../vs140/CDaoRecordset--GetEditMode.md) member function to determine if there is a pending operation that can be canceled.  
  
 For related information, see the topic "CancelUpdate Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::AddNew](../vs140/CDaoRecordset--AddNew.md)   
 [CDaoRecordset::Delete](../vs140/CDaoRecordset--Delete.md)   
 [CDaoRecordset::Edit](../vs140/CDaoRecordset--Edit.md)   
 [CDaoRecordset::Update](../vs140/CDaoRecordset--Update.md)   
 [CDaoRecordset::CanTransact](../vs140/CDaoRecordset--CanTransact.md)