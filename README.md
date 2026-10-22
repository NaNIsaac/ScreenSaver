# ScreenSaver

Moved to games-2023/ScreenSaver (https://github.com/NaNIsaac/games-2023/tree/main/ScreenSaver). This repo is no longer maintained.

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

## Build status

Not rebuilt on 2026-10-23: the project needs an openFrameworks tree around it (`ScreenSaver.vcxproj` and
`ScreenSaver.sln` reference `..\..\..\libs\openFrameworksCompiled\project\vs\openframeworksLib.vcxproj`,
and `$(OF_ROOT)`), and none was available on the machine used. The openFrameworks version is not recorded
in the repository. The solution is in Visual Studio 15 format with toolset v142 and uses
`ofSetupOpenGL`, which fits the 0.11.x releases; this is an inference from the project files, not
something that was tried.

## Contributors and origin

Commits come from Isaac Yong and `culee1999` (the first commit, "수정 버전", is on the branch `rev_branch`).
The scenes are named after their authors (`src/Kim`, `src/Lee`, `src/Yong`).

This repository's history was imported into [games-2023](https://github.com/NaNIsaac/games-2023) as
`ScreenSaver/` with `git subtree` (games-2023 commit `28feec7`, from commit `be99f8d` here). Apart from
line endings, the files there are identical to this repository's.
