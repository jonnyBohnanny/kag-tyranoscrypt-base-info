# Making Cool Games with Friends in KAG3 Tyranoscrypt
 basic info for KAG and tyranoscrypt

# Why this Document Exists
This document was created to help facilitate collaboration on KAG / Tryranoscrypt projects. Some of the technology mentioned:
* Tyranoscrypt
* KEG
* HTML5 / javascrypt / tjs
* Visual Studio Code
* Midjourney
* Gituhb
* Faceapp
* Adobe Background Remover
* Gimp
* Chrome / Chromium
* imagemagic

# How to Make Stuff

## Git Hub
### Editing This Document in GitHub
This document is created with Markdown, it's how you make it look nice <https://www.markdownguide.org/basic-syntax/>

### Live Editor in GitHub
If you push the . (period button) on a git hub page you get a web version of Visual Studio Code, and it's pretty cool.

### Contributing to Shared Files
Contributing to a project is probably easiest through a GitHub account because GitHub is really great for sharing projec files. Not shilling 
for them but it works.


## KAG / Tyranoscrypt
### Tiny Gotacha
You have to change the language to Japanese -> English in the side navigation bar.

Language / syntax reference for KAG3
<https://kirikirikag-sourceforge-net.translate.goog/contents/index.html?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=en&_x_tr_pto=wapp>
### KAG Important Notes / Gotchas 
#### Background Scale / Crop
KAG does not seem to have a way to resize backgrounds - so make sure you crop scale as needed.

### Running Project in Crome or Cromium
If you want to run your KAG project to work in a local browser with no web server you need to give chrome access to your file system - probably don't use it for browsing though becaue I guess everything some how has aceess.

### Tiny Gotcha
Before running a session with local file access you have to close your other open windows or it won't work.

#### On Windows
You can run a session of crome that has local file access by entiner the following command into the windows Power Shell, or maybe `cmd.exe` (have not tried the `cmd.exe`)
Template for you to add your username:
```
Start-Process "C:\Users\<your username here>\AppData\Local\Chromium\Application\chrome.exe" "--allow-file-access-from-files"
```

Example using Jonny as a username:
```
Start-Process "C:\Users\Jonny\AppData\Local\Chromium\Application\chrome.exe" "--allow-file-access-from-files"
```

## Imagemagic
<https://imagemagick.org/script/download.php#windows>
<file:///C:/Program%20Files/ImageMagick-7.1.0-Q16-HDRI/index.html>

### Basic Example
Command example:
```
"C:\Program Files\ImageMagick-7.1.0-Q16-HDRI\magick.exe" mogrify -resize 640x960 *.png
"C:\Program Files\ImageMagick-7.1.0-Q16-HDRI\magick.exe" mogrify -resize 640x *.png
```

### Recursive Example
```
for /r "C:\Source\Folder\Root" %a in (*.*) do mogrify -resample 72 -resize 700x700 -format png "%~a"
```

## Powershell Bulk Rename
```
Get-ChildItem -File -Recurse | % { Rename-Item -Path $_.PSPath -NewName $_.Name.replace("My project (1).png","face_5.png")}
```

### Fixed Width
Use `-resize 100x` to resize images to 100 pixels in width while maintaining the height's aspect ratio.

Used to resize / crop images in bulk on the command line.

### Example Bulk Resize

## Midjourney
Midjourney is a cool place to generate character and background art.
<https://midjourney.gitbook.io/docs/user-manual>

### Respond With Emojis
* The mail emoji gets you the `--seed` argument.
* The red x emoji cangels and delets a run.

### Propmpt Notes
* Everything gets upscaled so don't worry about size but DO worry about setting a good ratio
** `--ar` is better supported and should be used instead ex: `--ar 1:4`
* Background images will need to be scaled or cropped to work with KAG3 
* Use `::` between prompts for a hard separator as describe in the answer above.

### Prompt Examples
#### Basic
```
/imagine prompt: http://myimageonline.jpg A forest spirit at night --iw 0.2 --no trees
```

* `[image URL] [text prompt]` with no weights specified results in a 20% image(s) / 80% text generation.
* `[image URL] [text prompt 1] --iw 1` Results in a 50% image(s) / 50% text generation.
* `[image URL] [text prompt 1]::2 [text prompt 2]::3 --iw 1` results in a 1/6=17% image(s) , 2/6= 33% text1 , 3/6 = 50% text2.
```

#### My Examples
### Best

/imagine prompt:dr. ghul, open eyes, standing in front of a pink gate::1.5 handsome face, wearing fine suit jacket on a bright day, HD, detailed, ultra-realistic, 8k, cinematic, looking directly at camera::1.6, centered::0.3 --ar 5:8 --upbeta --s 1250


/imagine prompt:dudeovergame, cool guy, open eyes, standing in front of a purple gate::1.5 handsome face, wearing fine suit jacket on a bright day, HD, detailed, ultra-realistic, 8k, cinematic, looking directly at camera::1.6, centered::0.3 --ar 5:8 --upbeta --s 1250

/imagine prompt:old man cooper smith, standing in front of a rainbow gate::1.5 serious face, wearing fine suit jacket on a bright day, HD, detailed, ultra-realistic, 8k, cinematic, looking directly at camera::1.6, centered::0.3 --ar 5:8 --upbeta --s 1250

Dale Blake, standing in front of a black gate::1.5 serious face holding a sandwich, wearing fine shorts on a bright day, HD, detailed, ultra-realistic, 8k, cinematic, looking directly at camera::1.6, centered::0.3 --ar 5:8 --upbeta --s 1250