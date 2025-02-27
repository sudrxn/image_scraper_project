# Flask Image Scraper Application  

This Flask application scrapes images from Google Images based on user input, stores them in a local directory, and saves the image data to a MongoDB database.  

## Prerequisites  

Before running the application, ensure you have the following installed:  

- Python 3.x  
- Flask  
- Flask-Cors  
- requests  
- BeautifulSoup (bs4)  
- pymongo  
- MongoDB  

## Installation  

1. **Clone the repository:**  
   ```bash
   git clone https://github.com/your/repository.git
   cd repository
   ```  

2. **Install dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```  

3. **Set up MongoDB:**  
   - Create a MongoDB database named `image_scrap`.  
   - Update the MongoDB connection string in `app.py` (`client = pymongo.MongoClient(...)`).  

## Usage  

1. **Run the Flask application:**  
   ```bash
   python app.py
   ```
   The application will start on `http://0.0.0.0:8000/`.  

2. **Access the Web UI:**  
   - Navigate to `http://127.0.0.1:8000/` in your browser.  
   - Enter a search query and submit the form to fetch images.  

3. **Image Storage:**  
   - Downloaded images are stored in the `images/` directory.  
   - Image data is saved in MongoDB under the `image_scrap_data` collection.  

## Features  

- **Home Page**: Simple UI to enter search queries.  
- **Image Scraping**: Extracts images from Google search results.  
- **Local Storage**: Saves images in a specified directory.  
- **Database Storage**: Stores image data in MongoDB.  
- **Error Handling**: Logs exceptions in `scrapper.log`.  

## File Structure  

```
├── app.py                    # Main Flask application file  
├── templates/                # HTML templates  
│   ├── index.html            # Home page template  
│   └── results.html          # Results page template (if added)  
├── images/                   # Directory for storing downloaded images  
├── scrapper.log              # Log file for debugging  
├── requirements.txt          # List of dependencies  
└── README.md                 # Documentation file (you are here)  
```  

## Contributing  

Contributions are welcome! If you have suggestions, create a pull request.  

## License  

This project is licensed under the MIT License.  
