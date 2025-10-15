# Tiny Tapeout Datasheet Artwork

This repo is intended to provide easy access to artwork which is dedicated to Tiny Tapeout. Its contents are used by the
shuttle "build datasheet" action to showcase photos and renders from the team and community.

Details of each photo (such as its title and artist) can be found within the `manifest.yaml` file. New photos must be
added to `manifest.yaml` and the required fields filled out so that the build action can make use of the images.

## Structure of `manifest.yaml`

There can be one or more dictionaries at the root of this file. The key of these dictionaries must correspond to a
folder within the root of this repo, i.e. "artwork" or "backgrounds".

The values of these root dictionaries can be one or more dictionaries where its key is an unique ID for an image,
and its value consists of the keys shown below.

| key       | required  | scope    | description                                |
| :-------- | :-------- | :------- | :----------------------------------------- |
| file      | yes       | all      | file path of image (relative to root key)  |
| title     | yes       | artwork  | title of the artwork                       |
| artist    | yes       | artwork  | author of the artwork                      |
| designer  | no        | artwork  | author of the design being illustrated     |

Depending on the scope of the image, only some keys may need to be specified. Anything which is used as artwork in
the datasheet must have its attribution information filled out before being made available.

The filepath string is relative to the root key. For example, if the root key = "artwork", and file = "example.jpg"
then the resolved filepath will be `artwork/example.jpg`.