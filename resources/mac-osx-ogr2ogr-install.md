# mac osx ogr2ogr install

to install ogr2ogr with libkml support you need to download an installer, rather than using homebrew which downy build ogr2ogr with libkml support

## download the mac gdal installer

download the latest gdal mac installer

[https://www.kyngchaos.com/software/frameworks/](https://www.kyngchaos.com/software/frameworks/)

## edit your shell config

edit your shell config and add the path to the gdal framework

### if you arre using bash edit your ~/.bashrc

```bash
vi ~/.bashrc
```

### if you arre using zsh edit your ~/.zshrc

```bash
vi ~/.zshrc
```

### add the following code to your shell config

```bash
if [ -d "/Library/Frameworks/GDAL.framework/Programs" ]; then
   PATH="/Library/Frameworks/GDAL.framework/Programs:$PATH"
fi
```

### source your shell config

if you are using the bash shell source your ~/.bashrc

```bash
source ~/.bashrc
```

if you are using the zsh shell source your ~/.zshrc

```bash
source ~/.zshrc
```

