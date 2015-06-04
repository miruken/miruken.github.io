# Setup Guide for Running Locally
### Required dependencies: Ruby, Jekyll, Python 2.7
##### If you need help setting up Jekyll to run locally on windows refer to this guide: http://jekyll-windows.juthilo.com/

###### NOTE: Make sure that MirukenJS and miruken.github.io are locally stored in the same root folder. For example, let's assume you use \Sources for storing your repos. You will want to clone MirukenJS and the sourcecode for the website into that sources folder so that you end up with:
<pre>\Sources\MirukenJS
\Sources\miruken.github.io</pre>

I'm going to assume that you have installed ruby, the jekyll gem, and python 2.7. If you have not, I highly recommend following the guide mentioned at the head of this article if you are running windows. 

Your first step is taking note of the note, and cloning both this repo and the mirukenJS repo which can be found at https://github.com/cneuwirt/MirukenJS

You will need to work through the setup for MirukenJS (ex: run npm install / grunt install) before proceeeding to the next step.

Once you have completed that, navigate to your \Sources\MirukenJS\ folder and either via command prompt, or double click, execute the mirukendocs.bat file located in the root folder. 

This will run the necessary command to generate the docs and then copy them to the miruken.github.io project folder.

Now go back to the miruken.github.io folder and open the config.yml in a text editor. You will find on line 24
<pre>url: "https://miruken.github.io"
#"http://localhost:4000"</pre>

Comment out the http://miruken.github.io and uncomment the http://localhost:4000
###### NOTE: This was done because of a bug in the source code for the theme that does not allow the config_dev to properly override all of the links when local hosting. You will have half of your links referring to the github site, and half referring to the localhost if you do not follow this step.

From there, using powershell, or your command prompt of choice, go to your \Sources\miruken.github.io folder and run 
<pre>jekyll serve</pre>

In your browser go to localhost:4000 and enjoy.

