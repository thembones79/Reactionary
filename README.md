# Reactionary

Reactionary is a WordPress theme that uses WP REST API to remove WordPress completely from the front end.

PHP template files are replaced by React.js components, so this is a SPA (Single Page Application) blog.

# Modern Browsers only
Reactionary is aimed at modern browsers only, it makes heavy use of flex/flexbox and some relatively new CSS3 properties. But you can replace the CSS with anything you want, like Twitter or Foundation - that should be pretty straightforward.

# Responsive brutalism
The current styling is a sort of responsive brutalism inspired by classic chinese propaganda art.
Styling is quite lightweight, SCSS files are included (along with include-media breakpoints), so it should be fairly straightforward to restyle.


# Why?
Using WordPress as a CSM only, but dropping all the WP flavour from the front end in favour of React makes a lot of sense. 
This builds on my previous projects NoPress and ReactPress, which I've abandoned in favour of Reactionary as it does everything better, with less flab.

# Semi-static
Unfortunately, the WP REST API (v2) just is not fast enough.
So the JSON is cached in static (flat) files that are updated when posts or pages are published.

This means that you can potentially keep your WP installation offline, and just upload these files to the server:

+ index.html (in root)
+ everything in the assets folder, except:
++ scss folder
++ reactionary-source.js in /assets/js/

Unfortunately, that would pretty much break the images, so a bit of work would be needed to accomplish this - that is not the current focus of the project, but it's a good idea for a fork maybe. 