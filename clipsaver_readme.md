# ClipSaver (v2.0.0)

This workflow is triggered with the `cs` keyword by default.

It presents images from Alfred's clipboard history via a Script Filter, and allows selecting an image to be extracted, converted to a format of your choice (default is PNG) and placed in a folder of your choosing (default is on the Desktop, in a folder called `saved_clips`). You can optionally set the `save_to_current` environment variable to have the workflow save to the currently active Finder window.

Upon success, the original clipboard entry as well as the .tiff from Alfred's database will be removed.

## Workflow Variables

- `db_name` defaults to `clipboard.alfdb`
- `db_path` defaults to `Library/Application Support/Alfred/Databases`
- `dest_dir` where to save images if `save_to_current == false`, defaults to `Desktop/saved_clips` (required)
- `sf_clip_limit` (default: empty) you can optionally specify a limit to constrain the number of results displayed in the Script Filter
- `save_to_current` (default: false) - set to `true` if you want the workflow to put saved images in the directory of the "frontmost" Finder window
- `default_format` - set to e.g. `jpeg`, `png` etc (use `sips --formats` to see all available formats). You can override per invocation by passing as an argument.

## Usage Tips

- Tap `SHIFT` while navigating through Script Filter results to get a QuickLook preview of the image. While QL is displayed, you can use the Arrow keys to flip through results.
- Pass a number as an argument to the script to save X number of clips in bulk
- Pass an image format e.g. `jpeg` as an argument to override your default format

## Screenshot:
<img width=500 src=https://user-images.githubusercontent.com/1992842/148102272-1e6e8cf5-08c1-4f3e-add5-63b56225ba3c.png>

## Download:
https://github.com/luckman212/alfredworkflows/blob/master/ClipSaver.alfredworkflow?raw=true

## Forum topic:
https://www.alfredforum.com/topic/14400-clipsaver-save-images-from-clipboard-history-to-png-files/
