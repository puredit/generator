# Generator
An application for generating code pattern templates and projection components from samples.

## Using the generator
Add the generator to your project by adding the following line to your `devDependencies`:
```json
"@puredit/generator": "https://github.com/puredit/generator.git"
```
Run `npm i`.

The sample-based generator takes a set of text files containing both code and projection samples as input.
All samples are divided by an empty line.
The code samples are divided from the projection samples by a line containing only `---`` as content.
You can look at the datasets in `examples` as a reference.
Execute the generator as follows, replacing the argument placeholders with your according values:

```sh
npm start @puredit/generator -- \
    --language <language> \
    --parser-name <parser-name> \
    --parser-module <parser-module> \
    --projection-name <projection-name> \
    --samples <samples> \
    --target-dir <target-dir>
```

On Windows Powershell, `\` does not work for multiline commands, so write everything in one line instead:

```sh
npm start @puredit/generator -- --language <language> --parser-name <parser-name> --parser-module <parser-module> --projection-name <projection-name> --samples <samples> --target-dir <target-dir>
```

Note that the path of `parser-module` must be relative to the path of `target-dir`. 

A more practical example can be found in the [samples repository](https://github.com/puredit/samples).
