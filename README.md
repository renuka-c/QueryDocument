# QueryDocument
given total explanation on find query, finding  query using condition, specify  and condition

 Shop> show collections
Things
Shop> db.collections.find()

Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 25,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: 45,
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop> db.Things.update({item : 'postcard'},{$set: {qty : '50'}});
DeprecationWarning: Collection.update() is deprecated. Use updateOne, updateMany, or bulkWrite.
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 25,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop> db.Things.update({tags : ['blank','red']},{$set: {qty : '100'}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: '100',
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop> db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 100,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop> db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:[22,30]});
Uncaught:
SyntaxError: Unexpected token, expected "," (1:88)

> 1 | db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:[22,30]});
    |                                                                                         ^
  2 |

Shop>  db.Things.updateMany({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:[22,30]});
Uncaught:
SyntaxError: Unexpected token, expected "," (1:90)

> 1 |  db.Things.updateMany({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:[22,30]});
    |                                                                                           ^
  2 |

Shop>  db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:[22,30]}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 0,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 100,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop>  db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:['22','30']});
Uncaught:
SyntaxError: Unexpected token, expected "," (1:93)

> 1 |  db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:['22','30']});
    |                                                                                              ^
  2 |

Shop> db.Things.updateOne({tags : ['blank','red']},{$set: {qty : 100}},{$set: {dim_cm:['22','30']}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 0,
  upsertedCount: 0
}
Shop> dbs.Things.find()
ReferenceError: dbs is not defined
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 100,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop> Shop>  db.Things.updateOne({tags : ['blank','red']},{$set: {dim_cm : [20, 30]}});
ReferenceError: Shop is not defined
Shop>  db.Things.updateOne({tags : ['blank','red']},{$set: {dim_cm : [20, 30]}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 100,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 20, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 75,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]
Shop>  db.Things.updateMany({tags : ['blank','red']},{$set: {qty : 10}},{$set: {dim_cm:[7, 4]}});
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
Shop> db.Things.find()
[
  {
    _id: ObjectId('6594f6915f508329515f758e'),
    item: 'journal',
    qty: 10,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 20, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f758f'),
    item: 'notebook',
    qty: 50,
    tags: [ 'red', 'blank' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7590'),
    item: 'paper',
    qty: 100,
    tags: [ 'red', 'blank', 'plain' ],
    dim_cm: [ 14, 21 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7591'),
    item: 'planner',
    qty: 10,
    tags: [ 'blank', 'red' ],
    dim_cm: [ 22.85, 30 ]
  },
  {
    _id: ObjectId('6594f6915f508329515f7592'),
    item: 'postcard',
    qty: '50',
    tags: [ 'blue' ],
    dim_cm: [ 10, 15.25 ]
  }
]


  
    

 
