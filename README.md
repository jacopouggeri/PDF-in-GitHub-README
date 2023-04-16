# PDF in GitHub README.md

This is a workaround to the fact that PDF files are not displayed when linked in `README.md`.
The shell script pdftopng.sh generates png files for each page in your pdf and adds them to `README.md` so they can be shown there.

To use this script, copy it in the directory of your project and run

```shell
./pdftopng.sh
```

This will generate a `png` folder with all your pages converted to the png format. 

Then it will generate the link to the files at the end of your `README.md` like this:

```md
![Page <n>](png/<filename>-<n>.png)
```
Where `<filename>` is the name of your pdf file and `<n>` the page number. When the script is run again, only the missing pages will be added.

The default backgorund color is white. If you want a transparent background, you can run:
```shell
./pdftopng.sh -a
```
