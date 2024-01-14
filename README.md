# csound_plugins

This repository is a facility to build my plugin opcodes for Csound all at once. 
It contains : 
- [hypercurve](https://github.com/johannphilippe/hypercurve) - piecewise curve editing library
- [lua_csound](https://github.com/johannphilippe/lua_csound) - lua opcodes for Csound 
- [rawmidi_csound](https://github.com/johannphilippe/rawmidi_csound) - a flexible set of MIDI opcodes using RtMidi 


# Build 


```bash
git clone https://github.com/johannphilippe/csound_plugins.git  --recurse-submodules
cd csound_plugins
mkdir build && cd build 
cmake ..
make
```

You might disable some plugin build by using cmake options : 
- `-DBUILD_LUA_CSOUND=OFF`
- `-DBUILD_HYPERCURVE=OFF`
- `-DBUILD_RAWMIDI=OFF`
