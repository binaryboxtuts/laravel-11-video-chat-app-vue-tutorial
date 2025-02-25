# Laravel 11 Video Chat Application

This project is a tutorial on video chat application built with **Laravel 11**, utilizing **Breeze** for authentication, **Reverb** for real-time WebSocket communication, **Vue.js** for the frontend, and **PeerJS** with **WebRTC** for peer-to-peer video streaming.

## Features

- **User Authentication**: Implemented using Laravel Breeze.
- **Real-Time Communication**: Managed through Laravel Reverb.
- **Dynamic Frontend**: Built with Vue.js.
- **Peer-to-Peer Video Streaming**: Enabled by PeerJS and WebRTC.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- [Composer](https://getcomposer.org/)
- PHP >= 8.2
- Node.js >= 18

## Installation

Follow these steps to set up the application:

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/binaryboxtuts/laravel-11-video-chat-app-vue-tutorial.git
   cd laravel-11-video-chat-app-vue-tutorial
   ```

2. **Install Dependencies**:

   ```bash
   composer install
   npm install
   ```

3. **Set Up Environment Variables**:

   Copy the `.env.example` file to `.env`:

   ```bash
   cp .env.example .env
   ```

   Update the `.env` file with your database configuration:

   ```env
   BROADCAST_CONNECTION=reverb

   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_username
   DB_PASSWORD=your_database_password

   REVERB_APP_ID=your_local_app_id
   REVERB_APP_KEY=your_local_app_key
   REVERB_APP_SECRET=your_local_app_secret
   REVERB_HOST="localhost"
   REVERB_PORT=8080
   REVERB_SCHEME=http

   VITE_APP_NAME="${APP_NAME}"
   VITE_REVERB_APP_KEY="${REVERB_APP_KEY}"
   VITE_REVERB_HOST="${REVERB_HOST}"
   VITE_REVERB_PORT="${REVERB_PORT}"
   VITE_REVERB_SCHEME="${REVERB_SCHEME}"
   ```

4. **Generate Application Key**:

   ```bash
   php artisan key:generate
   ```

5. **Run Migrations**:

   ```bash
   php artisan migrate
   ```

## Running the Application

1. **Start the Laravel Development Server**:

   ```bash
   php artisan serve
   ```

2. **Start the Reverb WebSocket Server**:

   ```bash
   php artisan reverb:start
   ```

3. **Compile Frontend Assets**:

   In a separate terminal window, run:

   ```bash
   npm run dev
   ```

4. **Access the Application**:

   Open your browser and navigate to:

   ```
   http://localhost:8000
   ```

## Usage

- **Registration and Login**: Create a new account or log in with existing credentials.
- **Contacts Page**: View and select contacts to initiate a video chat.
- **Video Chat**: Start a video call with selected contacts using peer-to-peer connection.

## Additional Resources

For a detailed step-by-step guide on building this application, refer to the original tutorial by Binaryboxtuts:

[Building A Video Chat App Using Laravel 11 (Breeze, Reverb, Vue, PeerJs, WebRTC)](https://www.binaryboxtuts.com/php-tutorials/laravel-tutorials/building-a-video-chat-app-using-laravel-11-breeze-reverb-vue-peerjs-webrtc/)


---

*Note: This README provides a concise overview of the project setup and usage. For comprehensive instructions and code examples, please refer to the original tutorial linked above.*