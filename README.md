Barta
Barta is a dynamic social application built with Laravel, designed to enable seamless user interaction through posts, comments, and likes. With a focus on performance and usability, Barta provides real-time updates, advanced search capabilities, and comprehensive user profile management. 

✨ Features
Core Features
User Authentication & Authorization: Secure login, registration, and email verification.
Post Creation (Barta): Users can create posts with optional photos.
Nested Commenting System: Two-level replies to enhance discussions.
Redis-Powered Like System: Efficient and scalable implementation for likes.
Real-Time Notifications: Powered by Laravel Reverb for in-app and email notifications.
Profile Picture Management: Upload and update avatars with automatic deletion of old ones.
User Profiles: View personal profiles or explore others' profiles, complete with post summaries and statistics.
Search Functionality: Find users or bartas using usernames, full names, or post titles.
Full-Image View: Show full-sized images on post detail pages.
Performance and Usability Enhancements
Optimized Query Handling: Designed to reduce database queries for faster performance.
Infinite Scrolling: Load posts and comments dynamically with enhanced performance.
Seamless CRUD Operations: All create, read, update, and delete actions are implemented without page reloads.
Real-Time Updates: Automatic datetime updates without requiring a refresh.
Image Management: Edit, update, and upload images with live previews.
💻 Technologies Used
Backend: Laravel 11.x, Redis, Laravel Reverb for Websockets
Frontend: Livewire, TailwindCSS
Queue Handling: database-powered queue workers for stability
🚀 Installation Guide
Prerequisites
Ensure a Redis server is running locally or in your production environment.
Configure a mail server (e.g., Mailpit for local or SMTP for production) for email verification.
Steps
Clone the repository
git clone https://github.com/OsimAkash/barta.git
cd barta
Install dependencies
composer install
npm install
Configure environment variables
cp .env.example .env
php artisan key:generate
Configure .env
Update database settings.
Set REDIS_CLIENT to either predis or phpredis
REDIS_CLIENT=predis
# or
REDIS_CLIENT=phpredis
Configure mail settings.
Run migrations and seed the database:
php artisan migrate
php artisan db:seed
Set up storage:
php artisan storage:link
Start the development server:
php artisan serve
Start asset compilation:
npm run dev



# Start the queue worker
php artisan queue:work
Verified User
After seeding the database, you can log in with the following credentials:

Email: jhon@doe.com
Password: password
