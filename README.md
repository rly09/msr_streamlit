# 🎬 Movie Recommender System

<div align="center">
  <p><strong>An intelligent movie recommendation engine powered by content-based filtering and Streamlit</strong></p>
  <p>
    <img src="https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python" alt="Python">
    <img src="https://img.shields.io/badge/Streamlit-1.0+-red?style=flat-square&logo=streamlit" alt="Streamlit">
    <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">
  </p>
</div>

---

## 📖 Overview

This project is a **Movie Recommender System** built with Streamlit that leverages content-based collaborative filtering to suggest movies based on user selection. The system uses similarity metrics to find movies with comparable characteristics and displays movie posters fetched from The Movie Database (TMDb) API.

## ✨ Features

- 🎯 **Smart Recommendations**: Get personalized movie suggestions based on your selected movie
- 🖼️ **Beautiful UI**: Clean and intuitive Streamlit interface with movie poster displays
- ⚡ **Fast Performance**: Optimized with caching for rapid response times
- 🎭 **Rich Movie Data**: Access to a comprehensive movie database with metadata
- 🌐 **Poster Integration**: Real-time poster fetching from TMDb API
- 💨 **Error Handling**: Graceful handling of API failures with fallback images

## 🛠️ Tech Stack

- **Python 3.8+** - Core programming language
- **Streamlit** - Web application framework
- **Pandas** - Data manipulation and analysis
- **Scikit-learn** - Machine learning and similarity computation
- **Requests** - HTTP library for API calls
- **Pickle** - Data serialization
- **TMDb API** - Movie database and poster source

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package manager)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/rly09/msr_streamlit.git
   cd msr_streamlit
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\\Scripts\\activate
   ```

3. **Install dependencies**
   ```bash
   pip install streamlit pandas requests
   ```

## 📂 Project Structure

```
msr_streamlit/
├── app.py                 # Main Streamlit application
├── movies.pkl             # Pickled movie dataframe
├── movies_dict.pkl        # Pickled movies dictionary
├── similarity.pkl         # Pre-computed similarity matrix
├── .gitignore            # Git ignore file
└── README.md             # This file
```

## 🎮 Usage

1. **Start the Streamlit application**
   ```bash
   streamlit run app.py
   ```

2. **Open your browser** and navigate to `http://localhost:8501`

3. **Select a movie** from the dropdown menu

4. **Click the "Recommend" button** to get personalized recommendations

5. **View the results** with movie titles and posters displayed side-by-side

## 🔧 How It Works

### Algorithm

The system uses **content-based filtering** with cosine similarity:

1. **Data Preparation**: Movie data is preprocessed and stored in pickle format
2. **Similarity Computation**: A pre-computed similarity matrix stores cosine similarity scores between all movies
3. **Recommendation Generation**: When a movie is selected, the system finds the top 5 most similar movies
4. **Poster Fetching**: Movie posters are fetched dynamically from TMDb API
5. **Display**: Results are presented in a visually appealing grid layout

### Key Functions

- `fetch_poster(movie_id)`: Retrieves movie poster from TMDb API
- `recommend(movie)`: Generates top 5 movie recommendations

## 🔑 API Configuration

The application uses The Movie Database (TMDb) API. The API key is already configured in the code. For production use, consider:

- Using environment variables to store sensitive API keys
- Implementing rate limiting
- Adding error handling for API quota exceeded scenarios

## 📊 Data Files

- **movies_dict.pkl**: Dictionary containing movie information
- **movies.pkl**: Pandas DataFrame with movie data
- **similarity.pkl**: Pre-computed cosine similarity matrix (shape: n_movies × n_movies)

## 🎯 Future Enhancements

- [ ] User ratings and feedback system
- [ ] Collaborative filtering integration
- [ ] Advanced filtering options (genre, year, rating)
- [ ] Recommendation history tracking
- [ ] Multi-language support
- [ ] Dark mode theme
- [ ] Movie details modal with reviews
- [ ] Export recommendations as list

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**rly09** - [GitHub Profile](https://github.com/rly09)

## 🙏 Acknowledgments

- [Streamlit](https://streamlit.io/) for the amazing web framework
- [The Movie Database (TMDb)](https://www.themoviedb.org/) for the movie data and API
- [Scikit-learn](https://scikit-learn.org/) for machine learning utilities

## ⚠️ Disclaimer

This project is for educational purposes. Movie data and posters are fetched from TMDb API. Please respect their terms of service and usage policies.

---

<div align="center">
  <p><strong>Made with ❤️ by rly09</strong></p>
  <p>If you find this project helpful, please consider giving it a ⭐ on GitHub!</p>
</div>
