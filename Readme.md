# wasmIRCpp

wasmIRCpp is a webassembly implementation of the client using the IRC protocol.
It is based on the implementation for [inspIRCdv3](https://github.com/inspircd/inspircd) and uses a simple interface as an example of how to use it.

## Building

To build this project you'll need emscripten and make. Generated files will be place inside "wasm" folder

```bash
make
```

## Usage

To make use of the client, create a ircController class through importing the emscripten generated ircppwasm.js file

```javascript
<script src="./wasm/ircppwasm.js">/*IMPORT*/</script>
<script>
  var irc;
  var module;

  async function init() {
    module = await Module();
    irc = new module.ircController();
    return module;
  }
  const m = init();
</script>
```

## Contributing

The project is missing a couple of functionalities, when all commands are implemented, see [inspIRCd's commands](https://docs.inspircd.org/3/commands/). Then I'll update this describign how to contribute.

## License

[Mozilla Public License 2.0](https://choosealicense.com/licenses/mpl-2.0/)
