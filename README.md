# Pix.ly - Image Editor Coding Project

## Description

Pix.ly is a `Flask BackEnd` application with Server Side Rendering. Images uploaded are re-sized for server handling and loaded into a cloud-based `AWS s3 bucket`, EXIF metadata is stripped and included as part of the image's database record. Utilizing the `Python Pillow library`, Pix.ly allows users to manipulate images: current functions include filter, sketchify, and border. Pix.ly has `PSQL full-text search` capabilities which allows handling of natural language searches vs. limited text queries.


<img width="45%" alt="pixly_editor_before" src="https://user-images.githubusercontent.com/72634901/174491113-771c204b-6467-4c91-9fde-a0f1060b2971.png">

<img width="45%" alt="pixly_editor_after" src="https://user-images.githubusercontent.com/72634901/174491119-9c0c14db-d3e9-4aec-ac71-58d09f38c6b8.png">


## DEMO

[DEMO](https://al-pixly.herokuapp.com/): Edit and/or upload your own images. 

## Getting Started

### Installing Dependencies

```
python3 -m venv venv
```
```
source venv/bin/activate
```
```
pip3 install -r requirements.txt
```

### Running the app

To run the app, first run the `seed.py` file directly to create the database tables:

```
$ python3 seed.py
```

You only need to do this once, unless you change your model definitions.

Then run the app itself:

```
$ flask run -p 5001
```

Visit [http://localhost:5001/](http://localhost:5001/) in your browser to see the results.
`
## Future
1. Testing
2. Add a route/page for users to download their edited image.
3. Expand on PSQL full-text search with image recognition library to create image descriptions.
4. Add a delete image option.
5. Expanding image editing functions.


## Acknowledgments

Inspiration, code snippets, etc.
* [Strip EXIF Metadata](https://medium.com/nerd-for-tech/script-to-extract-image-metadata-using-python-and-pillow-library-53a6ae56ccc3)
* [Pillow: Re-Size](https://www.tutorialspoint.com/python_pillow/python_pillow_resizing_an_image.htm)
* [Pillow: Convert Sepia](https://www.codementor.io/@isaib.cicourel/intermediate-image-filters-mj6y7abx4)
* [Pillow: Sketchify](https://www.tutorialspoint.com/python_pillow/python_pillow_adding_filters_to_an_image.htm)
* [Pillow: Border](https://www.blog.pythonlibrary.org/2017/10/26/how-to-add-a-border-to-your-photos-with-python/)
