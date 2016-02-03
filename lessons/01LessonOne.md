![](http://static1.squarespace.com/static/538f3fcde4b05c5fecc7a40e/t/538f48a4e4b00d94e8c253b3/1453396632576/?format=400w)
# Full Stack Textbook
## Lesson One

### "Spec"ing out the MVP
All great apps start out as an idea. That idea is broken down into smaller, more detailed, ideas, called "specs", or specifications. The ideas are expanded, prioritized, and cut until you have the map to your MVP (Minimum Viable Product). This is the level your app needs to reach before you, an investor, or a small level of test users decide if your app has potential or if it's worth spending any more of your precious time on.

### Database Design
At the heart of every app, the only real value lies in the database. The design of this database is vital to the speed at which you can develop.

#### Tables

##### Primary Keys
##### Foreign Keys
##### Relationships
* One to One ([hasOne](https://laravel.com/docs/5.2/eloquent-relationships#one-to-one))
* One to Many ([hasMany](https://laravel.com/docs/5.2/eloquent-relationships#one-to-many))
* Inverse Relationship (belongsTo)
* Many-to-Many ([belongsToMany](https://laravel.com/docs/5.2/eloquent-relationships#many-to-many))
* Has Many Through ([hasManyThrough](https://laravel.com/docs/5.2/eloquent-relationships#has-many-through))

## Homework
On http://ondras.zarovi.cz/sql/demo/ is a great tool for visualizing databases. [Here's a video](https://www.youtube.com/watch?v=hCQzJx9AKhU) tutorial on how to use it. 

[Here](https://gist.githubusercontent.com/mistakevin/7152054fcdf022e73e71/raw/3e58a4121da0e15c61bc879dabcf633fae3869f8/breddit.xml) is the database design we built in class. Click "Save/Load" in the table builder screen, then copy and paste that into the "Input/Out", then click "Load XML" to view.

Build amd save two database designs for the following app descriptions. To "Save" a design, you simply click the "Save/Load" button in the table builder screen, then "Save XML". The code that is generated in the "Input/Output" box should be saved in a text file, like _bocket.xml_, on your desktop, or in a [gist](https://gist.github.com/)! 

### Bocket
Bocket is a "Better" bookmarking service, much like [Pocket](getpocket.com). Users each has a username, email, password. They each have many Bookmarks, which are made up by a link and a user_id. Each Bookmark can have many Tags, which are simply made up of user_id and a name.

### Bitter
Bitter is a "Better" posting app which shares features from Twitter and Facebook. A User can have many Posts. Each Post can have many likes, which are made by other Users!
