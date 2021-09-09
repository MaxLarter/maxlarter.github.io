# maxlarter.github.io
Max Larter's website

Hi,
This is the github repo for my personnal / professional website. I don't have much skill at all this, and not very much time to develop it either. 
I hope to get more things up soon (today is Jan 30 2019, for reference!) like fieldwork photos and stuff (maybe some blogging?).
Anyway, thanks for reading!
Max.

in main folder:

.R.Rproj: rstudio project file
CVmake.Rmd: "knit" to update cv on website and plop out html and pdf of CV
make pub list.Rmd: "knit" to fetch publication list and citations from google scholar and update the publications/publications.html page on website

about.html: bio page; edit manually
index.html: home page; edit manually


_layouts default layout file (not used right now)
_pdfs pdf files of all my papers (hopefully up to date)
_site the github pages site automatically updated I think
css folder: css styles


<!---
cv folder: this is borrowed and modified from GUANGCHUANG YU https://github.com/GuangchuangYu/cv  huge props to him and also Nick Strayer who created it initially https://github.com/nstrayer/cv
-->

CV_larter.csv <- where to update CV items: 	
	the headers are pretty mixed up and un-intuitive:
	loc = left hand side under list-item headers
	title = main title / header at same level as dates
	institution = right hand side with maps pin, under list-item header
	start/end: dates in timeline, put end==9999 if current!
	descriptions are bullet points below, I think none have more than one level at the moment
	section = publications / work / etc <- which section of the CV to print to
	order = to specify the order in which they are printed out (only used for education at the moment)

put NA where empty or not needed
when updating pub list on website:
get pdf and add to _pdfs folder with sane name (avoid too many spaces)

get exact title of paper, and url of the file on the github _pdfs folder and add them to publications/pdf_urls.csv => formatted like this title,pdf_url - replace spaces with '%20'

then you can run knit "make pub list.Rmd" to update the publications table on the website 

also edit the CV file "CV_larter.csv" with the new item:
note the whole citation here is in the "title column of the csv file surrounded by ""
My name is **bolded**, journal is *italics*, check link to pdf (same as above in publication website page)
section is 'academic_articles', 
start and end is twice the same year
rest is NAs

NA,"Author list, ..., ..., **M Larter** et al. (YEAR) Title blablabla, *Journal italics* [pdf](https://github.com/MaxLarter/maxlarter.github.io/blob/master/_pdfs/link_to%20pdf.pdf)",NA,YEAR,YEAR,NA,NA,NA,academic_articles,NA

save and its good to output




credits:
I "borrowed" code from Auriel Fournier's website source code, hosted on github here: https://aurielfournier.github.io/. Both of us used Barry Clark's posts about making a website/blog using Jekyll and github pages. His work can be found here https://github.com/barryclark/jekyll-now and here https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/
Thanks!

The publication list https://maxlarter.github.io/publications/publications.html is built using code borrowed and modified from Thomas Hackl: https://thackl.github.io/automatically-update-publications-with-R-scholar - thanks for sharing, what a time saver!

Code for the icons in the footer was generated using SVG icon files from https://github.com/edent/SuperTinyIcons/tree/master/images/svg
and they were transformed to base64 for insertion into the css file using this tool: https://base64.guru/converter/encode/image/svg