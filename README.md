# Test_capstone

IMAGIME
Database Schema:

Tables for:
Users: Contains user account information (username, email, password, profile image).
Posts: Stores information related to user posts (image, description, associated user ID).
Songs: Details about songs retrieved from the Spotify API (title, artist, preview URL, album artwork).
PostSong: A join table linking posts to songs, enabling multiple songs to be associated with a single post.
FavoritedSongs: Tracks songs favorited by users, linking both the user and the specific song.
API Issues:

Spotipy API: Handle data inconsistencies from the Spotify API, such as missing preview URLs or album images. Ensure robust error handling when fetching song details based on keywords.
Everypixel API: Manage potential mismatches between keywords generated from uploaded images and available songs on Spotify. Implement error handling when no keywords are found or when the keyword-to-song mapping fails.
Sensitive Information:

User Account Details: Securely store user credentials and profile images. Ensure encryption and safe handling of passwords. Manage user sessions to prevent unauthorized access.
Uploaded Images: Protect personal or sensitive content in user-uploaded images.
Functionality:

Image and Song Integration: Users upload an image, which is analyzed to generate keywords that map to related songs from the Spotify API. These songs are displayed alongside the image.
Favorites System: Users can favorite songs associated with any post. Favorited songs are stored in the database, and users do not see the favorited status unless they also favorited the song.
Dynamic Content Loading: Implement a "Load More" button to load additional songs without a full page reload, enhancing user experience.
User Flow:

Sign-Up/Login: New users create an account with a username, email, and optional profile image. Existing users log in to access personalized content.
Post Creation: Users upload images and optionally add descriptions. The app matches the image to songs based on generated keywords.
Interaction with Content: Users view posts, listen to preview songs, and favorite tracks. They can also view a list of favorited songs and navigate back to the original post from the favorited songs list.
Stretch Goals:

Enhanced Recommendations: Suggest songs or images based on a user’s favorited content.
Community Features: Allow users to comment on posts, share favorite posts, or rank songs/images.
Advanced Search Options: Enable users to search posts by keywords, song titles, or users. Implement filtering options for refined searches.
Custom Playlists: Allow users to create playlists based on favorited songs or matched songs from uploaded images.
Instruction

Description:
Imagime is a platform that allows users to upload images and discover songs that match the mood or theme of the images. It offers a unique way to remember moments in sound by combining visual memories with music.

Stack

Tech stack used for the project:

HTML/CSS
JavaScript (with Bootstrap)
Python/Flask
SQLAlchemy/PostgreSQL
Focus

Is the front-end UI or the back-end going to be the focus of your project? Or are you going to make an evenly focused full-stack application?

The project is evenly focused on full-stack development, with significant attention to creating a seamless, visually appealing UI, backed by robust back-end functionality. The UI aims to provide an intuitive and engaging experience, while the back-end handles complex data processing and API integrations.

Type

Website: Imagime is developed as a responsive web application accessible on various devices.

Goal

What goal will your project be designed to achieve?

The goal is to provide users with an interactive platform where they can combine visual memories with music, creating a unique and personalized experience. The app aims to make it easy for users to upload images, match them with songs, and curate their favorite tracks.

Users

What kind of users will visit your app? In other words, what is the demographic of your users?

The app is designed for music enthusiasts, photography lovers, and general users who enjoy combining visual art with music. It targets anyone who wants to enhance their memories with a musical backdrop.

Data

What data do you plan on using? How are you planning on collecting your data?

Data Sources: Spotipy API for song data, Everypixel API for generating keywords from images.
Data to Collect: Songs matching uploaded images, user-generated posts, favorited songs.
Collection Method: Data is collected dynamically through API calls based on user interactions, with data stored in a relational database for a persistent user experience.
