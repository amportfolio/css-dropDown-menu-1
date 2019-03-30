# CSS-Only Drop-Down Hamburger Menu 1.0

With the creation of [Basic Grid 1.0](https://github.com/amportfolio/basic-grid-1), I wanted to remove much of the features and items I never used that one normally gets with Bootstrap. However, there was one feature I used religiously and wanted in my Basic Grid — the header that collapses into a hamburger menu when you go to mobile.

Now I know hamburger menus have been a source of contention and debate in the UX community, but they are here to stay. It’s really up to the UX Designer to do everything in his/her power to make sure the end user isn’t confused on where to go. I do have plans to create a version of this menu that collapses to a smaller menu on the bottom...for those not into the hamburger.

## Before you use this...

In order to use this header and menu you will either need my [Basic Grid 1.0](https://github.com/amportfolio/basic-grid-1) framework to aid in placement, or the *container.css* included with the download. I also use [Normalize](https://github.com/necolas/normalize.css) and [Eric Meyer’s reset](http://meyerweb.com/eric/tools/css/reset/) for improved cross-browser rendering. I did include a minified version of the two with the download, or you can use your own.

## Setup and Configuration

The download contains a nested CSS file for those who don’t want to mess with SCSS *(although you should learn it...it’s so worth it)*.

For those using SCSS, you will need to open the *_config.scss* and set up these two configuration variables:

    // Number of menu items you want
    $number-menu-items: 5;

    // Individual height of menu items
    $menu-item-height: 2em;

These two configuration items are important because it’s needed to mathematically determine the height of the drop-down menu when one is in mobile. In order to semantically keep the menu an unordered list, but have the animation of the menu sliding down, a height was needed.

If you are more akin to using the straight CSS, then you’ll need to set the height of the drop-down menu on line 74 of the CSS code:

    header .headerRight input[type="checkbox"]:checked ~ nav {
        height: 10em;
    }

Your final number should be the **&number of items in your menu multiplied by the height of each item item as you see fit**.

You’ll also need to decide if you want the menu to be fixed at the top or scroll with content. Just a true or false on this configuration variable:

    // Should this menu be fixed at the top?
    // Place "true" in the variable if you want to,
    // or "false" if you do not.
    $menuFixed: false;

The fonts and colors are up to you, but you can also change the labels that go on the menu button itself. Just be aware that you might have to tweak the placement in the CSS depending on what you enter.

    // Labels for the button that go under the hamburger.
    // Bear in mind you might have to play with the
    // placement depending on what you put.
    $menuTerm: "Menu";
    $closeTerm: "Close";

## Examples

I have examples on Codepen.

* [Original Menu](https://codepen.io/amportfolio/pen/LydMdz)
* [Fixed-Top Sticky Menu](https://codepen.io/amportfolio/pen/vZjpOV)
* [Amanda Neff's Menu](https://codepen.io/amportfolio/pen/pwKyEd) (honorable mention) 

## Questions? Comments? Suggestions?

Please feel free to reach out or fork this and improve on it.

## Authors

* **Alex Moschopoulos** - *Initial work* - [amportfolio](https://github.com/amportfolio)

## Acknowledgments

* Bootstrap...it was a nice start, but it drove me to push for more.
* SCSS...I love it