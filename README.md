# Real-Time Hand Cricket

![Flutter](https://img.shields.io/badge/framework-flutter-blue) ![TensorFlow Lite](https://img.shields.io/badge/framework-TFLite-lightblue) ![Python](https://img.shields.io/badge/python-3.8%2B-yellow) ![VGG16](https://img.shields.io/badge/model-VGG16-orange)

## Overview

Real-Time Hand Cricket is a cross-platform mobile game built with Flutter that lets two players compete live using on-device hand-gesture recognition. It captures real-time images from each player’s camera, classifies ten hand-gesture categories with a VGG16-based CNN fine-tuned via transfer learning on a custom set of 20,000 images, and achieves 99% validation accuracy. A low-latency socket architecture synchronizes game state in real time for seamless multiplayer action.

## Features

- **Live Multiplayer**: Real-time head‑to‑head Hand Cricket matches.
- **Custom Gesture Dataset**: 20,000+ labeled images spanning 10 classes.
- **Transfer Learning**: Fine-tuned VGG16 CNN for 99% validation accuracy.
- **On‑Device Inference**: TensorFlow Lite integration for fast, offline gesture classification.
- **Interactive UI**: Animated scoreboards, intuitive prompts, and error handling in Flutter.

## Prerequisites

- **Flutter SDK**
- **Python 3.8+**
- **TensorFlow & TensorFlow Lite**

## Getting Started

1. **Model Preparation**: Train and fine-tune the VGG16 model on the custom dataset, then export to TensorFlow Lite format.
2. **Server Launch**: Start the real-time socket server to coordinate gameplay between clients.
3. **Client Launch**: Run the Flutter app on Android or iOS devices and connect to the same game room code.
4. **Play**: Show batting or bowling gestures to the camera—predictions update game logic instantly.

## How It Works

1. **Image Capture**: Each client streams camera frames locally.
2. **Gesture Classification**: The TensorFlow Lite model classifies gestures into one of ten classes in real time.
3. **State Sync**: Socket messages relay each player’s move to the opponent’s client.
4. **Game Logic**: Classified gestures translate into runs or wickets, updating the animated scoreboard.

Experience immersive, real-time Hand Cricket with accurate gesture detection and seamless multiplayer gameplay on mobile devices.

