# Database2

**1. Create a Database called customers.**
```
test> use customers
switched to db customers

```

**2. Create a collection called customerdetails.**
```
switched to db customers
customers> db.createCollection("customerdetails")
{ ok: 1 }

```

**3. Insert all documents into the collection named   customerdetails.**
```customers> db.customerdetails.insertMany([
{ name: "John", age: "25", gender: "Male", city: "New York" }, 
 { name: "Emily", age: "22", gender: "Female", city: "London" }, 
 { name: "Daniel", age: "28", gender: "Male", city: "Sydney" }, 
 { name: "Sophia", age: "24", gender: "Female", city: "Paris" }, 
{ name: "William", age: "26", gender: "Male", city: "Chicago" }, 
{ name: "Olivia", age: "23", gender: "Female", city: "Los Angeles" }, 
 { name: "Benjamin",age: "27", gender: "Male", city: "Toronto" }, 
 { name: "Mila", age: "29", gender: "Female", city: "Berlin" }, 
 { name: "James", age: "30", gender: "Male", city: "Tokyo" }
 ])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654cb02d8ff6b33fa23020e3"),
    '1': ObjectId("654cb02d8ff6b33fa23020e4"),
    '2': ObjectId("654cb02d8ff6b33fa23020e5"),
    '3': ObjectId("654cb02d8ff6b33fa23020e6"),
    '4': ObjectId("654cb02d8ff6b33fa23020e7"),
    '5': ObjectId("654cb02d8ff6b33fa23020e8"),
    '6': ObjectId("654cb02d8ff6b33fa23020e9"),
    '7': ObjectId("654cb02d8ff6b33fa23020ea"),
    '8': ObjectId("654cb02d8ff6b33fa23020eb")
  }
}
customers> 
```

**4. Retrieve all documents from the collection and sort the results by the “age” field    in ascending order.**
```
customers> db.customerdetails.find().sort({ age: 1 })
[
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e4"),
    name: 'Emily',
    age: '22',
    gender: 'Female',
    city: 'London'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e8"),
    name: 'Olivia',
    age: '23',
    gender: 'Female',
    city: 'Los Angeles'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e6"),
    name: 'Sophia',
    age: '24',
    gender: 'Female',
    city: 'Paris'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e3"),
    name: 'John',
    age: '25',
    gender: 'Male',
    city: 'New York'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e7"),
    name: 'William',
    age: '26',
    gender: 'Male',
    city: 'Chicago'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e9"),
    name: 'Benjamin',
    age: '27',
    gender: 'Male',
    city: 'Toronto'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020e5"),
    name: 'Daniel',
    age: '28',
    gender: 'Male',
    city: 'Sydney'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020ea"),
    name: 'Mila',
    age: '29',
    gender: 'Female',
    city: 'Berlin'
  },
  {
    _id: ObjectId("654cb02d8ff6b33fa23020eb"),
    name: 'James',
    age: '30',
    gender: 'Male',
    city: 'Tokyo'
  }
]

```

**5. Count the number of females.**
```customers> db.customerdetails.countDocuments({ gender: "Female" })
4
customers>
```

**6.Insert one document into the customerdetails collection.**
```customers> db.customerdetails.insertOne({
...     name: "Sam",
...     age: 30,
...     gender: "male",
...     city: "New York"
... })
{
  acknowledged: true,
  insertedId: ObjectId("654cb2dc8ff6b33fa23020ec")
}
customers> 

```

**7. Update city=SriLanka to John.**
```
customers> db.customerdetails.updateOne({ name: "John" },{$set: {city: "Sri Lanka" }})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
customers> 


```

**8. Remove the customer from Tokyo.**
```customers> db.customerdetails.deleteOne({ city: "Tokyo" });
{ acknowledged: true, deletedCount: 1 }
customers> 

```

**9.  Find customers not from Los Angeles.**
```
```

**10.Find the customers who are older than age 25.**
```
```

**11.Retrieve the males who are less than 25.**
```
```

**12.Update Francis age to 35, if Francis is not available upsert.**
```
```

**13.Retrieve males who are younger than 30 and older than25.**
```
```

**14.Find a customer who is lesser than or equal to 23.**
```
```

**15.Remove the customer from Tokyo.**
```
```


















