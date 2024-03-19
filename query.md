1) tutte le risorse con isActive = true
db.collection('W2-P1-Users').find({isActive: true });


2) trova tutte le risorse con dato age maggiore di 26
db.collection('w2-p1-Users').find({age: {$gt: 26}})

3) trova tutte le risorse con dato age maggiore di 26 e minore o uguale a 30
db.collection('w2-p1-Users').find({$and: [{age: {$gt: 26}} ,{age: {$lte: 30}}]})

4) trova tutte le risorse con il dato eyes che sia brown o blue
db.collection('w2-p1-Users').find({$or: [{eyeColor: "brown"},{eyeColor: "blue"}]})

5) trova tutte le risorse che non presentano il dato eyes uguale a greeen
db.collection('w2-p1-Users').find({eyeColor: {$not: {$eq:"green"}}})

6) trova tutte le risorse che non presentano il dato eyes uguale a green e neanche a blue
db.collection('w2-p1-Users').find({$nor: [{eyeColor: "green"},{eyeColor:"blue"}]})

7) trova tutte le risorse con il dato company = "FITCORE" e ritorna solo la mail
db.collection('w2-p1-Users').findone({"company": "FITCORE"}, {"email": 1, "_id": 0})


