# littlepioneer-gulp:  [Little Pioneer Cider House](http://littlepioneer.com/)

## What is this

Little Pioneer Cider House is a side project that I have been working on since 2015.  It is a github page site for a friend who produces music and an absolute pleasure to work on.

The first incarnation of this site has been hand optimized.  Every image is preprocessed through tiny PNG, every page is compressed by hand, the style sheets minified by hand, the github-pages branch rebased off of master frequently, etc cetera.  (You can check it out [here](https://github.com/ninjaofawesome/littlepioneer-v2).)

As it wasn't regularly updated, it was semi-maintainable, but clearly not an ideal situation.  Thus, littlepioneer-gulp does all the heavy lifting through gulp tasks, and even deploys to github for me!

## How do I fire this up?

`npm start`

## How do I build this thing?

`npm build`

## How do I deploy it for the world to see?

`npm run deploy`

## Where do I put pages?

In the app directory.  If you like, you can modify the gulp task to watch a page directory, it can be found on line 66 of gulpfile.js.  However, you should leave the index page out of there as a point of entry.

## Where do I put my sass files?
In the scss subdirectory.  There's a manifest called styles.scss.  You can link to any subdirectories with partials there.  In the head of your document that you require these files, you will also want to add the following right above the closing head tag.

```
<!--build:css css/styles.min.css -->
    <link rel="stylesheet" href="./css/styles.css">
<!-- endbuild -->
```

## Where do I put any additional JS files?

In the js subdirectory.  In the body of your document that you require these files, you will also want to add the following right above the closing body tag.

```
<!--build:js js/main.min.js -->
  <script src="./js/my-file-name.js"></script>
  <script src="./js/my-other-file-name.js"></script>
<!-- endbuild -->
```