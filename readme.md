# Autoencoding Edward Hopper:<br>Using deep learning to recommend art
Larry Finer  
March 2019

The goal of this project was to build a model that would take an image of an artwork and compare it visually to a corpus of more than 100,000 artworks from museums and other sources in order to find works that are similar visually. The main steps in the project were:

1. Download artwork images and metadata from multiple sites  
   1a. Artspace  
   1b. [Guggenheim]('./1b. Download Guggenheim images and metadata.ipynb')  
   1c. MoMA  
   1d. National Gallery of Art  
   1e. Tate  
   1f. Whitney  
   
2. [Combine metadata into a single pandas dataframe](2. Combine metadata into dataframe.ipynb)  
3. [Develop a convolutional neural network autoencoder model that adequately reproduces the images](3. Create autoencoder model.ipynb)
4. [Extract the narrowest encoded layer and use it to encode the entire corpus as well as a test image; then compare the test image to the entire corpus using a cosine distance measure to find the nearest images](4. Encode corpus and compare test image.ipynb)

Each of the links above is a Jupyter Notebook file with Python code to complete each step.

Also contained in this repository:

- [Presentation summarizing the results of the project in Keynote format](Autoencoding Hopper.key)
- [Presentation in PDF](Autoencoding Hopper.pdf)

Finally, the following code was used to develop a Flask web app:

- [Flask app code in Python](similart.py)
- [Home page of the web app](index.html)
- [Results page of the web app](results.html)