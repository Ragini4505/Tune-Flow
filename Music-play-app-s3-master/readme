# 🎵 MusicHub - Music Streaming App with AWS S3

A modern web-based music streaming application with AWS S3 integration for cloud storage. Stream, upload, and manage your music collection with a beautiful, responsive interface.

## ✨ Features

- 🎶 **Music Streaming**: Play songs directly in the browser
- ☁️ **Cloud Storage**: AWS S3 integration for reliable file storage
- 🎨 **Modern UI**: Clean, responsive design with music player controls
- 📱 **Mobile Friendly**: Works seamlessly on desktop and mobile devices
- 🔧 **Admin Panel**: Upload and manage songs with ease
- 🎯 **Category Filters**: Organize music by genres (Pop, Rock, Jazz, Classical, Hip Hop)
- 📊 **Analytics**: Track plays and downloads
- ⬇️ **Download Support**: Download songs for offline listening

## 🏗️ Project Structure

```
Music-play-app-s3/
├── backend/
│   ├── package.json          # Node.js dependencies
│   ├── server.js             # Express server with S3 integration
│   ├── setup-s3-bucket.js    # S3 bucket configuration script
│   └── uploads/              # Local file storage (fallback)
│       ├── audio/            # Audio files
│       └── images/           # Cover images
├── frontend/
│   ├── index.html           # Main music player interface
│   ├── admin.html           # Admin panel for uploads
│   ├── script.js            # Main frontend logic
│   ├── admin.js             # Admin panel logic
│   └── styles.css           # Application styles
└── README.md               # This file
```

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- AWS Account with S3 access
- AWS CLI configured (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/amitcodee/Music-play-app-s3.git
   cd Music-play-app-s3
   ```

2. **Install dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Environment Setup**
   
   Create a `.env` file in the `backend` directory:
   ```env
   AWS_REGION=your-aws-region
   AWS_ACCESS_KEY_ID=your-access-key-id
   AWS_SECRET_ACCESS_KEY=your-secret-access-key
   S3_BUCKET_NAME=your-s3-bucket-name
   PORT=3000
   ```

4. **AWS S3 Setup**
   
   Run the S3 bucket setup script to configure proper permissions:
   ```bash
   node setup-s3-bucket.js
   ```

5. **Start the application**
   ```bash
   npm start
   # or for development with auto-reload
   npm run dev
   ```

6. **Access the application**
   - Main App: http://localhost:3000
   - Admin Panel: http://localhost:3000/admin.html

## 🔧 Configuration

### AWS S3 Setup

1. **Create an S3 Bucket**
   - Log into AWS Console
   - Create a new S3 bucket
   - Note the bucket name and region

2. **IAM User Setup**
   - Create an IAM user with S3 permissions
   - Attach the following policy:
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Effect": "Allow",
         "Action": [
           "s3:GetObject",
           "s3:PutObject",
           "s3:DeleteObject",
           "s3:ListBucket"
         ],
         "Resource": [
           "arn:aws:s3:::your-bucket-name",
           "arn:aws:s3:::your-bucket-name/*"
         ]
       }
     ]
   }
   ```

3. **Bucket Policy (Auto-configured by setup script)**
   The `setup-s3-bucket.js` script automatically configures your bucket for public read access.

## 📖 Usage

### For Users
1. Visit the main page to browse and play music
2. Use category filters to find specific genres
3. Click on any song to start playing
4. Use the built-in audio player controls
5. Download songs using the download button

### For Administrators
1. Access the admin panel at `/admin.html`
2. Upload new songs with cover images
3. Specify song details (title, artist, genre)
4. View upload statistics and analytics

## 🛠️ API Endpoints

- `GET /` - Serve main application
- `GET /songs` - Get all songs
- `POST /upload` - Upload new song (multipart/form-data)
- `DELETE /songs/:id` - Delete a song
- `GET /stats` - Get application statistics
- `POST /songs/:id/play` - Track song play
- `POST /songs/:id/download` - Track song download

## 🎯 Technologies Used

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **AWS SDK v3** - S3 integration
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing
- **UUID** - Unique identifier generation

### Frontend
- **HTML5** - Structure and audio support
- **CSS3** - Modern styling and animations
- **Vanilla JavaScript** - Interactive functionality
- **Font Awesome** - Icons

### Cloud Services
- **AWS S3** - File storage and delivery
- **AWS IAM** - Access management

## 🔒 Security Features

- CORS configuration for secure cross-origin requests
- File type validation for uploads
- File size limits (10MB max)
- AWS IAM-based access control
- Public read-only access for audio files

## 🐛 Troubleshooting

### Common Issues

1. **AWS Credentials Error**
   - Ensure `.env` file has correct AWS credentials
   - Verify IAM user has S3 permissions

2. **Upload Fails**
   - Check file size (max 10MB)
   - Ensure both audio and image files are selected
   - Verify S3 bucket permissions

3. **Songs Don't Play**
   - Ensure S3 bucket has public read access
   - Check browser console for CORS errors
   - Verify audio file format is supported

## 📝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- AWS SDK for seamless S3 integration
- Font Awesome for beautiful icons
- Express.js community for excellent documentation

---

**Happy Listening! 🎵**
