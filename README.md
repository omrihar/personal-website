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


## From Vue.is to Quasar Framework

I'm a big fan of the [Quasar Framework](https://www.quasar-framework.org) which is a 
Vie.as implementation of Material UI. If you don't know it I urge you to go 
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

## Content backend

The next step is to set up the back and front end to display content. I want 
something that simulates `jekyll` in the ease of publishing new content - which 
means I want a format such as markdown with YAML headers, that will be 
converted to content the front-end can display. 

For this end, I want the API to discover files in a predefined directory of the 
website, serve them based on the content of the YAML header, and display them 
on the client side. One obvious field in the YAML header will be whether it is 
a draft or published material, another is type (blog post, project description, 
resource, cv entry, etc...). Ideally the content of the files will be able to 
handle complex things such as embedding a small JavaScript application. A 
second approach would be to simply include an IFrame in the body. 

### YAML specification

| Field | Description |
| ----- | ----------- |
| `title` | Title of the content. |
| `date` | Publication date. |
| `subtitle` | If relevant, a subtitle |
| `draft` | Is this in draft status, or published |
| `type` | `'blog'`, `'project'`, tbd |
| `section` | In which section of the website should this appear? |
| `tags` | Relevant tags |
| `resources` | A list of relevant resources such as links, articles, repos, 
etc... |
