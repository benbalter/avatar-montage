# Avatar Montage

*Create a tiled montage (or collage) of GitHub Avatar images for use in all hands and other "welcome" or "thank you" slides*

This repo contains two tiny bash scripts in the `scripts/` directory. One to download avatars via `curl`, the other to create the montage via ImageMagick's `montage` command. 

Here's an example of what the resulting montage looks like using the first 98 GitHub users by user ID:

![montage](https://user-images.githubusercontent.com/282759/142458138-0210ba86-d5f2-4697-9f24-49cb60dee52e.png)

Of course you can customize the output. [See below](#customizing-the-output) for details. Don't need to control the output or are looking for something simpler? Check out @jhutchings1's hosted [Thank you builder](https://github.com/jhutchings1/thank-you-builder).
## Usage

1. Clone this repo locally and `cd` into the directory
2. Add a list of GitHub handles (without the `@`) to a `handles.txt` file, one handle per line
3. Run `script/download` to fetch the avatars
4. Run`script/create` to create the montage
5. Use the resulting `montage.png` file in your presentation

## Requirements

To run the scripts, you'll need:

* `curl`, and 
* `imagemagick`

Note: You can install both on MacOS with `brew bundle`

## Customizing the output

You can customize the output by passing additional arguments to `script/create`, e.g., `script/create -tile 10x` to force the montage to be 10 images wide. See [the ImageMagick montage documentation](http://www.imagemagick.org/Usage/montage/) for a list of available options.

## Credit

Credit goes to @martinwoodward for his "very quick ruby script to create a bash script that will create a montage" for the idea, and for pointing me towards the ImageMagick `montage` command.