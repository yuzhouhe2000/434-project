# EE434 Project Updating 

Team: Michael Pozzi, Matt Baseheart, Yuzhou He

requirements.txt may not be complete, pip3 install the missing ones

Currently, denoiser live uses soundflower as the default loopback device. Need to change input/output from code.

Reference: https://github.com/facebookresearch/denoiser


****

TODO: 

- [X] Template for flask app + a basic denoiser model

- [x] Face and mouth detection

- [x] Voice Activity Detection using voice

- [ ] Adjust sound volume (mono/bi channel) by speaker position

- [ ] Add extra denoising function using filters

- [ ] Voice activity detection from mouth movement

- [ ] Depth sensing using eye separation

- [ ] Allow the project to be ran on Jetson with Gstreamer

****

To run the flask server (linux/mac):

    pip3 install -r requirements.txt

    download "denoiser.th" and "shape_predictor_68_face_landmarks.dat" from drive

    move "denoiser.th" to env/denoiser/

    move "shape_predictor_68_face_landmarks.dat" to env/camera/

    cd env

    flask run

    open site in chrome


if dlib fails to install, try to install from source:

    git clone https://github.com/davisking/dlib.git

    cd dlib

    mkdir build; cd build; cmake ..; cmake --build .

    cd ..

    python3 setup.py install

    (if assert error happens, delete the lines with the assert(false) statement in the error files)




