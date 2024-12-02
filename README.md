[//]: # (README.md)
[//]: # (Copyright © 2024 Joel A Mussman. All rights reserved.)
[//]: #

![Banner Light](https://raw.githubusercontent.com/jmussman/cdn-fun/main/banners/banner-lod-xmodmap-light.png#gh-light-mode-only)
![Banner Light](https://raw.githubusercontent.com/jmussman/cdn-fun/main/banners/banner-lod-xmodmap-dark.png#gh-dark-mode-only)

# Fix bad CMD-key mapping on Ubuntu systems at Microsoft Azure

## Overview

Learn On Demand Ubuntu systems host at Microsoft Azure assume the client computer is Microsoft Windows, not Apple MacOS.
This creates a problem because the keymapping is not correct, most significantly ctrl-C (^C) will not work to terminate
the process in the terminal window.

In order to fix this problem the CMD (Windows) key mapping must be undone on the Learn On Demand Ubuntu computer.
This only applies when the client computer is Apple MacOS, not Microsoft Windows.

## Configuration - Ubuntu (Learn On Demand Host)
### .Xmodmap

1. Download the .Xmodmap file to the Ubuntu computer.
1. Copy the file to ~/.Xmodmap (home directory) for both the current user and root (/root is the home directory for root).
1. Add the command "xmodmap ~/.Xmodmap" to ~/.bashrc for both the current user and root.
This will initialize the map for every shell or terminal window that is started. 
1. Source the .bashrc file with ". ~/.bashrc" to initialize the character map in the current shell.

## License

The code is licensed under the MIT license. You may use and modify all or part of it as you choose, as long as attribution to the source is provided per the license. See the details in the [license file](./LICENSE.md) or at the [Open Source Initiative](https://opensource.org/licenses/MIT).


<hr>
Copyright © 2024 Joel A Mussman. All rights reserved.