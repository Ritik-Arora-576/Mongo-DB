<h1 align="center">Mongo DB</h1>
<div align="center">
  <img src="https://res.cloudinary.com/hevo/image/upload/f_auto,q_auto/v1644403814/hevo-learn/springboot_MongoDB_configuration_mongodb.jpg?_i=AA" align="center" height=50% width=50%>
</div>
<br>
<ul>
  <li><strong>Mongo: </strong>It is a command line shell that connect to a specific instance of Mongo D.</li>
  <li><strong>MongoD: </strong>It is also known as <em>Mongo Daemon</em> it's basically host the process for the database.</li>
</ul>
<br>
<div align="center">
  <img src="https://user-images.githubusercontent.com/68052449/223647052-8ced9cd1-57ed-4440-a24b-c079cf9d015f.png" align="center" row=50% width=50%>
</div>
<h3>Mongo DB Terminologies</h3>
<ul>
  <li><strong>Database:</strong> It is a set of collections.</li>
  <li><strong>Collections:</strong> It is a set of data. (For SQL it is a kind of table)</li>
  <li><strong>Document (BSON):</strong> It is acted like a row or data stored inside a collections.</li>
  <li><strong>Fields:</strong> It is a set of attributes or columns.</li>
</ul>
<br>
<h3>Commands:</h3>
<ul>
  <li><strong><em>mongosh</em></strong> is used to start the Mongo shell.</li>
  <li>Database</li>
  <ul>
    <li><strong><em>show dbs;</em></strong> is used to view all databases.</li>
    <li><strong><em>use database_name</em></strong> is used to create or switch to new database.</li>
    <li><strong><em>db</em></strong> is use to view currently used database.</li>
    <li><strong><em>db.dropDatabase();</em></strong> is use to delete currently active database.</li>
  </ul>
  <li>Collections</li>
  <ul>
    <li><strong><em>show collections</em></strong> is use to view all collections in currently active database.</li>
    <li><strong><em> db.createCollection("collection_name");</em></strong> is use to create new collection.</li>
    <li><strong><em> db.collection_name.drop()</em></strong> is use to delete collection.</li>
  </ul>
  <li>Enteries Insertions in Database</li>
  <ul>
    <li><strong><em>db.collection_name.insertOne({'name':'Ritik','Branch':'EE'})</em></strong> is use to insert one entry in collection.</li>
    <li><strong><em>db.collection_name.insertMany([{'name':'Ritik','Branch':'EE'},{'name':'Naman','Branch':'CSE'}])</em></strong> is use to insert more than one entries in collection.</li>
    <li>A unique object ID is attach to every object enteries.</li>
    <li><strong><em>db.collection_name.find();</em></strong> is use to view all rows inside the collection.</li>
    <li>We can add different feilds to multiple row enteries.</li>
    <li><strong><em>db.collection_name.find({'name':'Ritik','Branch':'EE'})</em></strong> is use to find the entry whose name is Ritik and Branch is EE.</li>
    <li><strong><em>db.collection_name.findOne({'name':'Ritik','Branch':'EE'})</em></strong> is use to find the first occurance whose name is Ritik and Branch is EE.</li>
    <li><strong><em>db.collection_name.find().limit(5);</em></strong> is use to limit the output upto 5. If there is less than 5 row enteries in collection then it will show all the outputs.</li>
    <li><strong><em>db.collection_name.find().count();</em></strong> is use to show the total number of outputs.</li>
    <li><strong><em>db.collection_name.find().sort({'value':1});</em></strong> is use to sort row enteries in ascending order.(Assume value as feild of enteries)</li>
    <li><strong><em>db.collection_name.find().sort({'value':-1});</em></strong> is use to sort row enteries in descending order.</li>
  </ul>
  <li>Updation</li>
  <ul>
    <li><strong><em>db.collection_name.updateMany({'name':'Ritik'},{$set:{'name':'Ritik', 'Branch':'MCE'}});</em></strong> is use to update entries whose name is Ritik.</li>
    <li><strong>upsert</strong> is false by default. If upsert gets true then if any entries has not been matched then new entry has been inserted.<strong><em>db.collection_name.updateMany({'name':'Ritik'},{$set:{'name':'Ritik', 'Branch':'MCE'}},{upsert:true});</em></strong></li>
    <li><strong><em>db.collection_name.updateMany({'name':'Ritik'},{$inc:{'value':2}});</em></strong> is use to increase value feild by 2.</li>
  </ul>
</ul>
