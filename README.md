# filebiner
A bash script that uploads and manages files on https://filebin.net

```
Usage: filebiner <argument> [subarguments]

Arguments:

upload, up          Upload a file to filebin.net
    Subarguments:
    --bin, -b       The bin name to use (optional; defaults to '$USER')
    --name, -n      The name of the file (optional; defaults to name of file being uploaded)
    --file, -f      The path of the file being uploaded (required)
    Ex: 'filebiner upload --file ~/filename.extension --bin mybin --name myfile.extension'

list, ls            List files in a bin on filebin.net
    Subarguments:
    --bin, -b       The bin name to use (optional; defaults to '$USER')
    --names, -n     Show files by names instead of full urls (optional)
    Ex: 'filebiner list --bin mybin --names'

download, dl        Download a file from filebin.net
    Subarguments:
    --bin, -b       The bin name to use (optional; defaults to '$USER')
    --all, -a       Download all files in specified bin to a tar archive
    --name, -n      The name of the file to download (required unless --all used)
    --output, -o    The path and filename to save the file as (optional; defaults to ~/Downloads/<name of file>)
    Ex: 'filebiner download --bin mybin --name myfile.extension'

remove, rm          Remove a file from a bin on filebin.net
    Subarguments:
    --bin, -b       The bin name to use (optional; defaults to '$USER')
    --name, -n      The name of the file to remove (required)
    Ex: 'filebiner remove --bin mybin --name myfile.extension'

--yes, -y           Always answer 'yes' to all questions without showing prompts.
    Ex: 'filebiner --yes remove --bin mybin --name myfile.extension'
```
