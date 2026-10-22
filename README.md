# WanderStay

A vacation rental web app inspired by Airbnb. You can browse places to stay, list your own property with photos, and leave reviews. I built it as my final-semester BCA project to learn how a full-stack app comes together, from the database all the way to deployment.

It's a learning project and isn't affiliated with Airbnb.

**Live demo:** https://wonderlust-awqy.onrender.com/listings

<!--# Screenshots -->

<!-- A -->

## What you can do

- Browse all listings with photos, price and location
- Sign up, log in and log out
- Add your own listing with photos, and edit or delete it later (only the owner can change a listing)
- See where a listing is on a map
- Read and write reviews with star ratings
- Search through the listings
- Get quick feedback on every action through flash messages, like "Listing created" or "Please log in first"
- Forms are checked in the browser and again on the server

## Built with

| Area | Tools |
|---|---|
| Front end | HTML, CSS, JavaScript, Bootstrap, EJS |
| Back end | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Authentication | Passport.js (local strategy), express-session, connect-mongo |
| Image uploads | Multer, Cloudinary |
| Validation | Joi on the server, Bootstrap validation in the browser |
| Maps | Mapbox |
| Hosting | Render |

Also used: connect-flash for flash messages and dotenv for environment variables.

## How the code is organized

I followed the MVC pattern. Mongoose models hold the data, EJS views are the pages, controllers have the logic, and routes connect URLs to controllers. Keeping them separate makes the project easier to read and easier to extend later.

## Run it locally

You'll need Node.js, a free MongoDB Atlas cluster, a Cloudinary account and a Mapbox access token.

**1. Clone the repo and install dependencies**

```bash
git clone https://github.com/manishkum7/WanderStay.git
cd WanderStay
npm install
```

**2. Create a `.env` file in the project root**

```env
ATLASDB_URL=your_mongodb_atlas_connection_string
SECRET=a_long_random_string_for_sessions
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret
MAP_TOKEN=your_mapbox_access_token
```

Don't commit this file. Keep `.env` in your `.gitignore`.

**3. Start the server**

```bash
node app.js
```

Then open http://localhost:8080 in your browser.

## Deployment

The app is deployed on Render and uses MongoDB Atlas as its database. On Render, the environment variables are added from the dashboard instead of a `.env` file.

## What I learned

- How sessions and cookies keep a user logged in, and why secrets should never go into the repo
- Why validation has to happen on both the client and the server
- How an image travels from a form, through Multer, to Cloudinary, and back as a URL saved in MongoDB
- A lot of "it works on my machine" problems come down to environment variables

## What I'd like to improve

- Add automated tests
- Add pagination to the listings page
- Let users save their favorite listings

## Author

Built by **Manish Kumar** | [GitHub](https://github.com/manishkum7)

If you find a bug or have a suggestion, feel free to open an issue.
```
