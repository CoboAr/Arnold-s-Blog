# Arnold's blog

## Requirements
On the integrated terminal on Pycharm run:

On Windows type:     
python -m pip install -r requirements.txt

On MacOS type:       
pip3 install -r requirements.txt

This will install the packages from requirements.txt for this project.

## What is Arnold's blog?

It a website with a collection of different blog posts that express my interests. Different users can register, read the posts, comment, and start discussions.

## How does it work?
<ul>
<li>The website is managed by the admin, which is the first registered user. The admin, can post a new blog post, can edit any of these blog posts, and delete them. </li>
<li>New users can be registered by providing an email address, a password, and a name. </li>
<li> All registered users can login and those users that do not have admin priviledges, can only comment on a blog post.</li>
<li>3 relational databases are created to manage the relationships between users (database), comments(database), blog_posts(database)</li>
<li>Registered and non registered users have the possibility to contact the admin through a webform.</li>
</ul>

## Demo on local host

https://github.com/CoboAr/Arnold-website-blogs/assets/144629565/3706a8af-a5f5-48fe-b2dc-5eec5b7b9027

## Deployment
To deploy this website I have used [Render](https://render.com/). It has a free tier which will be more than enough for demonstration purposes.  

<uL>
<li>
  Step 1. Setup a WSGI server with gunicorn (gunicorn is added to the requirement.txt file).    
</li>
<li>
Step 2. Create a Procfile    
Add the following into the Procfile:       
web: gunicorn main:app   
</li>
<li>
Step 3. Create a git github repository and push the local project into the remote repository.   
</li>
<li>
Step 4. Sign up to https://render.com/ and create your web service.  
</li>
  
<img width="307" alt="Screenshot 2024-01-05 at 12 52 12 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/0e7d6947-bd7a-48d3-8b8a-e097f0d89b73"> 

<img width="489" alt="Screenshot 2024-01-05 at 12 53 58 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/83aef18b-2e48-440b-8141-a05683934d71">

Copy/paste the link of your repo and click continue.

<img width="824" alt="Screenshot 2024-01-14 at 5 01 49 PM" src="https://github.com/CoboAr/Arnold-s-blog/assets/144629565/e33f04ac-2c75-44c6-8bbd-6b4b6f38c1c5">

Edit the Start Command to:

gunicorn main:app

<img width="1434" alt="Screenshot 2024-01-05 at 12 58 36 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/cdb616ec-6245-4198-b1e0-5db4eb2b4f05">


Add Environment variables FLASK_KEY, EMAIL, PASSWORD:

<img width="1248" alt="Screenshot 2024-01-05 at 1 00 55 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/48088540-85e2-4b71-91e4-44a48dc2cd7f"> 

Scroll to the bottom and create your web service.

<li>

Step 5. Upgrade SQLite Database to PostgreSQL
</li>
<ul>
  <li>
    Create a new Postgres Database
  </li>
  <li>
    Pick a name for the database and create it.
  </li>
  <li>
    Copy the internal database URL
  </li>
<img width="1348" alt="Screenshot 2024-01-14 at 5 16 24 PM" src="https://github.com/CoboAr/Arnold-s-blog/assets/144629565/32cad82d-2270-4e76-b6ac-54fdd8a02a45">
  
<li>
  Set your SQLALCHEMY_DATABASE_URI environment variable   
  Go back to  web service settings called "environment".  Create an environment variable that matches the name of the key you're using in the main.py.    
  
</li>
<img width="1038" alt="Screenshot 2024-01-14 at 5 19 38 PM" src="https://github.com/CoboAr/Arnold-s-blog/assets/144629565/0b8bb7c8-8ca0-4ca1-8952-8f68c81bd963">
<li>
  Paste  internal database URL as the key value. It should look something like this
</li>

<img width="574" alt="Screenshot 2024-01-05 at 1 12 21 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/af2a061a-55a7-42d0-9368-2111dcfccb90">

<li>
  Change the first part from postgres to postgresql. The URI has to start with "postgresql" because this is required by SQLAlchemy:
</li>
<img width="564" alt="Screenshot 2024-01-05 at 1 13 15 PM" src="https://github.com/CoboAr/Rank-your-10-best-movies/assets/144629565/20fefaf7-f96d-44c7-9a61-e0de620603a4">

<img width="1278" alt="Screenshot 2024-01-14 at 5 22 02 PM" src="https://github.com/CoboAr/Arnold-s-blog/assets/144629565/bc33302c-9a1b-4f2e-9ca0-41e7864d6be6">

</ul>
</ul>

## Demo Deployment 

Website link: [https://top-10-movies.onrender.com  ](https://top-10-movies.onrender.com)  
Domain can be customized upon desire.
The link might not be functional by the time you are checking it, because a free tier of Render is being used.


https://github.com/CoboAr/Arnold-s-blog/assets/144629565/402ce5bd-387f-4451-bc3e-88898bc1ddcd

Enjoy! And please do let me know if you have any comments, constructive criticism, and/or bug reports.
## Author
## Arnold Cobo
