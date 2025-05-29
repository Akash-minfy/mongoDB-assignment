use toDoList
switched to db toDoList
toDoList.insert({name:"mongoAssign",done:0})
ReferenceError: toDoList is not defined
db.toDoList.insert({name:"mongoAssign",done:0})
DeprecationWarning: Collection.insert() is deprecated. Use insertOne, insertMany, or bulkWrite.
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e34d671aa3c83439408f')
  }
}
db.toDoList.insertOne({name:"mongoAssign",done:0})
{
  acknowledged: true,
  insertedId: ObjectId('6836e357671aa3c834394090')
}
show dbs
sample_mflix  156.23 MiB
toDoList        8.00 KiB
admin         344.00 KiB
local         122.10 GiB
db
toDoList
db.toDoList.insertMany([{name:"watchSeries",done:0},{name:"readTerraform",done:0}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e3fa671aa3c834394091'),
    '1': ObjectId('6836e3fa671aa3c834394092')
  }
}
show collections
toDoList
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0
}
db.toDoList.insertMany([{name:"play",done:0},{name:"relax",done:0}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e4fd671aa3c834394093'),
    '1': ObjectId('6836e4fd671aa3c834394094')
  }
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0
}
db.toDoList.updateMany({done:0},{$set:{done:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 6,
  modifiedCount: 6,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: false
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: false
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: false
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: false
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: false
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: false
}
db.toDoList.updateMany({done:false},{$set:{done:1}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 6,
  modifiedCount: 6,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 1
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 1
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 1
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 1
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 1
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 1
}
db.toDoList.updateMany({done:false},{$set:{done:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.toDoList.updateMany({done:false},{$set:{done:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 1
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 1
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 1
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 1
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 1
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 1
}
db.toDoList.updateMany({done:1},{$set:{done:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 6,
  modifiedCount: 6,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0
}
db.toDoList.insertMany([{name:"eat",done:0},{name:"sleep",done:0},{name:"workout",done:0}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e6f9671aa3c834394095'),
    '1': ObjectId('6836e6f9671aa3c834394096'),
    '2': ObjectId('6836e6f9671aa3c834394097')
  }
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0
}
db.toDoList.updateMany({dueDate:new Date()})
MongoInvalidArgumentError: Update document requires atomic operators
db.toDoList.updateMany({"dueDate":new Date()})
MongoInvalidArgumentError: Update document requires atomic operators
db.toDoList.updateMany({},{$set:{dueDate:new Date("28-05-2025")}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0,
  dueDate: 1970-01-01T00:00:00.000Z
}
db.toDoList.updateMany({},{$set:{dueDate:Date("28-05-2025")}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0,
  dueDate: 'Wed May 28 2025 16:12:21 GMT+0530 (India Standard Time)'
}
db.toDoList.updateMany({},{$set:{dueDate:"28-05-2025"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0,
  dueDate: '28-05-2025'
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0,
  dueDate: '28-05-2025'
}
db.toDoList.updateMany({done:0},{$set:{status:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
db.toDoList.updateMany({done:0},{$set:{}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 0,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  done: 0,
  dueDate: '28-05-2025',
  status: 0
}
db.toDoList.updateMany({done:0},{$unset:{done:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 0
}
db.toDoList.updateMany({name:'sleep'},{$set:{status:1})
SyntaxError: Unexpected token, expected "," (1:54)

[0m[31m[1m>[22m[39m[90m 1 |[39m db[33m.[39mtoDoList[33m.[39mupdateMany({name[33m:[39m[32m'sleep'[39m}[33m,[39m{$set[33m:[39m{status[33m:[39m[35m1[39m})
 [90m   |[39m                                                       [31m[1m^[22m[39m[0m
db.toDoList.updateMany({name:'sleep'},{$set:{status:1}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 1
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 0
}
db.toDoList.updateMany({},{$set:{status:0})
SyntaxError: Unexpected token, expected "," (1:42)

[0m[31m[1m>[22m[39m[90m 1 |[39m db[33m.[39mtoDoList[33m.[39mupdateMany({}[33m,[39m{$set[33m:[39m{status[33m:[39m[35m0[39m})
 [90m   |[39m                                           [31m[1m^[22m[39m[0m
db.toDoList.updateMany({},{$set:{status:0}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 1,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 0
}
db.toDoList.update({_id:ObjectId('6836e6f9671aa3c834394097')},{$set:{status:1}})
DeprecationWarning: Collection.update() is deprecated. Use updateOne, updateMany, or bulkWrite.
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1
}
db.toDoList.updateMany({},{$set:{createdAt:new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z
}
db.toDoList.updateMany({},{$set:{updatedAt: new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:09:47.017Z
}
db.toDoList.updateMany({},{$currentDate:{updatedAt: new Date()}})
MongoServerError: date is not valid type for $currentDate. Please use a boolean ('true') or a $type expression ({$type: 'timestamp/date'}).
db.toDoList.updateMany({},{$currentDate:{updatedAt: true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.922Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.922Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.922Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:20.923Z
}
db.toDoList.updateMany({},{$currentDate:{updatedAt: true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:12:35.549Z
}
db.toDoList.updateMany({},{$currentDate:{updatedAt: new Date()}})
MongoServerError: date is not valid type for $currentDate. Please use a boolean ('true') or a $type expression ({$type: 'timestamp/date'}).
db.toDoList.updateMany({},{$set:{updatedAt: new Date()}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 9,
  modifiedCount: 9,
  upsertedCount: 0
}
db.toDoList.find()
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
db.toDoList.count()
DeprecationWarning: Collection.count() is deprecated. Use countDocuments or estimatedDocumentCount.
9
db.toDoList.sort({name:1})
TypeError: db.toDoList.sort is not a function
db.toDoList.find().sort({name:1})
{
  _id: ObjectId('6836e6f9671aa3c834394095'),
  name: 'eat',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e34d671aa3c83439408f'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e357671aa3c834394090'),
  name: 'mongoAssign',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394093'),
  name: 'play',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394092'),
  name: 'readTerraform',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e4fd671aa3c834394094'),
  name: 'relax',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394096'),
  name: 'sleep',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e3fa671aa3c834394091'),
  name: 'watchSeries',
  dueDate: '28-05-2025',
  status: 0,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
{
  _id: ObjectId('6836e6f9671aa3c834394097'),
  name: 'workout',
  dueDate: '28-05-2025',
  status: 1,
  createdAt: 2025-05-28T10:52:38.950Z,
  updatedAt: 2025-05-28T11:14:06.830Z
}
Atlas atlas-w72zb5-shard-0 [primary] toDoList

