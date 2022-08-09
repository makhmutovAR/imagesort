﻿# ImageSort

This script sorts images by their resolutions from the INITIAL folder to the TARGET folder.
In the target folder new directories named "Width x Height" (for example, "1920x1080") will be created.

* if target folder doesn't exist then it will be created;
* if folder already exists files will be added there;
* if the file with the same name already exists, then the new file will be renamed:
  "({number})" will be added to its name (for example, "wallpaper(3)").

All images from the nested directories in the initial folder will be sorted too.

* files for which resolution couldn't be determined will be copied or moved to the directory "Not images" in the target folder.


## To run script:
`\..\imagesort.py mode "initial folder" "target folder"`

### mode = dryrun, copy, move, sort
* `dryrun "initial_dir" "report_dir"` sorts files from "ini_dir" and generates html report in "report_dir"
* `copy "initial_dir" "target_dir"` sorts and copies files from "initial_dir" into "target_dir"
* `move "initial_dir" "target_dir"` sorts and moves files from "initial_dir" into "target_dir"
* `sort "initial_dir"` sorts files into "initial_dir" and deletes the initial files


## Script runs on Python 3.9, with next modules:
* `hashlib`, `os`, `pathlib`, `shutil`, `stat`, `sys` (standard libraries)
* `argparse`, `Chameleon`, `Pillow`  (3rd party libraries)

### The 'imagesort_tests.py' tests ImageSort
* `bs4`, `json`,`tempfile`, `unittest` additionally are used for testing