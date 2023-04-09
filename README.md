# libtermkey-cygwin

This a recipe to build and package [libtermkey][1] for [Cygwin][2]. The recipe
is based on the [recipe in cascent's old neovim port][3].

Dependencies:
- [libunibilium{4,-devel}][4]

To build the package install the dependencies and run the following command:
```sh
cygport libtermkey.cygport download prepare compile install package
```

To install the package you can extract it into the root directory:
```sh
eval "$(cygport libtermkey.cygport vars PVR)"
tar -C / -xjvf libtermkey-$PVR.x86_64/dist/libtermkey/libtermkey1/libtermkey1-$PVR.tar.xz
```

[1]: http://www.leonerd.org.uk/code/libtermkey/
[2]: http://www.cygwin.com/
[3]: https://github.com/cascent/neovim-cygwin/blob/09277e3f76981189a2f15d1dbc2f5a4ab4b6c86f/libtermkey/libtermkey.cygport
[4]: https://github.com/kgraefe/unibilium-cygwin
