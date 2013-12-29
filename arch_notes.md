


# Auth

## login

- Set last login session in user doc
- add document to session collection

{
 "_id"
 "user_id"
 "last_activity"
 "last_ip"
 "login token"
}

The session collection is a TTl collection to keep the size small. We use the session DB to
insure the collection and index stay in memory.

## logout
We destry the session document in the session collection



## Client duties

- The auth token will be regenerated every n minutes.
- it is the clients duty to update and start using the new token

## Session ip changes
- We log every change of ip in session

