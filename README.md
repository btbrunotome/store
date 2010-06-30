store.js
========

store.js exposes a simple API for cross browser local store

	// Store 'marcus' at 'username'
	store.set('username', 'marcus')
	
	// Get 'username'
	store.get('username')
	
	// Remove 'username'
	store.remove('username')
	
	// Clear all keys
	store.clear()
	
	// Use JSON to stash an object (see http://www.json.org/json2.js)
	store.set('user', JSON.stringify({ name: 'marcus', likes: 'javascript' }))
	
	// Use JSON to retrieve an object (see http://www.json.org/json2.js)
	var user = JSON.parse(store.get('user'))
	alert(user.name + ' likes ' + user.likes)

Tests
-----
Go to test.html in your browser

Supported
---------
 - Tested in Firefox 2.0
 - Tested in Firefox 3.0
 - Tested in Firefox 3.6
 - Tested in Chrome 5
 - Tested in Safari 4
 - Tested in Safari 5
 - Tested in IE6
 - Tested in IE7
 - Tested in IE8
 - Tested in Opera 10

Not supported
-------------
 - Firefox 1.0: no means (beside cookies and flash)
 - Safari 2: no means (beside cookies and flash)
 - Safari 3: no synchronous api (has asynch sqlite api, but store.js is synch)

TODO
----
 - I believe underlying APIs can throw under certain conditions. Where do we need try/catch?
 - Check if there's an API for storage in Opera 9
 - Test in Firefox 3.5
 - Test in Chrome 4
 - Test in Opera 9
 - Test different versions of Opera 10.X explicitly
