xl-activetabs
============================

AngularJS Directives for activating any tab(s) that match the current $location.path()
************
It's one of the most fundamental of UI constructs: the humble tab interface. It's familiar and effective. So, for any UI dev, the goal is to not only provide tabs for UI, but also to show the user which tab is currently active. In Angular, we want such interfaces to all be declarative and data-driven, and preferably to be aware of the $location service. 

One good Angular-compatible example of a Tabs interface is the [Angular-UI project's version of Boostrap's Tabs](http://angular-ui.github.io/bootstrap/#/tabs). It works well, but you may not want to trouble yourself to put the Bootstrap CSS into your project, and you may not like their \<li\>-driven approach to the tab elements. It also may just be more complex or verbose than you need.

So, if Bootstrap Tabs aren't for you, this version should be right up your alley. It's simple, declarative, doesn't require any special payloads on the route, and is reusable across contexts without code modification. It's designed for use on basic \<a\> elements, regardless of whether you wrap them in an \<li\> or not. (Assuming you structure your CSS correctly to make the anchors into blocks.)

It comes in two versions: one for use on individual tabs/anchors (xl-detect-active-tab), and one for use on the parent element of all the tabs (xl-find-active-tab). You can simply include the 'xml-activetab' module as a dependency of your main Angular module, which will make both flavors available to you, or you can copy/paste the directives and instantiate them directly off of your own Angular module(s). 

There are explanatory comments inline in the directive source, and more documentation about these directives can be found in the [StackOverflow Question](http://stackoverflow.com/a/17496112/800457) that inspired me to release them. (As noted there, you can in fact use the detect-active-tab directive with Bootstrap-style HTML, by simply changing line 28 to `element.parent().addClass("active");`)
