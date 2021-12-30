# pandoc_html_gen

cmake project for pandoc html generation.

# Usage

```bash
mkdir build
cmake ..
make
```

In CMakeLists.txt, use add_html_target function.  
add_html_target take 2 variable.  
TARGET_NAME and SRC_FILE.

TARGET_NAME is the target name.  
TARGET_NAME.html is the artifacts.  
SRC_FILE is markdown file.  
note that only one SRC_FILE is valid.  

# License

This software is released under the Apache 2.0 License where except otherwise indicated, see LICENSE.
