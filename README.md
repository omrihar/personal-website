# Omri Har-Shemesh's Personal Website

This is my (soon-to-be) new personal website, which is based on the 
beautifully-made 
[Flask-Vuejs-Template](https://github.com/gtalarico/flask-vuejs-template).

In the hopes of turning this to my first blog post on the new website, I'll 
first document here in `README.md` my progress in developing the website.

## First step: set-up git flow

In my development I try to always follow the [git-flow][1] pattern. Since I'm
git kraken it is very easy to set up the repository to use git-flow. Just head
to the settings section and choose the naming style for the branches. This time
I just used the defaults, even though I tend to replace the forward slashes
`/` with dashes `-`.

[1]: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow


## From Vue.js to Quasar Framework

I'm a big fan of the [Quasar Framework](https://www.quasar-framework.org) which is a 
Vue.js implementation of Material UI. If you don't know it I urge you to go 
over to their website and have a look. The lead developer behind the framework 
is really dedicating a lot of his time and efforts to this framework and it is 
rapidly growing, both in terms of capabilities as well as community.

So my first step in adapting this template was to remove the `vue_client` and 
initialize a quasar template instead. You can see the commit log to the exact 
changes necessary, but it basically amounts to removing `vue_client`, running 
something like `quasar init frontend` and changing some references to 
`vue_client` in the Flask app.

Now that I have a working quasar app, it's time to design the website...

## Choosing a color scheme

I tried to find a good color scheme that will make the content pop and the 
website fall in the background. Since I'm not a designer I decided to browse 
around the web to find a nice color combination that will work for me. I really 
like the feeling of brown, earthy colors and tried to find a good color palette 
to reflect that preference. There are many websites that offer a long list 
(typically 25 or 50) of color schemes and knowing in which direction I want to 
take the website helped to narrow it down to only one or two from 50. I decided 
to simply try one out, build a simple layout using these colors and if it 
doesn't work, change the colors. Since they are stored in `stylus` variables 
it's not very difficult to replace later on.
 
 Since I'm not a designer and coming up with a complete concept of the layout 
 as I want it proved to be difficult, I decided to start working on the content 
 and later on incrementally improve the design as well.


