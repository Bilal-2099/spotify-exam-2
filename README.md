# Spotify Exam 2

## 🚀 Project Overview  
This project (“Spotify Exam 2”) is a Python‑based utility that extracts data from the Spotify API, processes it, and stores it (or prepares it) for further analysis or use in downstream applications.  
It is designed for data engineering practice: extracting, transforming, and preparing music‑/user‑related data from Spotify.

## 🧰 Key Features  
- Connects to Spotify’s API using the `spotipy` library (or equivalent) to fetch data (tracks, artists, playlists).  
- Contains a script (`extract_spotify_data.py`) that handles the data extraction logic.  
- Uses auxiliary files like `Athena.txt`, `Instructions.txt`, and `S3_Full_Access.txt` (presumably for documentation or infrastructure instructions).  
- Includes a ZIP file (`spotipy_layer.zip`) likely designed for AWS Lambda layer usage (for deployment) or similar layer packaging.

## 📁 Folder / File Structure  
```
spotify‑exam‑2/
│  
├── extract_spotify_data.py     # Main extraction script  
├── spotipy_layer.zip           # Compressed package for reusable layer (e.g., Lambda)  
├── Athena.txt                  # Documentation/instructions related to AWS Athena or query work  
├── Instructions.txt            # Setup/run instructions for this project  
├── S3_Full_Access.txt          # Access/infrastructure notes for AWS S3 usage  
└── …
```

## 🔧 Setup & Usage  
Here’s how you can get it running locally:

1. **Clone the repository**  
   ```bash
   git clone https://github.com/Bilal‑2099/spotify‑exam‑2.git
   cd spotify‑exam‑2
   ```

2. **Create & activate a virtual environment**  
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   # or: source venv/bin/activate  # On macOS/Linux
   ```

3. **Install required libraries**  
   ```bash
   pip install -r requirements.txt
   ```
   _Note: If `requirements.txt` is not present, install dependencies manually (e.g., `pip install spotipy boto3` etc.)._

4. **Configure API credentials**  
   - Register your Spotify developer account.  
   - Create an app and get `Client ID` + `Client Secret`.  
   - Set environment variables or update a config file:
     ```bash
     export SPOTIFY_CLIENT_ID=your_client_id
     export SPOTIFY_CLIENT_SECRET=your_client_secret
     ```
     or _on Windows_:
     ```cmd
     set SPOTIFY_CLIENT_ID=your_client_id
     set SPOTIFY_CLIENT_SECRET=your_client_secret
     ```

5. **Run the extraction script**  
   ```bash
   python extract_spotify_data.py
   ```
   This script will connect to Spotify’s API and pull the necessary data based on the logic you’ve defined (e.g., playlists → tracks → artists).

6. **Post‑processing / Storage**  
   After extraction you can:
   - Store the data in a database or data lake (e.g., AWS S3/Athena).  
   - Run analytics or build dashboards.  
   - Reuse the `spotipy_layer.zip` if deploying on AWS Lambda or similar serverless infrastructure.

## 🧭 Why This Project Matters  
- Shows how to **connect to a real‑world web API** (Spotify) and handle authentication, rate limits, pagination etc.  
- Demonstrates a practical **ETL (Extract, Transform, Load)** workflow.  
- Prepares you for data engineering tasks: working with large data sets, cloud services (S3, Athena), packaging dependencies (Lambda layers).  
- Perfect for your portfolio as a data engineering student (you’re at S.M.I.T under Sir Qasim Hassan) showing you can go from API to storage and analytics.

## 👤 Author  
This project was created by **Bilal Raza — Python developer and Data Engineering student at S.M.I.T. under Sir Qasim Hassan.  
GitHub: [Bilal‑2099](https://github.com/Bilal‑2099)**
