# Emotion-Driven Playlist Generator 🎵😊

Welcome to the **Emotion-Driven Playlist Generator**! This project uses **facial emotion detection** or **text-based sentiment analysis** to create personalized Spotify playlists based on your current mood. Whether you're happy, sad, angry, or calm, this app will curate a playlist that matches your emotions.

---

## **Features**
- **Facial Emotion Detection**: Uses a pre-trained deep learning model to detect your emotion from your webcam feed.
- **Text-Based Emotion Input**: Allows you to manually describe your mood, and the app will analyze it using sentiment analysis.
- **Spotify Integration**: Fetches songs from Spotify and creates a playlist tailored to your emotion.
- **User-Friendly GUI**: Built with `tkinter` for a seamless and intuitive user experience.

---

## **How It Works**
1. **Emotion Detection**:
   - The app detects your emotion using either:
     - **Facial Expression Analysis**: Captures your face via webcam and predicts your emotion using a pre-trained deep learning model.
     - **Text Input**: Analyzes your mood description using sentiment analysis (e.g., "I feel happy today").
2. **Playlist Generation**:
   - Based on the detected emotion, the app fetches songs from Spotify using the Spotify API.
   - Songs are selected based on audio features like **valence** and **energy**, which correlate with emotions.
3. **Playlist Creation**:
   - The app creates a new playlist in your Spotify account and adds the selected songs to it.
   - You receive a link to the playlist, ready to play!

---

## **Technologies Used**
- **Python**: The core programming language.
- **OpenCV**: For facial detection and webcam feed processing.
- **Keras/TensorFlow**: For loading and using the pre-trained emotion detection model.
- **Spotipy**: A Python library for interacting with the Spotify API.
- **TextBlob**: For sentiment analysis of text input.
- **Tkinter**: For building the graphical user interface (GUI).

---

# **Installation Guide**

Follow these steps to set up the project on your local machine:

## **1. Clone the Repository**

First, clone the repository to your local machine using the following command:

```bash
git clone https://github.com/your-username/emotion-playlist-generator.git
cd emotion-playlist-generator
```

## **2. Install Dependencies**

Install the required Python libraries using pip. Run the following command in your terminal:

```bash
pip install opencv-python keras tensorflow spotipy textblob
```

## **3. Set Up Spotify API**

To interact with Spotify, you need to set up the Spotify API:

1. Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard) and log in with your Spotify account.
2. Click on **Create an App** and fill in the required details (e.g., app name and description).
3. Once the app is created, note down your **Client ID** and **Client Secret**.
4. In the app settings, add the following Redirect URI:

```
http://localhost:8888/callback
```

This is required for Spotify's authentication process.

## **4. Configure the Script**

Open the script file (`emotion_playlist_generator_gui.py`) and replace the following placeholders with your Spotify API credentials:

```python
SPOTIPY_CLIENT_ID = 'your_client_id'  # Replace with your Client ID
SPOTIPY_CLIENT_SECRET = 'your_client_secret'  # Replace with your Client Secret
SPOTIPY_REDIRECT_URI = 'http://localhost:8888/callback'  # Must match the Redirect URI in Spotify Dashboard
```

## **5. Run the Application**

Once everything is set up, run the script using the following command:

```bash
python emotion_playlist_generator_gui.py
```

## **6. Grant Access to Spotify**

When you run the script for the first time:

- A browser window will open, asking you to log in to your Spotify account.
- After logging in, you will be redirected to the Redirect URI (`http://localhost:8888/callback`).
- Copy the URL from the browser's address bar and paste it into the terminal give it to me in a way that i can just copy and paste it there

