# Pokémon Images Downloader

This script allows you to download Pokémon images using the Google Custom Search API. The images can be used as a training set for deep learning models, such as convolutional neural networks (CNNs).
## Requirements

To run this script, you will need the following Python libraries:

    google_images_search
    google-auth
    google-auth-oauthlib
    google-auth-httplib2
    google-api-python-client
    Pillow
    requests
    imagehash

You can install them using the following command:

    pip install google_images_search google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client Pillow requests imagehash

## Usage

To use the script, first update the following variables in the code:

    API_KEY: Replace with your Google Custom Search API key.
    CX: Replace with your Custom Search JSON API search engine ID.

Then, run the script using the following command:

python pokemon_images_downloader.py

This script will download images of Pokémon and save them in the pokemon_images directory. Each Pokémon will have a separate folder, containing up to 10 images.

The images are filtered to reduce duplicates and unrelated images by adjusting the search query and using image hashing.
## Known Issues and Limitations

    The Google Custom Search API has a daily quota limit, which might cause HTTP Error 429 if exceeded. To resolve this, either wait for the quota to reset or request an increase in your quota limits. You can also create another Google API key with a separate project and use that key as a temporary solution.
    The script uses a combination of search terms and filters to improve the accuracy of the image results, but there is no guarantee that all images will be relevant or unique.
    The image hashing method used to reduce duplicates might lead to a smaller number of images than specified in the max_images parameter if many images are similar.

## Future Improvements

    Enhance the filtering of images using machine learning techniques, such as similarity detection or image classification.
    Add support for parallel or asynchronous downloading to speed up the image downloading process.
    Enable the use of other image search APIs as alternative sources of images.
