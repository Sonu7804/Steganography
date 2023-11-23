# Steganographyx

What is steganography?
Steganography is the technique of hiding data within an ordinary, nonsecret file or message to avoid detection; the hidden data is then extracted at its destination. Steganography use can be combined with encryption as an extra step for hiding or protecting data. The word steganography is derived from the Greek word steganos, meaning "hidden or covered," and the Greek root graph, meaning "to write."

Steganography can be used to conceal almost any type of digital content, including text, image, video or audio content. The secret data can be hidden inside almost any other type of digital content. The content to be concealed through steganography -- called hidden text -- is often encrypted before being incorporated into the innocuous-seeming cover text file or data stream. If not encrypted, the hidden text is commonly processed in some method to increase the difficulty of detecting the secret content.

# Overview
The steganography program provided is a Python application that facilitates hiding and extracting secret messages in various media, including images and wave audio files. The program utilizes cryptographic techniques to encode and decode messages securely.

# Libraries
Ensure you have the following Python libraries installed to run the program:

# PIL (Pillow): Used for image processing and displaying a logo in the GUI.
```
pip install Pillow
```

# Crypto.Cipher (PyCryptoDome): Provides cryptographic algorithms for secure message encoding and decoding.
```
pip install pycryptodome
```

# NumPy: Purpose: Required for numerical operations, especially in the image steganography program.
pip install numpy

# PyAudio: Purpose: Required for wave audio steganography programs to work with audio files.
```
pip install pyaudio
```

# 1. Image Steganography
class Encode
Purpose: Handles encoding (hiding) secret messages within images.
Methods:
__init__(image_path, password, text_to_encode): Initializes the Encode object with the image path, password, and text to be encoded.
is_password_valid(): Checks if the supplied password is valid.
is_text_valid(): Checks if the supplied text to be encoded is valid.
is_image_path_valid(): Checks if the supplied image path is valid and the image file exists.
get_text_binary(): Generates the binary equivalent of the text to be encoded.
encode_into_image(): Hides/encodes the binary data into the image using LSB modification.
are_values_valid(): Validates the password, image path, and text before encoding.
class Decode
Purpose: Handles decoding (extracting) secret messages from images.
Methods:
__init__(image_path, password): Initializes the Decode object with the image path and password.
is_password_valid(): Checks if the supplied password is valid.
is_image_path_valid(): Checks if the supplied image path is valid and the image file exists.
get_decoded_text(bytes_string): Decrypts the extracted bytes string to obtain the original text.
decode_from_image(): Extracts the encoded binary data from the image.
are_values_valid(): Validates the password and image path before decoding.

# 2. Wave Audio Steganography
class ExtractWaveGUI
Purpose: Provides a GUI for extracting hidden messages from wave audio files.
Methods:
__init__(root): Initializes the GUI window and sets up the necessary components.
create_widgets(): Creates the GUI components, including labels, entry widgets, and buttons.
browse_audio(): Opens a file dialog for selecting a wave audio file.
extract_message(): Extracts and displays the hidden message from the selected wave audio file.
class HiddenWaveGUI
Purpose: Provides a GUI for hiding messages in wave audio files.
Methods:
__init__(root): Initializes the GUI window and sets up the necessary components.
create_widgets(): Creates the GUI components, including labels, entry widgets, and buttons.
display_logo(): Displays a logo image in the GUI.
browse_audio(): Opens a file dialog for selecting a wave audio file.
browse_output(): Opens a file dialog for selecting the output path and filename.
hide_message(): Hides the entered message in the selected wave audio file and saves the result.

# How to Run
Ensure the required libraries are installed (Pillow, pycryptodome, Numpy, Tkinter, Wave).
Run the respective scripts for image steganography (encryptstego.py) or wave audio steganography (encode_audio.py and decode_audio.py).
Follow the GUI instructions to select input files, enter messages, and perform encoding or decoding.

# Notes
Image steganography modifies the least significant bit (LSB) of each pixel's channels to hide the message.
Wave audio steganography modifies the LSB of each audio frame to hide the message.
The length of the message affects the number of frames modified in wave audio steganography.
Feel free to reach out if you have any questions or need further assistance!





# Licence 
Copyright 2023 Sonu Kushwaha

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

https://github.com/Sonu7804/Steganography

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Copyright 2023 [SONU KUSHWAHA](https://github.com/Sonu7804/Steganography)
