*Work in Progress*

# Session 11 - GitHub Pages with Jekyll

## How are files stored on a computer?

## Save your old website and setup Jekyll with GitHub Pages
So far you have created your website using basic HTML (content) and CSS (styling). The code was saved in a file named ```index.html```, and it was saved in a repository named YourUserName.github.io. By default, GitHub will look for such a file in a repository of that name and then load it when you enter the URL ```https.YourUserName.github.io``` in your webbrowser.

Creating a website with basic HTML and CSS gives you a lot of flexibility, but it is a tedious work, therefore we go for a simpler route as of now. 

First, we will rename the repository of your website to archive it and then continue to use the Jekyll framework on a new repository of name YourUserName.github.io to create our blog. Jekyll has the advantage that you do not need to bother about formatting the content, it comes with default styling "out of the box". HTML is replaced by a simple language called Markdown. It consists of simple tags that describe the function of the content (i.e. headline, link, image, ...). For example, a HTML```<h2>title</h2>``` headline becomes ```## text``` in Markdown.

For creating a post, you will need to place each post into a separate file inside a folder called ```_posts```. There are naming rules for the file and each file starts with a so called *YAML frontmatter* containing information like the author's name, a category to search posts later and more. Afterwards you add your content, using Markdown.

Before you start I suggest that you check out an existing repository using Jekyll ([example](https://github.com/mibrs/mibrs.github.io) is the repo for this website here), check the contents of the folders and look inside the files containing the posts. You can also copy and paste content, in particular the YAML Frontmatter and then make the changes of your own post.

Let's get started.

### Step 1 - Archive your exisiting website
Just open the repository containing your website and then follow steps 1 to 4. You will save it in a new repository under a different name.

![Rename repository](/media/221122RenameGhRepo.png)

You can still access your site with the URL ```https:YourUserName.github.io/NewRepositoryName```.

![Access Repo on Web](/media/221122GhAccessRepoOnWeb.png)

### Step 2 - Create your new website
Now we generate our new website with Jekyll.

#### Step 2.1 Find the Jekyll theme minima on GitHub.
All the styling inside Jekyll is defined inside themes. We are using the theme minima. You find it [here](https://github.com/jekyll/minima)

![Jekyll Minima on GitHub](/media/221122JekyllMinimaRepo.png)

#### Step 2.2 Fork ("copy") the repository with the theme to your own user account and name the repo ```YourUserName.github.io```

Make sure that you are logged into your own GitHub account. Then follow the images to
1. Create your **Folk** of the repository
2. Name it in the form ```YourUserName.github.io```.

**ATTENTION:** User your own UserName instead of ```mbbbraehler``` shown on the screenshot!

![Fork Minima](/media/221122ForkMinima.png)

![Rename Fork](/media/221122NameFolkGh.png)

#### Step 2.3 Configure GitHub to use Jekyll with your theme
Next, go back and open the repository, then choose Pages on the left side menu and make the entries as shown. Do not forget to click on ```Save``` once you are finished.

![Configure Gh Pages](/media/221122ConfigureGhPages.png)

#### Step 2.4 Finished
Now you need to wait for some time (seconds to minutes) before the changes are updated on the GitHub servers and you can access your website. The website contains a lot of content that you do not want to keep. Wait for Step 3 before you start to clean up and make the site your own.


### Step 3 - Create your first post
Next, open [this](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll#about-content-in-jekyll-sites) page and scroll down to **Adding a new post to your site**. Follow the instructions until step 8. Then choose for step 9 ```Commit directly to the main branch```. You are done! Give GitHub a few seconds to update your site, then check on ```YourUserName.github.io``` to see your website and open the post.

Another approach is to have a look at my site [mibrs](https://github.com/mibrs/mibrs.github.io), the repository is using the same theme. Just have a look how the posts and assets look like, copy and paste content as you please and then start to modify your own site as you like. Furthermore, I left some content from the Minima theme there (readme.md for the repository) as well as a post about Markdown. You can always look "behind the scene" as the repository is public and with editing or RAW you see the source code.

### If You Want to Know More ...

[This Video](https://youtu.be/iWowJBRMtpc) explains you how to install Jekyll on an Apple computer to develop a website locally before you are uploading the site to a webserver for public viewing. The second part of the video explains many useful concepts of Jekyll.

The video is already older and covers version 2 (As of January 2023 there is version 4.3). But this is actually an advantage as all configuration files at that time were easier to understand and the content still applies to today. So this video is a very suitable introduction to the inner workings of Jekyll. What folders/files are important for the configuration and the content? The following topics are covered in the video.

- How to configure the basic settings as name of your site, links and categories in *_config.yml*

![config.yml example](/media/230109_Jekyll_config.yml.png)

- How the files in the *_include* folder allow you to define the appearance of certain blocks and links (footer, header, head, social media)
- How the files in the *_layout* folder allow you to define the appearance of posts, pages.
- The folder *_posts* contains your actual posts. 

![Jekyll View of all Posts](/media/230109_Jekyll_Overview.png)

- Each post document has a *Front Matter* at the beginning that allows you to enter date, title, categories and other information you have set up in the configuration. These information allow you to arrange and find your posts. In order for the post to be identifyable, you must also respect a certain naming convention for the file, it should only contain letters and numbers and hyphens. The name should begin with the date in the form YY-MM-DD (Year with two numbers, MM with two numbers, DD day with the two numbers, ex. 22-01-09 is January 9th, 2022). The file name must end with *.md*. A valid name would be *22-01-09-This-is-a-post.md*.

![Post with Front Matter and HTML](/media/230109_Jekyll_Post.png)

- In the *_sass* folder you find the definition of CSS properties to control the appearance of the site. They are linked with the content pages using CSS class selectors.

You will always need to write posts according the specifications above. Each post needs to start with the Front Matter, afterwards you will mostly use Markdown as a simple way to enter your content. You can always add HTML tags when required, or refer to class selectors when necessary.

These information should give you a starting point if you want to discover Jekyll in more detail and customize its appearance.
