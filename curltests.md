### Create User 1 and 2(Create new dummy ids.)


     curl -X POST https://neofi-epcs.onrender.com/signup \
          -H "Content-Type: application/json" \
          -d '{"username": "user001", "email": "user001@example.com", "password": "SecurePassword123"}'

     curl -X POST https://neofi-epcs.onrender.com/signup \
          -H "Content-Type: application/json" \
          -d '{"username": "user002", "email": "user002@example.com", "password": "SecurePassword123"}'

### Login one user

     curl -X POST https://neofi-epcs.onrender.com/login \
          -H "Content-Type: application/json" \
          -d '{"username": "user01", "password": "SecurePassword123"}'


### Create Note

     curl -X POST https://neofi-epcs.onrender.com/notes/create \
          -H "Authorization: Token   your_token_here" \
          -H "Content-Type: application/json" \
          -d '{"title": "My First Note", "content": "This is the content of my first note."}'


### Retrieve Note
     curl -X GET https://neofi-epcs.onrender.com/notes/note_id_here \
          -H "Authorization: Token  your_token_here"

### Update Note

     curl -X PUT https://neofi-epcs.onrender.com/notes/note_id_here/update \
          -H "Authorization: Token   your_token_here" \
          -H "Content-Type: application/json" \
          -d '{"title": "Updated Title", "content": "Updated content of the note."}'

### Delete Note

     curl -X DELETE https://neofi-epcs.onrender.com/notes/note_id_here/delete \
          -H "Authorization: Token  your_token_here"


### Share Note

     curl -X POST https://neofi-epcs.onrender.com/notes/share \
          -H "Authorization: Token  your_token_here" \
          -H "Content-Type: application/json" \
          -d '{"note_id": "note_id_here", "usernames": ["username1", "username2"]}'

### Version History
     curl -X GET https://neofi-epcs.onrender.com/notes/version-history/note_id_here \
          -H "Authorization: Token  your_token_here"
