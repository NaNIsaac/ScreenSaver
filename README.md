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
- `src/Kim/`, `src/Lee/`, `src/Yong/` - one scene per contributor (see License for who holds the rights)

## Build from the command line

Rebuilt on 2026-10-23 without source changes against openFrameworks 0.11.2
(`of_v0.11.2_vs2017_release`, the last 0.11 release; picked because the solution is in Visual Studio 15
format with toolset v142 and uses `ofSetupOpenGL`). With the repository at
`<openFrameworks>\apps\myApps\ScreenSaver`, MSBuild from the Visual Studio 2022 Build Tools (MSVC 14.44)
and the toolset overridden to v143, the openFrameworks library and the project built in 37 s with 0 errors
and 512 warnings:

```
MSBuild ScreenSaver.sln -p:Configuration=Debug -p:Platform=x64 -p:PlatformToolset=v143 -m:4
bin\ScreenSaver_debug.exe
```

openFrameworks and its prebuilt third-party DLLs are copied into `bin\` by the build. The window is
1024x768. Other openFrameworks versions were not tried.

## Contributors and origin

Three people made this in 2023, one scene each:

- `src/Kim` - [kimnoa](https://github.com/kimnoa)
- `src/Lee` - [culee1999](https://github.com/culee1999)
- `src/Yong` - [NaNIsaac](https://github.com/NaNIsaac)

Every commit on `main` was made by NaNIsaac; the one commit by `culee1999`, "수정 버전" (a revised version of the
project), is the only commit on the branch `rev_branch`, which has no common history with `main` and was kept as
it was.

## License

The code written by NaNIsaac is under the [MIT License](LICENSE): `src/Yong/`, `src/main.cpp`,
`src/ofApp.*` and the Visual Studio project files (all other files were committed by NaNIsaac as well).

`src/Kim/` and `src/Lee/` are scenes written by the two other contributors, who keep their rights. No
license from them is recorded in this repository, so the MIT License above is NaNIsaac's grant for NaNIsaac's own
files only and does not extend to those two folders. They stay here with their authors credited, as
they were published.

openFrameworks (MIT) is not part of this repository; it is installed separately (see Requirements).
