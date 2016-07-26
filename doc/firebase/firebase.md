## Firebase

The firebase library can be used to add real-time database functionality in your Python applications. This library depends on creating a Firebase app at [Google Firebase](https://console.firebase.google.com/). The Firebase database allows you to store, retrieve, and update data.

### Firebase Functions
* `firebase.loadFirebase(api_key, auth_domain, database_url)` : Creates a firebase database connection to your existing Firebase app. It returns the _Firebase_ object that you will use for all the database functionality (the class is explained below). Pass the API key and the app name twice as strings.
`db = firebase.loadFirebase('jyF2PpefHM', 'my_firebase_app', 'my_firebase_app')`
You will continue to use this db object to work with the database.

### Firebase Class

Save Data:

* `db.set(url, data)`: Write or replace data to a URL path, such as `users/star_count`. For example, `db.set('users/star_count', 10)`.
* `db.push(url, data)`: Writes data to URL path, which creates a new unique sub-directory for the data. For example, `db.push('users/', {'username': 'Bob'})`.
* `db.remove(url)`: Removes data at the given URL path. For example, `db.remove('users/')`.
* `db.update(url, data)`: Writes or replaces the data to the URL path. For example, `db.set('users/star_count', 15)`.

Retrieve Data:

* `db.child_added(url, fn)`: When data is initially fetched and added at the passed URL path the passed callback will execute. For example, `db.child_added('users/', printUsers)`.
* `db.child_removed(url, fn)`: When data is removed at the passed URL path the passed callback will execute. For example, `db.child_removed('users/', printRemovedUsers)`.
* `db.child_updated(url, fn)`: When data is updated at the passed URL path the passed callback will execute. For example, `db.child_updated('users/', printUpdatedUsers)`.

### Setup

Head to [Firebase setup](./setup.md).


### Examples

Saving/Updating/Removing Data Example:

```python
import firebase

db = firebase.loadFirebase('jyF2PpefHM', 'fir-docs-demo', 'fir-docs-demo')

"""

"""
db.set('users/star_count', 10) # data can be numbers
db.set('users/to_be_deleted', '10') # data can be strings
db.set('users/pi', 3.15)
"""

"""
db.push('users/', {'username': 'Mary'}) # data can be python dictionaries
db.push('users/', {'username': 'Joe'})
db.push('users/', {
                    'username': 'Bob',
                    'email': 'example@email.com',
                    'age': 22
                    })

db.remove('users/to_be_deleted') # remove the data at the URL 'users/to_be_deleted'

db.update('users/pi', 3.14) # the data at the URL 'users/star_count' is now the number 3.14

```

Retrieving Data Example:

```



```

Chat Example:

```

```

### Credits

* [Google Firebase](https://firebase.google.com/docs/web/setup)
