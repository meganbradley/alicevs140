---
title: "Fetching Data"
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
ms.assetid: b07f747f-9855-4f27-a03d-b1d5b10fa284
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fetching Data
After you open the data source, session, and rowset objects, you can fetch data. Depending on the type of accessor you are using, you might need to bind columns.  
  
### To fetch data  
  
1.  Open the rowset using the appropriate **Open** command.  
  
2.  If you are using `CManualAccessor`, bind the output columns if you have not already done so. To bind the columns, call `GetColumnInfo`, and then create an accessor with the bindings, as shown in the following example:  
  
    ```  
    // From the DBViewer Sample CDBTreeView::OnQueryEdit  
    // Get the column information  
    ULONG ulColumns       = 0;  
    DBCOLUMNINFO* pColumnInfo  = NULL;  
    LPOLESTR pStrings      = NULL;  
    if (rs.GetColumnInfo(&ulColumns, &pColumnInfo, &pStrings) != S_OK)  
        ThrowMyOLEDBException(rs.m_pRowset, IID_IColumnsInfo);  
    struct MYBIND* pBind = new MYBIND[ulColumns];  
    rs.CreateAccessor(ulColumns, &pBind[0], sizeof(MYBIND)*ulColumns);  
    for (ULONG l=0; l<ulColumns; l++)  
    rs.AddBindEntry(l+1, DBTYPE_STR, sizeof(TCHAR)*40, &pBind[l].szValue, NULL, &pBind[l].dwStatus);  
    rs.Bind();  
    ```  
  
3.  Write a `while` loop to retrieve the data. In the loop, call `MoveNext` to advance the cursor and test the return value against S_OK, as shown in the following example:  
  
    ```  
    while (rs.MoveNext() == S_OK)  
    {  
        // Add code to fetch data here  
        // If you are not using an auto accessor, call rs.GetData()  
    }  
    ```  
  
4.  Within the `while` loop, you can fetch the data according to your accessor type.  
  
    -   If you use the [CAccessor](../vs140/CAccessor-Class.md) class, you should have a user record that contains data members. You can access your data using those data members, as shown in the following example:  
  
        ```  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the data members directly. In this case, m_nFooID  
            // is declared in a user record that derives from  
            // CAccessor  
            wsprintf_s("%d", rs.m_nFooID);   
        }  
        ```  
  
    -   If you use the `CDynamicAccessor` or `CDynamicParameterAccessor` class, you can fetch data by using the accessing functions `GetValue` and `GetColumn`, as shown in the following example. If you want to determine the type of data you are using, use `GetType`.  
  
        ```  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the dynamic accessor functions to retrieve your data.  
  
            ULONG ulColumns = rs.GetColumnCount();  
            for (ULONG i=0; i<ulColumns; i++)  
            {  
                rs.GetValue(i);  
            }  
        }  
        ```  
  
    -   If you use `CManualAccessor`, you must specify your own data members, bind them yourself, and access them directly, as shown in the following example:  
  
        ```  
        while (rs.MoveNext() == S_OK)  
        {  
            // Use the data members you specified in the calls to  
            // AddBindEntry.  
  
            wsprintf_s("%s", szFoo);  
        }  
        ```  
  
## See Also  
 [Working with OLE DB Consumer Templates](../vs140/Working-with-OLE-DB-Consumer-Templates.md)