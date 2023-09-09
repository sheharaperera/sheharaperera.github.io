# Minimalist Hugo Template for Academic Websites

This repository contains the source code to https://pascalmichaillat.org: an academic website created with [Hugo](https://github.com/gohugoio/hugo) and [PaperMod](https://github.com/adityatelange/hugo-PaperMod). The website is hosted on [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages).

The code is publicly available as a template repository so anyone can generate a new repository with the same directory structure and files, and quickly create their own academic website. The code might also be helpful to anyone who wishes to learn about Hugo or wants to recreate specific features of this website.

## Documentation

The source code is documented at https://pascalmichaillat.org/d5/.

## Features

The PaperMod theme is modified in several ways to be more adapted to academic websites:

+ Webpages are organized in three categories, which are available from any page through the menu and from the homepage through buttons: 
	* Papers
	* Courses
	* Design projects
+ A list of tags (keywords) used in papers and courses is automatically generated so visitors can easily see the topics covered in research and teaching
+ The website provides social icons specific to academia: office hours, Zoom, Substack, Google Scholar
+ The metadata for webpages, which appear below the webpage title, are tailored to the academic context
+ Color scheme, font, spacing, buttons, and general appearance have been streamlined and made as minimalist as possible
+ The website provides new archetypes for paper pages, course pages, an archive page, and a search page

## Installation

+ Clone the repository to your local machine
+ Install [Hugo](https://gohugo.io/installation/). On a Mac, this is easily done with [Homebrew](https://brew.sh): simply run `brew install hugo` at the command line.
+ Since the website is hosted on GitHub Pages, having [GitHub Desktop](https://desktop.github.com) is very convenient to update the website.

## Usage

### Website development

To check that everything works, experiment with the code, and slowly develop your website, start by rebuilding the website locally. From the repository, run `hugo server` at the command line. The command builds the website with Hugo and starts a local web server. The website is then available at http://localhost:1313 in any web browser. Hugo automatically rebuilds the site and refreshes the web page in the browser as changes are made to the files (content, templates) in the repository. This allows you to see changes instantly as you are developing your website. 

### Website deployment

Once your website is ready to be made public, run `hugo` at the command line from the repository. This command will convert content files into HTML pages, handles static assets, generates URLs and organizes pages, and finally compile the website into the `public` folder for deployment.



### Google Analytics

The website supports Google Analytics 4. But do not forget to update the Google Analytics ID in `config.yml`. 

+ Either replace the ID `G-97G4MZ4061` with your own ID in the line `googleAnalyticsID: "G-97G4MZ4061"`. 
+ Or simply comment the line `googleAnalyticsID: "G-97G4MZ4061"` if you do not wish to use Google Analytics.

### Static files

The files in the `static` folder are PDF files and images to which the website links. All the files currently in the `static` folder pertain to this website and can be safely deleted, with the exception of the following files:

+ `picture.jpeg` is the picture appearing on the homepage. Replace it with your own picture.
+ `cv.pdf` is the CV linked to the CV icon on the homepage. Replace it with your own CV.
+ `favicon.io`, `favicon-32x32.png`, `favicon-16x16.png`, and `apple-touch-icon.png` is the favicon appearing in the menu bar next to the website title, and in the browser next to the URL. Replace it with the [favicon of your choice](https://favicon.io).

### Public folder

The `public` folder contains the fully generated static website files that are ready to be deployed to GitHub Pages. When you run the `hugo` command, Hugo processes your content, templates, and other project files and generates a static website. The resulting output is placed in the `public` folder by default.

The `public` folder can therefore be  safely deleted. A new version of the `public` folder will be created when you run the `hugo` command from your own repository.

## Speed

Despite the modifications to the PaperMod theme, the website continues to perform well on mobile and desktop devices. Here is an overview of the mobile performance from [PageSpeed Insights](https://pagespeed.web.dev/):

<img width="448" alt="mobile" src="https://github.com/pmichaillat/pmichaillat.github.io/assets/85443660/b54395b0-f9cb-4ad7-8daa-5f86e5f2cddc">

And here is an overview of the desktop performance:

<img width="453" alt="desktop" src="https://github.com/pmichaillat/pmichaillat.github.io/assets/85443660/eff134d2-6097-4bc2-bfd7-4f5c18571789">

Here are the [full report on mobile performance](https://pagespeed.web.dev/analysis/https-pascalmichaillat-org/hl96ythdue?form_factor=mobile) and the [full report on desktop performance](https://pagespeed.web.dev/analysis/https-pascalmichaillat-org/hl96ythdue?form_factor=desktop).

## License

+ The code used to generate this website is licensed under the terms of the MIT License.
+ Except where otherwise noted, the content of this website was created by Pascal Michaillat and is licensed under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
