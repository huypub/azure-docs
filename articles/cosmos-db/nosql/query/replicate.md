---
title: REPLICATE in Azure Cosmos DB query language
description: Learn about SQL system function REPLICATE in Azure Cosmos DB.
author: ginamr
ms.service: cosmos-db
ms.subservice: nosql
ms.topic: conceptual
ms.date: 03/03/2020
ms.author: girobins
ms.custom: query-reference, ignite-2022
---
# REPLICATE (Azure Cosmos DB)
[!INCLUDE[NoSQL](../../includes/appliesto-nosql.md)]

 Repeats a string value a specified number of times.
  
## Syntax
  
```sql
REPLICATE(<str_expr>, <num_expr>)
```  
  
## Arguments
  
*str_expr*  
   Is a string expression.
  
*num_expr*  
   Is a numeric expression. If *num_expr* is negative or non-finite, the result is undefined.
  
## Return types
  
  Returns a string expression.
  
## Remarks

  The maximum length of the result is 10,000 characters i.e. (length(*str_expr*)  *  *num_expr*) <= 10,000. This system function will not utilize the index.

## Examples
  
  The following example shows how to use `REPLICATE` in a query.
  
```sql
SELECT REPLICATE("a", 3) AS replicate
```  
  
 Here is the result set.
  
```json
[{"replicate": "aaa"}]
```  

## Next steps

- [System functions Azure Cosmos DB](system-functions.yml)
- [Introduction to Azure Cosmos DB](../../introduction.md)
