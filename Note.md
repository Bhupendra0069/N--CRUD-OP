# Basics syntax 
1. npm init -y => for packge.json
2. npm i express => for install express
3. npm i nodemon => for install nodemon
4. app.set("view engine","ejs") => to use ejf
5. app.use(express.json()); => to get input in json format
6. app.use(express.static(Path.join(__dirname,"public"))); => to use static file like images,css js
7. app.use(express.urlencoded({extended:true})); => to gt input form data
8. const path=require('path'); => import for to know path of folder
9. npm i ejs => for install package ejs


# Database
-Mongo DB

terminlogies:
-collections
-documents
-schemas
-keys
-models

1.npm i mongoose => connect node server and mongo Db server



# crude operation

 # Create
   app.get('/create',async (req,res)=>{
    let createduser=await userModel.create({
        name:"harsh",
        username:"harsh",
        email:"sjdh@gmail.com"
    })
    res.send(createduser)
});
 # Update
  app.get('/update',async (req,res)=>{
   let updateuser=await userModel.findOneAndUpdate({username:"harsh"}, {name:"harshsjdbhsdjsdhhjdjs"},);
    res.send(updateuser);
});
# read 
 app.get('/read',async (req,res)=>{
   let users=await userModel.findOne({username:"harsh"});
   res.send(users);
});
 # delete
app.get('/delete',async (req,res)=>{
   let users=await userModel.findOneAndDelete({username:"harsh"});
   res.send(users);
});




