# solarized.vim

A simpler fork of the awesome [Solarized colorscheme for Vim](https://github.com/altercation/vim-colors-solarized) by Ethan Schoonover, completely written from scratch.

What was removed? The degraded 256 color scheme, and all the functions and configuration options. Bold and underline attributes are enabled for both terminal and GUI modes. Italic is only enabled for GUI.

ERB templates are used to generate the colorscheme, so the code is easy to maintain and it runs fast in Vim.

## Requirements

For users of Vim in terminal mode, the terminal emulator color scheme must be set to the Solarized palette:
```
Term Color | Hex     | RGB
-----------|---------|------------
black      | #073642 |   7  54  66
red        | #dc322f | 220  50  47
green      | #859900 | 133 153   0
yellow     | #b58900 | 181 137   0
blue       | #268bd2 |  38 139 210
magenta    | #d33682 | 211  54 130
cyan       | #2aa198 |  42 161 152
white      | #eee8d5 | 238 232 213
brblack    | #002b36 |   0  43  54
brred      | #cb4b16 | 203  75  22
brgreen    | #586e75 |  88 110 117
bryellow   | #657b83 | 101 123 131
brblue     | #839496 | 131 148 150
brmagenta  | #6c71c4 | 108 113 196
brcyan     | #93a1a1 | 147 161 161
brwhite    | #fdf6e3 | 253 246 227
```

Configuration files for the main terminal emulators can be found in the [Solarized](https://github.com/altercation/solarized) repository.

## Installation

- Manual:

        curl -fLo ~/.vim/colors/solarized.vim --create-dirs https://raw.githubusercontent.com/ericbn/vim-solarized/master/colors/solarized.vim

- Using [pathogen.vim](https://github.com/tpope/vim-pathogen):

        cd ~/.vim/bundle
        git clone git://github.com/ericbn/vim-solarized.git

- Using [vim-plug](https://github.com/junegunn/vim-plug):

        Plug 'ericbn/vim-solarized'

## Configuration

Add one of the following to your `.vimrc`:

- For dark background:

        syntax enable
        set background=dark
        colorscheme solarized

- For light background:

        syntax enable
        set background=light
        colorscheme solarized

MacVim users will also want to configure their `.gvimrc` file, or add the following line to `.vimrc`:

    let macvim_skip_colorscheme = 1

## Contributing

- Edit the ERB files and run `erb solarized.vim.erb > colors/solarized.vim` to generate the colorscheme file. Ruby 2 required.
- Submit the changes in both the ERB and the colorscheme files.

## License

Copyright © Ethan Schoonover. Distributed under the same terms as Vim itself.
See `:help license`.
