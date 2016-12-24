# Hürriyet API JS SDK

## Initializing the API

1. Install the package;

	**Using yarn:**
	
	    yarn add hurriyet-js-sdk

	**Using npm:**
	
	    npm install --save hurriyet-js-sdk

2. Import it;

	    import hurriyetsdk from 'hurriyet-js-sdk';

	If import is not available;

		let hurriyetsdk = require('hurriyet-js-sdk');

3. Retrieve an account at https://developers.hurriyet.com.tr/
4. Get your API key at your Dashboard. (Under the menu when you click on top-right corner of the site.)
5. Initialize a HurriyetAPI object using said API key.

	**React Native;**
	
		let HurriyetAPI = new hurriyetsdk({ token: 'YOUR TOKEN' });

	**Node**
		
	Install node-fetch;
		
		npm install --save node-fetch
		
	Afterwards;
	
		let HurriyetAPI = new hurriyetsdk({
			token: 'YOUR TOKEN',
			fetch: require('node-fetch'),
		});
6. Example call is as follows (wrapping your properties as an object is a must.);

		HurriyetAPI.getArticles({
			articleId: '12345'
		}).then((response) => {
			console.log(response);
		});
	Please refer to the Hurriyet's docs for what the properties mean. You need to supply them as a key-value pair.
7. You can now use HurriyetAPI for your needs. Happy coding!

## Article
	 1. articleId: If not supplied, will retrieve a list of articles.
	 2. filter
	 3. select
	 4. top
	 5. skip
## Column
	 1. columnId: If not supplied, will retrieve a list of columns.
	 2. filter
	 3. select
	 4. top
	 5. skip
## Date
	None.
## News Photo Gallery
	 1. galleryId: If not supplied, will retrieve a list of news photo galleries.
	 2. filter
	 3. select
	 4. top
	 5. skip
## Page
	 1. pageId: If not supplied, will retrieve a list of pages.
	 2. filter
	 3. select
	 4. top
	 5. skip
## Path
	1. pathId: If not supplied, will retrieve a list of paths.
	2. filter
	3. select
	4. top
	5. skip
## Search
	1. skip
	2. top
	3. sort: s in Hurriyet's docs.
	4. keyword: Must be supplied.
## Writer
	1. writerId: If not supplied, will retrieve a list of writers.
	2. filter
	3. select
	4. top
	5. skip

Developed by amazing people **@** House of Apps.