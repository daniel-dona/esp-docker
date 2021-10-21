# Docker usage 

Go to the project root folder and then:

# Configure
```
docker run -it --rm -v $PWD:/project -w /project espressif/idf idf.py menuconfig
```

# Build
```
docker run --rm -v $PWD:/project -w /project espressif/idf idf.py build
```

# Flash
```
docker run --rm -v $PWD:/project -w /project --device /dev/ttyUSB0 espressif/idf idf.py -p /dev/ttyUSB0 flash
```

#  Monitor
```
docker run --rm -it -v $PWD:/project -w /project --device /dev/ttyUSB0 espressif/idf idf.py -p /dev/ttyUSB0 monitor
```

# Other options?
```
docker run --rm -v $PWD:/project -w /project espressif/idf idf.py help
```

For options that involves some interface (ncurses, etc...), add `-it` args to the Docker command. For options that comunicate with some device, use the `--device` arg on Docker command and `-p` on `idf.py` command.



