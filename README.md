# Whisper API Server

This project sets up a simple Flask server to provide an API for transcribing audio files using OpenAI's Whisper model. It allows users to upload audio files through an API endpoint, which are then processed by Whisper to return transcriptions.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6 or higher
- Pip (Python package manager)
- FFmpeg (for audio processing)

## Installation

To install the necessary dependencies for this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/sauravpanda/whisper-service.git
   cd whisper-api-server
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

   This will install Flask and Whisper.

3. Make sure `ffmpeg` is installed on your system:
   - For Ubuntu/Debian: `sudo apt-get install ffmpeg`
   - For Fedora: `sudo dnf install ffmpeg`
   - For macOS (with Homebrew): `brew install ffmpeg`
   - For Windows, download and install from [FFmpeg's official site](https://ffmpeg.org/download.html).

## Running the Server

To run the server, execute:

```bash
python app.py
```

This will start the Flask server on `http://localhost:5000`.

## Usage

To transcribe an audio file, send a POST request to the `/transcribe` endpoint with the audio file. For example, using `curl`:

```bash
curl -X POST -F 'file=@sounds/southpark-the-coon.mp3' http://localhost:5000/transcribe
```

Replace `sounds/southpark-the-coon.mp3` with the path to your audio file.

## Contributing

Contributions to this project are welcome. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any questions or feedback, please contact me at [saurav.panda@cloudcode.ai].
