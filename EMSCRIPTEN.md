# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS=mid -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@../../../../funcs.txt -sINITIAL_MEMORY=96mb -sENVIRONMENT=web --preload-file HUNTBGIN.RTC --preload-file HUNTBGIN.RTL --preload-file HUNTBGIN.WAD --preload-file REMOTE1.RTS --preload-file dgguspat/ --preload-file timidity.cfg --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
