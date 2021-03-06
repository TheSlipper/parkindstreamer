# ParkindStreamer

## Description

ParkindStreamer is a command-line tool for streaming camera feed and communicating with an instance of a Parkind server. The only dependency required for this tool isOpenCV 4.5.0. It works on Linux, MacOS and Windows 10 and any other operating system on which you can compile golang and OpenCV. 

## Installation

This repository contains a set of builds for amd64 architecture on multiple operating systems. You can find them in the [release section](https://github.com/TheSlipper/Parkind/releases) of this repository. As for the builds which you can't find in there you need to compile them on your own.

## Compiling from source

**1. Install OpenCV 4.5.0.** 

On macOS you can just use brew and install it like so:
```
brew install opencv
```
On ubuntu it is suggested to compile it from source. You can find instructions for ubuntu [here](https://www.samontab.com/web/2020/11/installing-opencv-4-5-0-in-ubuntu-20-04-lts/).

**2. Install the below build dependencies:**
```
go get -u -d gocv.io/x/gocv@v0.25.0
go get -u github.com/google/uuid@v1.1.2
```

**3. Clone this repository and navigate to the ParkindStreamer directory**
```
git clone https://github.com/TheSlipper/ParkindStreamer.git
cd ParkindStreamer/
go build
```

**4. ParkindStreamer is compiled. You can run it like so:**
```
LOGIN=your_parkind_login PASSWORD=your_password ./ParkindStreamer -verbose
```
