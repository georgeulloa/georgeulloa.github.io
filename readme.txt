##readme
To run:
1.Install a full Ruby development environment
2.Install Jekyll and bundler gems
    -gem install jekyll bundler
3.Create a new Jekyll site at ./dev-email
    -jekyll new dev-email
4. Upzip my files and put all the contents inside of the new repo you made.
5.Change into your new directory
     -cd dev-email
5. Build the site and make it available on a local server
    -bundle exec jekyll serve
Now browse to http://localhost:4444

If lost check out:
https://jekyllrb.com/docs/installation/
or
https://jekyllrb.com/docs/front-matter/
(this is what I needed to refer to to get liquid to compile)


Notes:
Normally I build emails from a blank template and create my own styles and classes as dictated
by the art asset. I didn't want to deviate too much from the style sheet so I built on top of that.
Ideally I would reduce and optimize the styles but for me the focus of the project was to learn
Jekyll!

So let me run you through what I made.
-Needed to load the json so instead of making the email static I wanted to leverage the JSON file.
-created _data folder, loaded json, then using front matter loaded the short code in the header to run liquid
- adjusted the json file to capture the vars requested in the notes such as merge vars.
-Created a data set for the suggested sub and products so that way I could use conditional liquid loops to generate content rather than make it by hand.
-Loaded images into s3 then added it to the json so it can pull the images when it compiles.
-filled out missing data information such as "edit_future_order" to capture the content in the sketch file and make it easy for
calling it into the email.
-Used liquid conditional logic to call in content as requested by the sketch.

Then upon learning about liquid/jekyll I stumbled onto includes and transformed my content blocks to the use % include name_of_component.html%
to modularize my email.

Things I would change.
I think self reflection is important and I admit deviated from the design in the mobile card stacking. When building I was unable to get the style of the product cards for mobile viewing just right, so I went for a vertical stack. If I had more time I would go back and adjust the mobile styles to better match the sketch file. Also as mentioned I would have streamlined my styles for better readability. I would have also included alt tags if given.

Hope you enjoy! Had a ton of fun learning a new way to make email and I hope you enjoy my work!



