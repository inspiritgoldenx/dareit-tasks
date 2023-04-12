# task 2
## the main goal was *to host a static website in a GCS bucket.*
1.  I opened the (console.cloud.google.com) and chose on the *Navigation Menu* --> *Cloud Storage* --> *Bucket* and clicked on **create bucket**
2.  I've created a bucket named: **example-bucket-070**. It is important that the bucket name has to be unique across ALL projects that exist in GCP. For example, when we create a bucket named: ml-unique-bucket-name we will got an error
3. While creating the bucket according to the instruction, I have chosen: *location type* --> **multi-region: eu (multiple regions in European Union)** and:
4. *storage class for your data* --> **set a default class**
5. *control access to objects* --> unchecked the **Enforce Public access prevention on this bucket**, and chosen **uniform*
6. *how to project object data* --> **none**
7. after chosen all this settings, I clicked **create**
8. in the second step, I created repository folder called [task_2](https://github.com/inspiritgoldenx/dareit-tasks/tree/main/task_2) with two files
9. the first one was called: ***website_url*** the second one: ***index.html***
10. in the content of the ***index.html*** I inserted:
```
<!DOCTYPE html>

<html>

  <head>

    <title>Hello World: Static Website</title>

  </head>

  <body>

    <h1>I am hosted on a bucket in GCP.</h1>

    <p>DareIT rocks!</p>

  </body>

</html>
```
11. after this, I have uploaded the *index.html* file to my bucket *example-bucket-070* in Google Cloud (it can be done easily done by dragging and dropping the file in the browser)
12. and made the website accessible by others by changing the permissions, in this case I went to the *permissions tab* and clicked **GRANT ACCESS**
13. in the *new principals* I wrote **allUsers** and selected a role called **Storage Object Viewer**, thanks to that anybody will be able to view the files
14. after clicking **save** and confirming: **Allow Public Access**, I copied the public url of the object and pasted it into my browser
15. the look:
16. ![dareITbucketpic](https://user-images.githubusercontent.com/125319277/231567020-5ab958e7-e935-40fe-a021-a82141828953.jpg)

