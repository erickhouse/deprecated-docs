### AWS Dynamo 

[DynamoDB Core Components](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html#HowItWorks.CoreComponents.SecondaryIndexes)

`{tableName}/{primaryKey}` but it is normal for the primary key to be a composit key

`{tableName}/{primaryKey/subkey}`

Tables – Similar to other database systems, DynamoDB stores data in tables. A table is a collection of data. For example, see the example table called People that you could use to store personal contact information about friends, family, or anyone else of interest. You could also have a Cars table to store information about vehicles that people drive.

Items – Each table contains zero or more items. An item is a group of attributes that is uniquely identifiable among all of the other items. In a People table, each item represents a person. For a Cars table, each item represents one vehicle. Items in DynamoDB are similar in many ways to rows, records, or tuples in other database systems. In DynamoDB, there is no limit to the number of items you can store in a table.

Attributes – Each item is composed of one or more attributes. An attribute is a fundamental data element, something that does not need to be broken down any further. For example, an item in a People table contains attributes called PersonID, LastName, FirstName, and so on. For a Department table, an item might have attributes such as DepartmentID, Name,Manager, and so on. Attributes in DynamoDB are similar in many ways to fields or columns in other database systems.

- Sort key and Range key are the same thing.
- You can only have one sort key per primary key
- Primary keys determine where things are saved logically. Sort keys search over the partition but not other paritions 
- It is really important to design your keys on how you want to search
- Local secondary indexes provide a way to add more sort keys on a primary key but they do not dictate logical organization of data in the database (they do not determine which partition on the data is saved on)
