---
title: "How to: Join Two Collections (LINQ to XML) (C#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b817ede-911a-4cff-9dd3-639c3fc228c9
caps.latest.revision: 5
---
# How to: Join Two Collections (LINQ to XML) (C#)
An element or attribute in an XML document can sometimes refer to another element or attribute. For example, the [Sample XML File: Customers and Orders (LINQ to XML)](../vs140/Sample-XML-File--Customers-and-Orders--LINQ-to-XML-2.md) XML document contains a list of customers and a list of orders. Each `Customer` element contains a `CustomerID` attribute. Each `Order` element contains a `CustomerID` element. The `CustomerID` element in each order refers to the `CustomerID` attribute in a customer.  
  
 The topic [Sample XSD File: Customers and Orders](../vs140/Sample-XSD-File--Customers-and-Orders1.md) contains an XSD that can be used to validate this document. It uses the `xs:key` and `xs:keyref` features of XSD to establish that the `CustomerID` attribute of the `Customer` element is a key, and to establish a relationship between the `CustomerID` element in each `Order` element and the `CustomerID` attribute in each `Customer` element.  
  
 With [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)], you can take advantage of this relationship by using the `join` clause.  
  
 Note that because there is no index available, such joining will have poor runtime performance.  
  
 For more detailed information about `join`, see [Join Operations (C#)](../Topic/Join%20Operations%20\(C%23\).md).  
  
## Example  
 The following example joins the `Customer` elements to the `Order` elements, and generates a new XML document that includes the `CompanyName` element in the orders.  
  
 Before executing the query, the example validates that the document complies with the schema in [Sample XSD File: Customers and Orders](../vs140/Sample-XSD-File--Customers-and-Orders1.md). This ensures that the join clause will always work.  
  
 This query first retrieves all `Customer` elements, and then joins them to the `Order` elements. It selects only the orders for customers with a `CustomerID` greater than "K". It then projects a new `Order` element that contains the customer information within each order.  
  
 This example uses the following XML document: [Sample XML File: Customers and Orders (LINQ to XML)](../vs140/Sample-XML-File--Customers-and-Orders--LINQ-to-XML-2.md).  
  
 This example uses the following XSD schema: [Sample XSD File: Customers and Orders](../vs140/Sample-XSD-File--Customers-and-Orders1.md).  
  
 Note that joining in this fashion will not perform very well. Joins are performed via a linear search. There are no hash tables or indexes to help with performance.  
  
```c#  
XmlSchemaSet schemas = new XmlSchemaSet();  
schemas.Add("", "CustomersOrders.xsd");  
  
Console.Write("Attempting to validate, ");  
XDocument custOrdDoc = XDocument.Load("CustomersOrders.xml");  
  
bool errors = false;  
custOrdDoc.Validate(schemas, (o, e) =>  
                     {  
                         Console.WriteLine("{0}", e.Message);  
                         errors = true;  
                     });  
Console.WriteLine("custOrdDoc {0}", errors ? "did not validate" : "validated");  
  
if (!errors)  
{  
    // Join customers and orders, and create a new XML document with  
    // a different shape.  
  
    // The new document contains orders only for customers with a  
    // CustomerID > 'K'  
    XElement custOrd = custOrdDoc.Element("Root");  
    XElement newCustOrd = new XElement("Root",  
        from c in custOrd.Element("Customers").Elements("Customer")  
        join o in custOrd.Element("Orders").Elements("Order")  
                   on (string)c.Attribute("CustomerID") equals  
                      (string)o.Element("CustomerID")  
        where ((string)c.Attribute("CustomerID")).CompareTo("K") > 0  
        select new XElement("Order",  
            new XElement("CustomerID", (string)c.Attribute("CustomerID")),  
            new XElement("CompanyName", (string)c.Element("CompanyName")),  
            new XElement("ContactName", (string)c.Element("ContactName")),  
            new XElement("EmployeeID", (string)o.Element("EmployeeID")),  
            new XElement("OrderDate", (DateTime)o.Element("OrderDate"))  
        )  
    );  
    Console.WriteLine(newCustOrd);  
}  
```  
  
 This code produces the following output:  
  
```  
Attempting to validate, custOrdDoc validated  
<Root>  
  <Order>  
    <CustomerID>LAZYK</CustomerID>  
    <CompanyName>Lazy K Kountry Store</CompanyName>  
    <ContactName>John Steel</ContactName>  
    <EmployeeID>1</EmployeeID>  
    <OrderDate>1997-03-21T00:00:00</OrderDate>  
  </Order>  
  <Order>  
    <CustomerID>LAZYK</CustomerID>  
    <CompanyName>Lazy K Kountry Store</CompanyName>  
    <ContactName>John Steel</ContactName>  
    <EmployeeID>8</EmployeeID>  
    <OrderDate>1997-05-22T00:00:00</OrderDate>  
  </Order>  
  <Order>  
    <CustomerID>LETSS</CustomerID>  
    <CompanyName>Let's Stop N Shop</CompanyName>  
    <ContactName>Jaime Yorres</ContactName>  
    <EmployeeID>1</EmployeeID>  
    <OrderDate>1997-06-25T00:00:00</OrderDate>  
  </Order>  
  <Order>  
    <CustomerID>LETSS</CustomerID>  
    <CompanyName>Let's Stop N Shop</CompanyName>  
    <ContactName>Jaime Yorres</ContactName>  
    <EmployeeID>8</EmployeeID>  
    <OrderDate>1997-10-27T00:00:00</OrderDate>  
  </Order>  
  <Order>  
    <CustomerID>LETSS</CustomerID>  
    <CompanyName>Let's Stop N Shop</CompanyName>  
    <ContactName>Jaime Yorres</ContactName>  
    <EmployeeID>6</EmployeeID>  
    <OrderDate>1997-11-10T00:00:00</OrderDate>  
  </Order>  
  <Order>  
    <CustomerID>LETSS</CustomerID>  
    <CompanyName>Let's Stop N Shop</CompanyName>  
    <ContactName>Jaime Yorres</ContactName>  
    <EmployeeID>4</EmployeeID>  
    <OrderDate>1998-02-12T00:00:00</OrderDate>  
  </Order>  
</Root>  
```  
  
## See Also  
 [Advanced Query Techniques (LINQ to XML) (C#)](../vs140/Advanced-Query-Techniques--LINQ-to-XML---C#-.md)