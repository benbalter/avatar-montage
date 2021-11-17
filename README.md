# Avatar Montage

*Create a tiled montage of GitHub Avatar images for use in all hands and other "welcome" or "thank you" slides*

Don't need to control the output or are looking for something simpler? Check out @jhutchings1's hosted [Thank you builder](https://github.com/jhutchings1/thank-you-builder).

## Usage

1. Clone this repo locally
2. Add a list of GitHub handles (with the `@`) to `handles.txt`, one handle per line
3. Run `script/download` to fetch the avatars
4. Run`script/create` to create the montage
5. Use the resulting `montage.png` file in your presentation

## Requirements

* `curl`
* `imagemagick`

Note: You can install both on MacOS with `brew bundle`

## Customizing the output

You can customize the output by passing additional arguments to `script/create`, e.g., `script/create tile 10x` to force the montage to be 10 images wide. See [the ImageMagick montage documentation](http://www.imagemagick.org/Usage/montage/) for a list of available options.

## Credit

Credit goes to @martinwoodward for his "very quick ruby script to create a bash script that will create a montage" for the idea, and for pointing me towards the ImageMagick `montage` command.