#Milestone Project 3 (Paddy Boyle photography showcase website)
 
##Initiation -

For the Interactive Data-Centric Development Milestone Project (project 3), I have decided to update a website for my client 
Paddy Boyle. He needs a website that showcases his property photography. I previously developed his old website 
http://www.pboylephotography.com/ and I think it needs updating to look more modern.
 
##£Kickstarter Meeting -

After talking with Paddy, we decided on a few main points, he needs different categories for his photo galleries, i.e:

- Architecture
- Commercial
- Property
- Construction 

He would also like an **about page**, a **services page** and a **contact page**.
 
##£Thoughts after the meeting:

It seems that Paddy wants a simple showcase website. He would like it to be a corporate looking site with a green colour 
scheme. I will be able to reuse a lot of the content from the old site (images, text).
 
 
##Main Technology Requirements for Project -

###Required:

- HTML & CSS - I will be able to use bootstrap to structure and style the front end of the site. The about page, services and 
contact page should be easy enough to implement with this framework.
- Javascript - Relevant Javascript could be used for lightbox galleries and contact form.
- Python & Flask - I think categorized photo galleries would be a good way to implement flask templates with Python. Also a 
navbar template for every page on the site.
- MongoDB - I can use the MongoDB DBMS with JSON framework to store data about the images and maybe add a text area so that 
you can comment on individual images. This user functionality will incorporate the CRUD processes.
 
##Plan -

###Initial UX/UI Development -

- Home Page - I have had a research into contemporary photography websites and settled on a simple homepage design that shows 
a striking image provided by paddy. He will be providing all of the Images for this project. This image will be full width and height. 
- Nav Bar - A nav bar across the top will be stuck to all pages as a template. This will encompass the about page link, a drop-down 
category page link list, the services link and the contact page link.
- About Page - Here I will have paddy write a bio and description of his profession.
- Category pages - With the use of the MongoDB DBMS I will call data from their servers to populate these photo galleries. A simple 
bootstrap gallery will suffice. I will format all the images so the y are the same size which will make the layout easier to make 
responsive.
- Prices Page - I can also input data from the database to describe the different costs of services on the services page. I will 
use a bootstrap gridded layout.
- Contact Page - I will use the gmail API to implement a contact form with a bootstrap themed form.
 
###Wireframe Sketches -

I decided to use a bootstrap theme to save time.
 
##Documentation -

I decided to use the GitPod IDE for this project because I couldn’t install pymongo in Cloud9. I thought it would be best 
if I started with the home page first so I could make a template that was consistent throughout the website.

Firstly I created a virtual environment so anything I store will be contained inside this scoped environment. I then 
Installed the relevant frameworks to VSCode, this included: flask, pymongo, flask-pymongo and dnspython. Then I added app.py 
to run my python code along with the Procfile and requirements.txt for the modules I would be needing. I then initiated a 
local git repository and added my progress with an Initial commit.

To make an outline for the entire application I opened up app.py and imported Flask. I then tested it using the relevant 
routing and the text “Hello World” to be shown in the browser as a test to see if all was running well.

I then created a static folder and a templates folder, adding an index.html file to the templates. Re-routed the index 
function to open the index,html and tested it using “Hello World two”.

For template inheritance I created a base.html and inserted boilerplate html and the ginger2 code block syntax for the head 
and the body. Then I added the relevant syntax to the index.html for template inheritance extension. I tested it using the H1 
“Testing” and ran the program.

I used a bootstrap theme from https://startbootstrap.com/ to save time I copied the head and navbar and pasted it into the 
base.html. This way all pages on the site will have this template. In the index.html I pasted the rest of the code into the 
flask body code block. I now had a layout for my homepage wher the **about**, **portfolio**, **prices** and **contact** all 
live. I added some bootstrap code for an image carousel and an image layout for the portfolio categories. I used an old contact 
form from a previous project to save time too. The website seemed to be working well and was fully responsive. The site was 
looking quite corporate which is what the client wanted. Using the content from the old site I filled in the about section, 
portfolio section and prices section. I also created a second base.html (base-002.html) which is a template for the separate 
gallery pages. I added some css styling to the main css file that came with the bootstrap theme to conform with my clients 
specification. Once I had the layout for the index page and the gallery pages set I needed to add the images.

I used a website called https://imgbb.com to upload all the images for the site. I had all these from his old site. By uploading 
all these images I gained a url link to each one. I then created individual database collections for each category and property 
in https://mongodb.com . Inside these collections I created data documents, including a photo name and a URL for each photo.

Using python and Flask I made functions for each gallery that loop through their related photo database on MongoDB and show them 
in the browser. The category galleries were a bit trickier as I need them to link to their respective property galley with a href 
which I couldn’t do with html, so I added an extra piece of data to each document, a link that would connect each photo to 
individual property page and added it into the flask loop. 

Once I had all the galleries finished I connected the contact form to the gmail API and got that functioning. All my documentation 
is backed up with regular Git commits. I then deployed the site with Heroku.

I think this project has shown that I am competent in building full-stack websites that use common dataset. All the images on 
the site apart from the carousel are kept in a MongoDB database and are accessed by utilising Python, Flask and pymongo.
 

