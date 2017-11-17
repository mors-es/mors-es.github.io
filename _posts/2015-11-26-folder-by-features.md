---
title: 'AngularJS: folder-by-features'
date: 2015-11-26 14:15:00 Z
tags:
- AngularJS
- JohnPapa
- Atom
- files-icon
description: Organise your files by components
image: "/assets/images/posts/ng-folders.png"
---

Four months ago, I've started to learn to code. Maybe later I'll make an article about my journey, but for now, I just wanted to share a little trick for all the developer who code with the awesome AngularJS framework and with the [Atom](http://atom.io) editor. I'm working as a front-end developer in a Belgian startup and last week I've to refactor the entire files structure of their Angular App. I choose to follow the [JohnPapa's recommendation](https://github.com/johnpapa/angular-styleguide). I recommended to check all of his advice and the [posts](http://johnpapa.net/angular-app-structuring-guidelines/) on his blog, it's super clear and well explained.

When you start to use his syntax (`name-of-the-file.type.extension`) and his folder's structure  (view next to his controller), it's much more easy to work on a new feature. But sometimes, you can't identify directly the right file. To helping you, you can install a cool package called [files-icon](https://atom.io/packages/file-icons). Since the package include all the icons from [FontAwesome](http://fortawesome.github.io/Font-Awesome/), you can parameter your own configuration. Here how it looks.

![folder-by-features](/assets/images/posts/ng-folders.png)

The must, it's when you have a lot of tabs opened and you have to quickly find the right file :-).

![folder-by-features](/assets/images/posts/tab-folders.png)

> Some of the icons ( `.factory-icon` ) come from the last update of FontAwesome and are not yet compatible with the package. I made a pull request in their repo to use them, meanwhile you can update manually in the package's path ( *resources > fonts > fontawesome-webfont.woff* ).

Here is the *CSS* configuration we use now. You have to copy-paste it in your Stylesheet in Atom (on OS X -> menu: *Atom > Open Your Stylesheet*).

```scss
// YOUR-APP-Angular config

@import "packages/file-icons/styles/colors"; // to use the colours
@import "packages/file-icons/styles/icons";  // to use the defined icons
@import "packages/file-icons/styles/items";

.factory-icon   {
  .fa;
  content: "\f275";
}
.ctrl-icon      { .fa; content: "\f11b"; }
.view-icon      { .fa; content: "\f06e"; }
.route-icon     { .fa; content: "\f018"; }
.module-icon    { .fa; content: "\f12e"; }
.run-icon       { .fa; content: "\f04b"; }
.filter-icon    { .fa; content: "\f0b0"; }
.spec-icon      { .fa; content: "\f0c3"; }
.decorator-icon { .fa; content: "\f1fc"; }
.modal-icon     { .octicons; content: "\f0c5"; }

// here you can put your own logo in .svg for the main app.js file
.app-icon       { content: url('data:image/svg+xml;utf8,<svg/>...</svg>') }

@{pane-tab-selector}, .icon-file-text {
  //for use your custom config only on specific folder
  &[data-path*="angular"] {  

    &[data-name*=".ctrl"]:before           { .ctrl-icon; .dark-yellow; }
    &[data-name*=".html"]:before           { .view-icon; .light-yellow; }
    &[data-name*=".modal.html"]:before     { .modal-icon; .light-yellow;}

    &[data-name*=".directive.js"]:before   { .code-icon; .dark-blue; }
    &[data-name*=".directive.html"]:before { .view-icon; .light-blue; }

    &[data-name*=".factory.js"]:before     { .factory-icon; .dark-green;}
    &[data-name*=".service.js"]:before     { .factory-icon; .dark-green;}
    &[data-name*=".filters.js"]:before     { .filter-icon; .light-pink;}

    &[data-name*=".route.js"]:before       { .route-icon; .dark-purple;}
    &[data-name*=".module.js"]:before      { .module-icon; .medium-pink;}
    &[data-name*="run.js"]:before          { .run-icon; .light-maroon;}
    &[data-name*="config.js"]:before       { .config-icon; .dark-cyan;}
    &[data-name*="app.js"]:before          { .app-icon; .dark-cyan;}
    &[data-name*=".spec.js"]:before        { .spec-icon; .dark-cyan;}
    &[data-name*=".decorator.js"]:before   { .decorator-icon; .dark-green;}
  }
}
```
