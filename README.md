# Image To RGB Array
Script which converts an image to a C array. Can be used to create images to load onto a DE1-SoC board. <br />
**Usage:**<br />
```
python3 image_to_rgb_array.py [-h] [--image_path IMAGE_PATH] [--file_path FILE_PATH] [--array_name ARRAY_NAME]
```
| Argument  | Description |
| ------------- | ------------- |
| image_path  |The path of the image. Relative is OK  |
| file_path  | The file path for the outputted header file. Relative is OK.  |
| array_name  | The name of the array variable e.g. unsigned short int **var_name**  |

**Examples:**<br />
```
python3 image_to_rgb_array.py --image_path cats.jpeg --file_path cats.h --array_name array_of_cats
python3 image_to_rgb_array.py --image_path ../doggos/dogs.jpeg --file_path ~/project/dog_stuff.h --array_name doggo_array
```
**Notes:** 
1. If you want the image to fit the screen it should have dimensions X:320, Y:240. Otherwise it will be displayed incorrectly.<br />
2. The type used by this script is "unsigned short int" 
3. Imageio is a required dependency. Install it using pip or conda.
4. There are no promises this is bug free :-)
This script uses imageio for the bulk of the image intake handling.<br />
List of supported image formats can be found on the imageio website<br />
See: https://imageio.readthedocs.io/en/stable/formats.html<br />
