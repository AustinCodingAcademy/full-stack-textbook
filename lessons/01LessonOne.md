![](http://static1.squarespace.com/static/538f3fcde4b05c5fecc7a40e/t/538f48a4e4b00d94e8c253b3/1453396632576/?format=400w)
# Full Stack Textbook
## Lesson Zero

### The Local Environment
Your local "environment" is your configuration of your physical machine you are programming on. Different technologies have certain dependencies, configuration files, binaries, and shortcuts that need to be in their correct places, seemingly strewn across your computer. Setting up your environment is often the largest "barrier of entry" to openly coding on a project, and is the first point of frustration. If you went through the [Install Guide](../InstallGuide.md), you have already set up your environment for this course. Let's briefly talk about what each technology is and what it is used for.

#### [Git](https://git-scm.com/)
Git is a "version control system" for your code. That that means is that if you code and code and code, and get your project doing something really well, you can "checkpoint", or version, it. When you want to add a feature, you risk breaking your past features. Then if you change your mind about the new feature, you can now just jump back to your past working "checkpoint". There are many more features of this tool that we will get into during class. [Github](https://github.com) is simply your Git checkpoints in the "cloud", or on the internet. This helps with making more secure copies of your work, as well as allow collaboration on projects.

#### [MAMP](https://www.mamp.info/)
MAMP stands for Mac, Apache, MySQL, and PHP. This is a popular "stack" for building PHP web applications. Most computers and operating systems come preinstalled with some of these technologies, but your OS depends on them to work a certain way. That's why you should be very careful when "developing/playing" with the default technologies, as even only upgrading could have negative side effects. The closer a developer gets to working on their default technologies, the closer he gets to developing on "bare metal". MAMP gives us an insulated layer to play with. No matter how bad we ruin things by tinkering with them, we can always reinstall a clean version of MAMP. Some developers go so far as to install a Virtual Machine (VM) on their computers. These are essentially a computer-within-a-computer, and are made to not only protect your computer's technologies, but to simulate other computer configurations.

#### [Composer](https://getcomposer.org/)
Composer is a package manager for PHP. You can simply search for a package on https://packagist.org/, then install it from the command line using `composer`.

#### [Node.js](https://nodejs.org/)
Node.js is sort of a JavaScript version of MAMP. Is does so much more than what we will be using it for in class. In class, we will mainly be using it for its packaging capabilities using a technology called Node Package Manager (`npm`). We can simply search for a package on https://www.npmjs.com/, and in your terminal run `npm install <package name>` and it magically appears.

#### [SQLite](https://www.sqlite.org/)
At the heart of all web apps is the precious database. There are many different types of databases, one of the most popular being Relational Databases. We can "talk" to these databases using SQL. The most popular free databases are MySQL, Postgres, and SQLite. These three are, more-or-less, interchangeable behavior-wise, but each excel in their own use cases. We went with SQLite becuase of its simplicity in setting up. It is not supposed to used as a production level webapp database, but more for local testing and development.
