---
title: Drawer
meta_title: Documentation for Kendo UI Drawer mobile widget
meta_description: How to initialize and use a mobile Drawer component in Kendo UI Mobile framework.
slug: gs-mobile-drawer
relatedDocs: api-mobile-drawer
tags: getting-started,mobile
publish: true
---

# Drawer

The Kendo Mobile Drawer widget provides slide to reveal global mobile application toolbox or navigation.

## Getting Started

The Kendo mobile Application will automatically initialize a mobile Drawer widget for every `div` element with `role` data attribute set to `drawer` present in the **mobile application DOM element** (same level as the application views).
The Drawer element may contain optional header and/or footer. A mobile scroller is automatically initialized around the contents of the element.

By default, the drawer will be revealed at the left side when swiping from from left to right.  The position can be changed using the `position` configuration option (`left` or `right`). One application can have up to two drawers (left and right one) active at the same time.

The drawer automatically hides when the user swipes back or taps the remaining visible area of the view. The drawer also hides automatically when the application navigates to another view.

### Drawer and a reveal button

    <div data-role="view">
        <a href="#foo" data-rel="drawer" data-role="button">Drawer</a>
    </div>

    <div data-role="drawer" id="foo">
        <div data-role="header">
            <div data-role="navbar">
                <span data-role="view-title">Hello World!</span>
            </div>
        </div>

        <ul data-role="listview">
            <li>Foo</li>
        </ul>

        <div data-role="footer">
           <div data-role="navbar">
               <a data-align="right" data-role="button">Details</a>
           </div>
        </div>
    </div>


### Drawer with view navigation links

    <div data-role="view" id="foo">
        Foo
    </div>

    <div data-role="view" id="bar">
        Bar
    </div>

    <div data-role="drawer">
        <ul data-role="listview">
            <li><a href="#foo">Foo</a></li>
            <li><a href="#bar">Bar</a></li>
        </ul>
    </div>



## Revealing a Drawer

In addition to responding to user swipes, the widget can be open when any mobile navigational widget (listview, button, tabstrip, etc.) is tapped.
To do so, the navigational widget should have `data-rel="drawer"` and `href` attribute pointing to the Drawer's element `id` set (prefixed with `#`, like an anchor).

### Button revealing a Drawer

    <div data-role="view">
        <a href="#foo" data-rel="drawer" data-role="button">Foo</a>
    </div>

    <div data-role="drawer" id="foo">
        ...
    </div>
