# Front-End Candidate Test

:wave: Welcome to The Telegraph front-end candidate test

- [Task](#wrench-task)
	- [Requirements](#mega-requirements)
	- [What we are looking for](#mag_right-what-we-are-looking-for)
	- [Data](#open_file_folder-data)
	- [Designs](#art-designs)
- [Set up](#floppy_disk-set-up)
- [Acceptance criteria](#scroll-acceptance-criteria)
- [Submitting your code](#mailbox_with_mail-submitting-your-code)

## :wrench: Task 

We would like you to build a responsive news article as per the included designs. You should meet the [ACs](#scroll-acceptance-criteria).

We've built a bare-bones [express](https://expressjs.com/) application with some basic front-end tooling ([webpack](https://webpack.js.org/) for JavaScript compilation and [PostCSS](https://postcss.org/) for CSS concatenation).

Your code should work in modern browsers such as Chrome, Firefox and Edge. Do not worry about supporting IE11 or below.

You should spend no more than four hours on this task. If you do not complete the task in time please submit with a list of what you would have done with more time. Feel free to be specific and write `// TODO`s throughout your code.

### :mega: Requirements

* Match the [designs](#art-designs) as closely as possible
* Application should be fully responsive
* Pass the [ACs](#scroll-acceptance-criteria)
* Ensure code is unit tested. We've set this up with [Jest](https://jestjs.io/) but feel free to use whatever you like
* Keep your JavaScript vanilla please
* Comments should be called in once the DOM is ready via [this endpoint](https://my-json-server.typicode.com/telegraph/frontend-exercise/comments)

### :mag_right: What we are looking for

* An understanding of web fundamentals
* A consistent and scalable approach to the test
* An understanding of accessibility
* Reasoning about web performance
* Reasoning about SEO
* Solid unit testing
* Ability to translate designs

### :open_file_folder: Data

* Article data: `server/content/article.json`
* Posts: `server/content/posts.json`
* Meta: `server/content/meta.json`
* Comments: [https://my-json-server.typicode.com/telegraph/frontend-exercise/comments](https://my-json-server.typicode.com/telegraph/frontend-exercise/comments)

### :art: Designs

* The designs are in [Figma](https://help.figma.com/article/116-getting-started) and can be found [here](https://www.figma.com/file/aNhLCCBFArm2CgETeo47lV/Article-Template)
* You can toggle the grid on and off by clicking the hamburger menu (top left) and selecting `View > Layout Grids`.

## :floppy_disk: Set up

Firstly, install all of the packages:

```sh
npm install
```

Then run:

```sh
npm run dev
```

Visit [http://localhost:3000/](http://localhost:3000/) in your web browser and you *should* see a blank webpage with The Telegraph logo and a 'Hello World' message.

The above command will watch and deploy your code. The watchers for CSS and JS files will not take into account changes to new files so make sure you restart the watchers when adding new files.

## :scroll: Acceptance criteria

```
Scenario: Show single post
	Given that I submit the path of the article into the browser
	And the path is "/einstein-and-churchill-both-took-daily-naps"
	Then the post page should be returned
	And the page shows the title of the article
	And the page shows the standfirst of the article
	And the page shows the date of the article
	And the page shows the image of the article
	And the page shows the associated comment count of the article
```

```
Scenario: Show associated articles
	Given that I access the single post page
	Then the post page should return associated posts by category
	And each item should show the title of the article 
	And each item should show the date of the article
	And each item should show the thumbnail of the article
	And each item should show the premium label if premium
```

```
Scenario: Show comments
	Given that I access the single post page
	Then the post page should return the associated comments
	And each comment should show the username
	And each comment should show the date of the comment
	And each comment should show the comment body
	And each comment should show the like count
```

```
Scenario: Order comments by newest
	Given that I click the Newest button in the comments area
	Then then the comments should display in order of date
	And the comments should show most recent first
```

```
Scenario: Order comments by likes
	Given that I click the Likes button in the comments area
	Then then the comments should display in order of most likes
	And the comments should show most liked first
```

## :mailbox_with_mail: Submitting your code

Please don't fork this repository as the links will be accessible to other candidates. Instead, please clone it into your own repo and send us a link. We should be able to build and run your application locally.

Please also feedback on how you found the test - what did you like/not like about it?

Feel free to send us any other additional notes. E.g. what you would have done with more time.

## TODO

- Update thumbnail sizes to match design
- Font?
