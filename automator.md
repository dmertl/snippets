# OS X Automator Snippets

## Droplets

### Setup

Save the Automator workflow as an Application. Files dropped onto the Application will be received as input.

### Shell Scripts

Add a Run Shell Script action as the first input. Set Pass input to "as arguments". Dropped file path will be available as $@. Test by adding a Get Specified Finder Items action with a test file (remove before saving).

    echo "$@" > ~/input_test.txt

### Extension replacement

When converting file formats, often want to change the extension. Example changing input file extension to ".pdf" during pandoc conversion.

    pandoc -f markdown --smart -o "${@/%.*/}.pdf" "$@"
