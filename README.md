# Keyboard DJ Set

## Team Members:
- Manas Gandhi
- Jack Prokop
- Milind Sagaram

## Problem
DJ boards have become the “hot topic” of today’s music industry, with the tool giving way to many of the greatest artists of our generation, including *John Summit* and *Twinsick*. While we have seen many great EDM artists shine due to the traditional DJ set, it has some drawbacks as well - namely the lack of portability, ease of use for new users, and high prices. 

## Solution
To address these challenges, we propose the DJ keyboard, a DJ board that simply uses the keys on an external keyboard, connected to a computer. This makes use of a microcontroller on a PCB for processing the inputs of the keyboard and converting that into commands for the software. We also will create software for the songs and audio processing, as well as the speaker technology. This approach simplifies the complicated DJ board, reduces the cost and size of getting a DJ board, and makes it easy to take anywhere, making the DJ experience for everyone much easier.

The specific DJ board elements we want to incorporate are volume control, tempo control, music slicing and looping, song skipping functionality, and if we have time, auto-crossfade capabilities

## Solution Components
### 1. Keyboard
This subsystem w inputs that our system will be receiving.

- **Inputs**: keyboard should take inputs for all keys on the keyboard, and maybe combinations of keys (if we have time).

### 2. Microcontroller
This subsystem is the core of the whole system, providing the communication between the input (keyboard) and the software.

- **Communication between keyboard and software:** this will be our communication system between the input and the output.
- **Power:** Will be used to power the keyboard.

### 3. Volume Control
This subsystem is where we control the volume using the PCB.

- **Volume controller:** We will use a potentiometer (which we might connect to a slider) to increase and decrease the volume (increased resistance = lower volume).
- **Speaker:** We will put two small speakers on the PCB, and connect to output of the potentiometer to the input of the speaker.

### 4. Tempo Control
This subsystem is where we control the tempo of the song (in BPM) that is currently playing.

- **Tempo controller:** We will use a potentiometer (which we might connect to a slider) to send a signal to the microcontroller to increase or decrease the tempo.

### 5. Skip song
This subsystem is where we skip the song that is currently playing, allowing us to switch to the next song.

- **Skip button:** We will use a button that sends a signal to the microcontroller to skip the current song and go to the queued up song.

### 5. Power
This subsystem where the power is supplied to the system, including the microcontroller and speakers.

- **Rechargeable Battery:** We will have a rechargeable battery on our PCB that will supply the power to the rest of the system, including the microcontroller and all other hardware components.

### 6. Software
This subsystem where the control and processing of the system happens. The inputs should be processed into some functionality based on a DJ board here.

- **Input processing:** Inputs will be processed and translated into functions here.
- **Communication with Keyboard:** embedded software will be written to communicate with the microcontroller through a USB using SPI.
- **Audio processing:** audio processing will occur here, where the audio files will be processed and manipulated based on the inputs of the keyboard.
  - Will have to incorporate signal processing libraries.

### 7. Laptop
This subsystem will be used for all the components we cannot buy, specifically for a hard drive.

- **Hard drive:** hard drive is just for storage purposes, real DJ boards have hard drives that they plug into the boards typically.

## Criterion for Success
- **Ability to read inputs:** the microcontroller should be able to read inputs from the keyboard and send that to the software to be processed.
- **Ability of software to process inputs:** the software should be able to take the inputs from the keyboard through the microcontroller and translate them into functions that represent manipulations of the audio files.
- **Ability to manipulate the audio files:** the software’s functions should be able to manipulate the audio files based on the keyboard inputs in real time without pausing the play of the music.
- **Ability of system to have music on the “hard drive”:** the music should be stored as audio files on the “hard drive” (in our case we will just use the laptop file system).
- **Ability to play selected music through speaker:** the system should play the selected music through the speaker without fail whilst taking input from the keyboard.
