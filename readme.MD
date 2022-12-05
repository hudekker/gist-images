# What is this repo?

This is an online addressable repo for all of your gist images. A copy of all your gists' images is stored here and all your gists will reference this repo for their image markdown addresses.

# How to use your gist-images repo

## Create a Github Page for this repo

You don't need an html document. Just create a Github Page and these images folders will be accessible online. To create a Github Page, go to Settings for this repo and then Pages

## Copy your images folder from your local markdown to this repo

Copy your images folder from your local markdown to this gist-images repo and rename the folder to `<your-gist-name>`. This will allow you to address your images by your gist's name.

### Local gist

<br>

![local-gist](https://hudekker.github.io/gist-images/readme/local-gist.png)

### Local gist images repo

<br>

![gist-images-repo](https://hudekker.github.io/gist-images/readme/gist-images.png)

## Commit and push this repo to Github

This makes your images folder accessible to both your local markdown and your gist

## In your local markdown folder,

- Create .gitignore and add .gitignore and your images folder name because you do not want this images folder to go to Gist. Actually gists do not support folders but this way you will avoid the push error.

  _.gitignore_

  ![gitignore](https://hudekker.github.io/gist-images/readme/gitignore.png)

- In your markdown document globally replace the image folder reference with your Github Page directory. Markdown images are of the form `![label](images/my-image.jpg)` so a "safe" global replace may be Find `](images/` and Replace with `](https://<your-account-name>.github.io/gist-images/<your-gist-name>/`. You don't want to replace the word 'images', just the images directory reference in the image markdown.

  _Before global replace_

  ```css
  ![ocean-waves](images/my-image.jpg)
  ```

  _After global replace_

  ```css
  ![ocean-waves](https://<your-account-name>.github.io/gist-images/<your-gist-name>/my-image.jpg)
  ```

## Push your gist

Your local markdown and your gist will both reference your Github Page directory of the images.

## Maintenance

If you add or change images, then remember to add/change the images in your local gist-images-repo and push.
