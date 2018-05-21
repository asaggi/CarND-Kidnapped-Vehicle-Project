# CarND-Kidnapped-Vehicle-Project
This repository contains implementation of [CarND-Kidnapped-Vehicle-Project](https://github.com/asaggi/CarND-Kidnapped-Vehicle-Project/blob/master/src/particle_filter.h)
 

## Running the Code

This repository includes two files that can be used to set up and intall uWebSocketIO for either Linux or Mac systems. For windows you can use either Docker, VMware, or even Windows 10 Bash on Ubuntu to install uWebSocketIO.

Once the install for uWebSocketIO is complete, the main program can be built and ran by doing the following from the project top directory.

1. mkdir build
2. cd build
3. cmake ..
4. make
5. ./particle_filter

Alternatively some scripts have been included to streamline this process, these can be leveraged by executing the following in the top directory of the project:

1. ./clean.sh
2. ./build.sh
3. ./run.sh

Tips for setting up your environment can be found [here](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/0949fca6-b379-42af-a919-ee50aa304e6a/lessons/f758c44c-5e40-4e01-93b5-1a82aa4e044f/concepts/23d376c7-0195-4276-bdf0-e02f1f3c665d)

I modified these 2 files for this project: are src/particle_filter.cpp, and particle_filter.h
and ran the code until I got - `Success! Your particle filter passed!`


# Implementing the Particle Filter

The `Particle Filter` is implemented in `src/particle_filter.cpp`:

`Initialization:` Particle initialization is implemented at ParticleFilter::init from line 24 to line 62.

`Prediction:` The prediction step is implemented at ParticleFilter::prediction from line 64 to line 100.

`Weight's update:` This is the more important operation in my opinion. It is implemented at ParticleFilter::updateWeights from line 138 to line 217.

Almost the rest of the magic happens on src/main.cpp. The event handler declared at line 49 parse the received message and call the above described Particle Filter methods.
 

#### The Map*
`map_data.txt` includes the position of landmarks (in meters) on an arbitrary Cartesian coordinate system. Each row has three columns
1. x position
2. y position
3. landmark id





