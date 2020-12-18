# Dev Interview

Let's build a multi-tenant todo app!

You are the lead developer and architect, you choose the stack, the architecture and assign tasks to team members.

Requirements:
- Users must be able to register and login with username and password
- Users must be able to create multiple todo lists
- Users must create, delete and complete a todo item on any list
- (Optional) Allow users to share lists with other users
- must be able to run 100% locally

Tech Requirements:
- Use Node.js for backend, framework your choice
- React frontend, frameworks your choice
- Services (DBs, etc.) via docker

Requirements Questions while wait'n

Register and login - out of box solution prefered OR we could just store the user in a totally unsecure and bad practices kinda table.
Is there something established we could use? Preference on anything? oauth or cognito or... Session or jwt?
Do we want users to login with google/facebook or create new?

Are users sharing same todos or clean slate for each user?
List for each user that each user can interact with or one long list of everyone's todos?
Can users delete and complete everyone's todos or is it restricted to their own?
Are todos just in the order they come in?


Structure
docker compose
   client - client in react create react app (talks to our locally running server)
   server - (express) locally running instance 
    route wise
       api - 
       todo(CRUD)
          get
          alter

       user
          register
          login
            
       req - user's todo - 
       
   db - sql - (postgress)
  
     user (email, loginName, firstname, lastname,password, todo ref to the todo table)
     logins (login activity, user where they logged in at , event that triggered, ref url, meta of login as activity)
     optional - (device table)
     devices - (mma)
     todo list
        todoItem( text, state, created, due, ownedByUser)
     todos()
       
   
   
   

Backend
auth service. create a handler for authenticateMe router. (req, resp, next)

