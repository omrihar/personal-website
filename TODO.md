# Ideas and DODOS for the website

## Ideas

### The website will contain:

1. Personal biographical information.

2. Academic projects I made during my studies:
    
    - M.Sc. thesis on using non-linear Thomson scattering to measure intense 
      laser fields.

    - Ph.D. project on measuring Fisher's information non-parametrically.

    - Ph.D. project on the Gray-Scott Reaction-Diffusion model

    - Ph.D. project on electric vehicles.

    - Ph.D. project on Subaks.

    - Ph.D. project on the simulation framework.

3. Personal / work projects

4. Blog posts.

5. Book / Movie / Podcast recommendations

### Types of content necessary to support this

- [ ] Text and images (markdown / html)

- [ ] LaTeX equations.

- [ ] Code snippets.

- [ ] Interactive visualizations (probably using `Plotly.js`).

- [ ] Running of backed python code to create interactive tools (for 
  gray-scott, Subaks dashboard, etc...) - probably using Heroku or serverless 
  using AWS Lambda functions.

### Design considerations

1. I don't want to have to recompile the front-end every time I add a new blog 
   post or project. Ideally it would be a `jekyll` like setup where new 
   markdown files will be compiled to pages on the front-end.

2. However I don't want to have a database on the backend. So I'll need to have 
   something like a `posts` folder that will contain the files which the 
   backend will parse and send to the frontend. A possible format for this 
   could be YAML files, maybe even markdown with YAML header such as jekyll 
   files.

   Resources:

   [1] 
       [https://github.com/goodwordalchemy/flask-jekyll](https://github.com/goodwordalchemy/flask-jekyll)

## TODOs

- [ ] Design the front-end.

- [ ] Plan the architecture for the backend.

- [ ] Create the content.

- [ ] Repeat.
