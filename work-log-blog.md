# Claude Command: Create blog post for work logs

The purpose of this command is to create draft blog posts for twitter articles and for my own website.

## High level plan
I have several work log files in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/logs`. I need to convert them to blog post drafts (one log file to one blog, or many log files to one blog, depending on if they talk about the same thing or not).

## What to do
1. Find a file called `last_work_log.md` in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs`. If it doesnt exist, that means none of the logs have been converted to blog posts yet. So therefore all log files should be considered.
2. If the `last_work_log.md` file exists, then read it and it will tell you the last work log file that was converted to a blog post. So only consider newer log files (each log file is named like `YYYY-MM-DD_HH-MM-SS.md`).
3. For all newer log files, read them, and create a list of blog post titles, and append then in a file called `blog_post_titles.md` in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs`.
4. Update the `last_work_log.md` file with the name of the latest work log file that was converted to a blog post.
5. Now go through each blog post title, and create a draft blog post for each of them. The draft blog post should be a markdown file in the `/Users/rishabhpoddar/Desktop/trythisapp/work_log/blogs/drafts` directory. The file name should be the blog post title (replace spaces with a "-"). You can refer to the associated log files to get the content for it. Use the /blog-writing skill to write the blog posts.
6. After each blog post is created, remove the associated title from the `blog_post_titles.md` file (keep the other titles that are still pending). If no titles are left, then delete the `blog_post_titles.md` file.
7. After everything is done, git add, commit and push the changes to the remote repository.