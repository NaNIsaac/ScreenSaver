# ScreenSaver

A set of small particle and animation sketches written in C++ with openFrameworks.

Hobby project from 2023, made together with two other contributors. Each person wrote one
scene (`src/Kim`, `src/Lee`, `src/Yong`); `ofApp.cpp` switches between them.

## Requirements

- Windows, Visual Studio 2019 or later (toolset v142)
- openFrameworks for Visual Studio

## Run

The project file uses relative paths into an openFrameworks install, so the repository has to sit
in `<openFrameworks>/apps/myApps/ScreenSaver`.

1. Clone it into `<openFrameworks>/apps/myApps/`.
2. Open `ScreenSaver.sln`, select `Debug` / `x64` and run (F5).

## Controls

- Left / Right arrow: previous / next scene (cycles Kim, Lee, Yong, then Lee again)
- In the first scene: drag the mouse to emit particles, click to change their color

## Structure

- `src/main.cpp`, `src/ofApp.*` - window setup and scene switching
- `src/Kim/`, `src/Lee/`, `src/Yong/` - one scene per contributor
