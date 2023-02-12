# Atomic (old version)

This repository is a copy of the old version of the [Atomic color scheme](https://github.com/gerardbm/atomic). It has been saved into a parallel repository because it provides support for NetBeans, Sublime Text, xfce4-terminal and konsole, while the new version focuses only Vim/Neovim, URxvt and XTerm.

In the new version, colors have been selected using the color space HSLuv (different algorithm).

### Multiple colors for multiple applications

Atomic is a dark color scheme designed to use with terminal, Vim/Neovim and several GUI code editors. This repository also includes themes for some terminal applications (vim-airline, irssi, mutt, cmus, vifm...) and Zsh.

### Color palette

The color palette consists of sixteen precision colors selected procedurally (algorithms), distributed in six hues and four balanced Luma (Y'). Note that Luma (Y') is the perceived brightness; don't confuse it with the lightness of the HSL color model.

Human vision doesn't detect brightness linearly with color: in a pixel (R'G'B'), we see red color (#FF0000) darker than green color (#00FF00), and green color (#00FF00) brighter than red (#FF0000) and blue (#0000FF) colors.

So Luma (Y') has been balanced according to the ITU-R Recommendation BT.601:

`Luma (Y') = 0.299 R' + 0.587 G' + 0.114 B'`

This algorithm is also [suggested by W3C](https://www.w3.org/TR/AERT#color-contrast), however it's still open to change.

![Atomic-luma](https://github.com/gerardbm/old-atomic/blob/master/img/luma_diff.png)

In a RGB color wheel, hues have been selected in order to be distinguishable for the human eye and keeping harmony: two analogous colors (0° and 30°), their complementary (180° and 210°) and tetrad (90° and 270°).

![Atomic-hues](https://github.com/gerardbm/old-atomic/blob/master/img/hues.png)

**Dark mode, blue**

![Atomic-scheme](https://github.com/gerardbm/old-atomic/blob/master/img/dark-mode-blue.png)

**Dark mode, cyan** (base colors alternative with hue 180°)

![Atomic-scheme](https://github.com/gerardbm/old-atomic/blob/master/img/dark-mode-cyan.png)

In the previous palettes, hues of **base colors** (1, 8, 9 and 16) are 210° and 180° respectively, so colors have more blue and green than red. During the day, these colors don't carry any problem, but at night blue light negatively affects health and sleep patterns: it affects levels of the sleep-inducing hormone melatonin more than any other wavelength.

Night modes use different hues of base colors: 30° and 0° instead of 210° and 180° (actually, they are their respective complementary colors). That means values of blue and green colors have been reduced inversely, while value of red color has been increased in the same proportion.

**Night mode, orange** (base colors alternative with hue 30°)

![Atomic-scheme](https://github.com/gerardbm/old-atomic/blob/master/img/night-mode-orange.png)

**Night mode, red** (base colors alternative with hue 0°)

![Atomic-scheme](https://github.com/gerardbm/old-atomic/blob/master/img/night-mode-red.png)

**Light mode**

Light mode is useful when the screen receives a high illumination or we have to code in a very bright environment. Our eyes will not have to adapt the light sensibility every time we look at the screen.

Luma (Y') of this palette has been calculated keeping the proportion of the other palettes and inverting the values, so there is a symmetry between dark and light palettes.

However, Luma (Y') is not linear, so this symmetry entails lower contrast between foreground and background on a brighter background. That means colors with Luma (Y') 50% are not valid [WCAG 2.0 AA](https://www.w3.org/WAI/WCAG2AA-Conformance): their contrast values are between 1:2.2 and 1:3.2 (from 1:3.1 is ok, though).

Hue of base colors is 45° for this palette.

![Atomic-scheme](https://github.com/gerardbm/old-atomic/blob/master/img/light-mode.png)

### Code editors and IDEs

- [x] Terminal
	- URxvt
	- XTerm
	- xfce4-terminal
	- konsole
- [x] [Vim and Neovim](https://github.com/gerardbm/vim-atomic)
	- [x] Vim-airline
- [x] NetBeans IDE
- [x] [Sublime Text](https://github.com/gerardbm/sublime-atomic-scheme)

### Themes

- [x] Irssi
- [x] Mutt
- [x] Cmus
- [x] Vifm
- [x] Zsh

## Installation

Atomic themes for cmus, irssi, mutt, vifm and zsh can be installed using the script `install.sh`. For example, to copy `atomic.zsh-theme` into its path use the following command:

`./install.sh -m copy zsh`

If you want to 'symlink' instead of 'copy', use the symlink option:

`./install.sh -m symlink cmus irssi`

Atomic colorscheme for Vim and Neovim can be installed directly from the following repository: [gerardbm/vim-atomic](https://github.com/gerardbm/vim-atomic).

Atomic theme for vim-airline is available from the official repository, just type: `:AirlineTheme atomic`.

Atomic colorscheme for Sublime Text is available from the official package manager.

For more specific information, read the following articles:

1. Installation for [terminals](https://github.com/gerardbm/atomic/blob/master/INSTALL_TERM.md) (URxvt, XTerm, xfce4-terminal, konsole).
2. Installation for [code editors](https://github.com/gerardbm/atomic/blob/master/INSTALL_EDITORS.md) (Vim, Neovim, Sublime Text, NetBeans, vim-airline).
3. Installation for [command-line tools](https://github.com/gerardbm/atomic/blob/master/INSTALL_TOOLS.md) (cmus, irssi, mutt, vifm, zsh).

- - -

## Font family

Atomic is designed to look good with any kind of typography, as colors are distinguishable to any thickness.

Some themes (vim-airline, zsh) require the installation of Powerline fonts.
URL: https://github.com/powerline/fonts

- - -

## The values

**Dark mode, blue**

```
ID  ATOMIC COLORS   LUMA    HUE    HEX    (R - G - B)   (H -- S -- L)
--  -------------  ------  ----  -------  -----------  ----------------
 1  Base 01          10%   210°  #141A1F   20  26  31  210°  21%  10.0% |
 9  Base 02          13%   210°  #1A2128   26  33  40  210°  21%  13.0% | Base
 8  Base 03          50%   210°  #6B859E  107 133 158  210°  21%  52.0% | Colors
16  Base 04          70%   210°  #A6B5C5  166 181 197  210°  21%  71.0% |
--  -------------  ------  ----  -------  -----------  ----------------
 2  Dark Red         50%     0°  #EC5252  236  82  82    0°  80%  62.3% |
 4  Dark Orange      50%    30°  #C97016  201 112  22   30°  80%  43.8% |
 3  Dark Green       50%    90°  #5DA713   93 167  19   90°  80%  36.3% | Dark
 7  Dark Cyan        50%   180°  #13AFAF   19 175 175  180°  80%  38.2% | Accent
 5  Dark Blue        50%   210°  #3890E9   56 144 233  210°  80%  56.6% |
 6  Dark Violet      50%   270°  #A359ED  163  89 237  270°  80%  63.8% |
--  -------------  ------  ----  -------  -----------  ----------------
10  Light Red        70%     0°  #FF9191  255 145 145    0° 100%  78.5% |
12  Light Orange     70%    30°  #EDA55D  237 165  93   30°  80%  64.6% |
11  Light Green      70%    90°  #9ACD68  154 205 104   90°  50%  60.5% | Light
15  Light Cyan       70%   180°  #6ECFCF  110 207 207  180°  50%  62.0% | Accent
13  Light Blue       70%   210°  #7DBEFF  125 190 255  210° 100%  74.6% |
14  Light Violet     70%   270°  #CB96FF  203 150 255  270° 100%  79.5% |
```

**Dark mode, cyan** (base colors alternative)
```
ID  ATOMIC COLORS   LUMA    HUE    HEX    (R - G - B)   (H -- S -- L)
--  -------------  ------  ----  -------  -----------  ----------------
 1  Base 01          10%   180°  #121C1C   18  28  28  180°  21%   9.0% |
 9  Base 02          13%   180°  #172424   23  36  36  180°  21%  11.6% | Base
 8  Base 03          50%   180°  #5E8F8F   94 143 143  180°  21%  46.5% | Colors
16  Base 04          70%   180°  #99BDBD  153 189 189  180°  21%  67.0% |
```

**Night mode, orange** (base colors alternative)
```
ID  ATOMIC COLORS   LUMA    HUE    HEX    (R - G - B)   (H -- S -- L)
--  -------------  ------  ----  -------  -----------  ----------------
 1  Base 01          10%    30°  #1E1813   30  24  19   30°  21%   9.6% |
 9  Base 02          13%    30°  #251F18   37  31  24   30°  21%  12.0% | Base
 8  Base 03          50%    30°  #957B62  149 123  98   30°  21%  48.4% | Colors
16  Base 04          70%    30°  #C0AF9F  192 175 159   30°  21%  68.8% |
```

**Night mode, red** (base colors alternative)
```
ID  ATOMIC COLORS   LUMA    HUE    HEX    (R - G - B)   (H -- S -- L)
--  -------------  ------  ----  -------  -----------  ----------------
 1  Base 01          10%     0°  #211515   33  21  21    0°  21%  10.6% |
 9  Base 02          13%     0°  #2B1C1C   43  28  28    0°  21%  14.0% | Base
 8  Base 03          50%     0°  #A27171  162 113 113    0°  21%  54.0% | Colors
16  Base 04          70%     0°  #C7A9A9  199 169 169    0°  21%  72.0% |
```

**Light mode**

```
ID  ATOMIC COLORS   LUMA    HUE    HEX    (R - G - B)   (H -- S -- L)
--  -------------  ------  ----  -------  -----------  ----------------
 1  Base 01          90%    45°  #EFE6C9  239 230 201   45°  55%  86.4% |
 9  Base 02          87%    45°  #EBDFBA  235 223 186   45°  55%  82.5% | Base
 8  Base 03          50%    45°  #8D815C  141 129  92   45°  21%  45.8% | Colors
16  Base 04          30%    45°  #554D37   85  77  55   45°  21%  27.5% |
--  -------------  ------  ----  -------  -----------  ----------------
 2  Dark Red         30%     0°  #C11C1C  193  28  28    0°  75%  43.2% |
 4  Dark Orange      30%    30°  #824100  130  65   0   30° 100%  25.5% |
 3  Dark Green       30%    90°  #346900   52 105   0   90° 100%  20.5% | Dark
 7  Dark Cyan        30%   180°  #006E6E    0 110 110  180° 100%  21.5% | Accent
 5  Dark Blue        30%   210°  #095CAE    9  92 174  210°  90%  36.0% |
 6  Dark Violet      30%   270°  #7C19DF  124  25 223  270°  80%  48.5% |
--  -------------  ------  ----  -------  -----------  ----------------
10  Light Red        50%     0°  #EC5252  236  82  82    0°  80%  62.3% |
12  Light Orange     50%    30°  #C97016  201 112  22   30°  80%  43.8% |
11  Light Green      50%    90°  #5DA713   93 167  19   90°  80%  36.3% | Light
15  Light Cyan       50%   180°  #13AFAF   19 175 175  180°  80%  38.2% | Accent
13  Light Blue       50%   210°  #3890E9   56 144 233  210°  80%  56.6% |
14  Light Violet     50%   270°  #A359ED  163  89 237  270°  80%  63.8% |
```
