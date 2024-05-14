import json

# Define your favorite series/movies with additional info
favorites = {
    "Terminator": {
        "ranking": 1,
        "description": "A sci-fi action film series created by James Cameron.",
        "image_url": "https://example.com/terminator.jpg"
    },
    "Stranger Things": {
        "ranking": 2,
        "description": "A supernatural horror drama created by the Duffer Brothers.",
        "image_url": "https://example.com/stranger_things.jpg"
    },
    "Maze Runner": {
        "ranking": 3,
        "description": "A series of young adult dystopian science fiction novels by James Dashner.",
        "image_url": "https://example.com/maze_runner.jpg"
    },
    "Boyka": {
        "ranking": 4,
        "description": "A series of martial arts action films starring Scott Adkins as Yuri Boyka.",
        "image_url": "https://example.com/boyka.jpg"
    },
    "Rocky": {
        "ranking": 5,
        "description": "A boxing film series starring Sylvester Stallone as the character Rocky Balboa.",
        "image_url": "https://example.com/rocky.jpg"
    }
}

# Sort favorites by ranking
sorted_favorites = sorted(favorites.items(), key=lambda x: x[1]['ranking'])

# Convert to JSON
favorites_json = json.dumps(sorted_favorites, indent=4)

# Write JSON to a file
with open('favorite_series_movies.json', 'w') as file:
    file.write(favorites_json)

print("Favorites list has been created and saved as 'favorite_series_movies.json'.")
