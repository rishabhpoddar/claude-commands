# Claude Command: Create blog post draft

The purpose of this command is to create draft blog posts for twitter articles and for my own website.

## High level plan
I have several work log files in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/logs`. I need to convert them to blog post drafts (one log file to one blog, or many log files to one blog, depending on if they talk about the same thing or not).

## What to do
1. Find a file called `last_work_log.md` in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs`. If it doesnt exist, that means none of the logs have been converted to blog posts yet. So therefore all log files should be considered.
2. If the `last_work_log.md` file exists, then read it and it will tell you the last work log file that was converted to a blog post. So only consider newer log files (each log file is named like `YYYY-MM-DD_HH-MM-SS.md`).
3. For all newer log files, read them, and create a list of blog post titles, and append then in a file called `blog_post_titles.md` in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs`.
4. Update the `last_work_log.md` file with the name of the latest work log file that was converted to a blog post.
5. Now go through each blog post title, and create a draft blog post for each of them. The draft blog post should be a markdown file in the `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs/drafts` directory. The file name should be the blog post title (replace spaces with a "-"). You can refer to the associated log files to get the content for it.
    a. The reader of the blog post has no prior knowledge about my projects or my work or the context around the work log. So if you are referring to my project name, then you should first explain what the project is and the context around it.
    b. If the blog post is technical, you can assume that the reader knows how to code, but if referring to a specific tool in the market, don't assume that the reader knows about it. You should giver a short intro to the tool and what it does.
    c. Keep the blog post interesting and engaging.
    d. You can see a few example blog posts that have been posted in the `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs/posted` folder
6. After each blog post is created, remove the associated title from the `blog_post_titles.md` file (keep the other titles that are still pending). If no titles are left, then delete the `blog_post_titles.md` file.
7. After everything is done, git add, commit and push the changes to the remote repository.