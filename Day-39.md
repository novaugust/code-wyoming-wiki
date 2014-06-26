## Ghost Development

### Steps

1. Install [NodeJS](http://nodejs.org/)
    This is the program that runs our server code. It installs two command line programs, `node` and `npm`.
2. Clone Ghost from https://github.com/TryGhost/Ghost.git
3. Follow the [ghost development installation guide](https://github.com/TryGhost/Ghost#getting-started-guide-for-developers)
    1. `npm install -g grunt-cli` //installs the "grunt" command on your computer
    2. `npm install` //installs all the modules that ghost depends on, listed in package.json
    3. `grunt init` (and grunt prod if you want to run Ghost in production mode) //runs a bunch of commands to build up ghost
    4. `npm start`

From here on, if you ever need to get Ghost up and running, do a `grunt dev`. This is a nifty utility that restarts the server on file change.

### Theme Development

Ghost works with two "branches" at any one time. `master`, which is where active development is occuring and which is *not* safe (ie, don't use it on a production server - your data could break) or standardized, and then a "tagged" version, which will look like `0.x.x`.

#### Ghost Versions

Type `git tag` to see a list of every tagged version of Ghost in the repository.

Right now, `0.4.2` is the production version of Ghost. Work is being done to move to version `0.5.0` sometime in early July.

In this class, we're going to develop themes for `0.4.2` since `0.5.0` is still up in the air. Keep in mind that if you release a theme for a certain version of Ghost, it's up to you to make sure it will work with future versions as well!

Since we want to work with `0.4.2`, type `git checkout 0.4.2` and the code in the repository will switch over to the older `0.4.2` code (by default, we're looking at the latest master version).

#### Handlebars

Ghost uses [Handlebars](http://handlebarsjs.com/) to do its templating. At its most basic, handlebars is just a convenient way for accessing data out of javascript objects and printing it into our html.

##### Html Escaping
`{{` vs `{{{`

##### Comments
`{{! this is a comment}}`

##### Block Helpers
```
{{#helper}}
....
{{/helper}}
```

###### if
```html
<div class="entry">
  {{! only output this author names if an author exists }}
  {{#if author}}
    <h1>{{firstName}} {{lastName}}</h1>
  {{/if}}
</div>
```

###### each
```html
<h1>Comments</h1>

<div id="comments">
  {{#each comments}}
  <h2><a href="/posts/{{../permalink}}#{{id}}">{{title}}</a></h2>
  <div>{{body}}</div>
  {{/each}}
</div>
```


##### Helpers

###### `with` helper
Given this context
```javascript
{
  title: "My first post!",
  author: {
    firstName: "Charles",
    lastName: "Jolley"
  }
}
```

with can be used like so
```html
<div class="entry">
  <h1>{{title}}</h1>

  {{#with author}}
  <h2>By {{firstName}} {{lastName}}</h2>
  {{/with}}
</div>
```

#### Theme Folder Structure

```
.
├── /assets
|   └── /css
|       ├── screen.css
|   ├── /fonts
|   ├── /images
|   ├── /js
├── default.hbs
├── index.hbs [required]
└── post.hbs [required]
└── package.json [will be required from 0.6]
```

##### default.hbs
>This is the default layout, or base template which contains all the boring bits of HTML that have to appear on every page – the `<html>`, `<head>` and `<body>` tags along with the {{ghost_head}} and {{ghost_foot}} helpers, as well as any HTML which makes up a repeated header and footer for the blog.

>The default template contains the handlebars expression {{{body}}} to denote where the content from templates which extend the default template goes.

>Page templates then have {{!< default}} as the very first line to specify that they extend the default template, and that their content should be placed into the place in default.hbs where {{{body}}} is defined.
