# Django Registration and Login System

This web app has been developed using the popular Django framework and Bootstrap for the frontend. My motivation to build this project is so that I can learn about Django and tighten up my skills. This mini-app can be easily integrated into a bigger system project that needs to have a registration and login system.

### Basic Features of The App
    
* Register – Users can register and create a new profile
* Login - Registered users can login using username and password
* Social Apps Login – Users can login using their GitHub or Google account
* User Profile - Once logged in, users can create and update additional information such as avatar and bio in the profile page
* Update Profile – Users can update their information such as username, email, password, avatar and bio
* Remember me – Cookie Option, users don’t have to provide credentials every time they hit the site
* Forgot Password – Users can easily retrieve their password if they forget it 
* Admin Panel – Admin can CRUD users

![ScreenShot](https://user-images.githubusercontent.com/66206865/131695930-648342b0-010b-44b2-a419-15ad54d47869.png)

## Tutorial
[Here](https://dev.to/earthcomfy/series/14274) is a tutorial on how to build this project.

### Quick Start
To get this project up and running locally on your computer, follow the following steps.
1. Set up a python virtual environment
2. Run the following commands
$ pip install -r requirements.txt
$ python manage.py migrate
$ python manage.py createsuperuser
$ python manage.py runserver


   
3. Open a browser and go to http://localhost:8000/

## Deploy to Vercel

You can deploy this Django application to Vercel with just one click using the button below:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/your-username/your-repository-name)

### Steps to Deploy

1. **Fork or Clone the Repository:**
   - Fork this repository or clone it to your local machine.

2. **Set Up Environment Variables:**
   - Create a `.env` file in the root of your project directory with the following content:
     ```plaintext
     SECRET_KEY=your_secret_key_here
     GITHUB_KEY=your_github_key_here
     GITHUB_SECRET=your_github_secret_here
     GOOGLE_OAUTH2_KEY=your_google_oauth2_key_here
     GOOGLE_OAUTH2_SECRET=your_google_oauth2_secret_here
     EMAIL_HOST_USER=your_email_host_user_here
     EMAIL_HOST_PASSWORD=your_email_host_password_here
     REDIS_URL=your_redis_url_here  # e.g., redis://<username>:<password>@<host>:<port>/<database>
     ```

3. **Deploy with Vercel:**
   - Click the "Deploy with Vercel" button above.
   - Connect your GitHub account if prompted.
   - Import the repository.
   - Set the environment variables in the Vercel dashboard to match those in your `.env` file.
   - Deploy your project.

### Additional Considerations

- **Static Files:** Ensure that static files are collected correctly by running `python manage.py collectstatic` locally before deploying.
- **Database:** Vercel does not provide persistent storage for databases. Consider using a managed database service like Heroku Postgres, AWS RDS, or any other cloud-based database service.
- **Media Files:** Similarly, Vercel does not provide persistent storage for media files. Use a service like AWS S3, Google Cloud Storage, or any other cloud-based storage service.
